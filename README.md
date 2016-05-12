# Experimental.ChangeTracker.js

[![Join the chat at https://gitter.im/TrackableEntities/Experimental.ChangeTracker.js](https://badges.gitter.im/TrackableEntities/Experimental.ChangeTracker.js.svg)](https://gitter.im/TrackableEntities/Experimental.ChangeTracker.js?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Experimental repository for implementing change tracking in a JavaScrpt library.

## Design goals

1. Leverage a library which performs object graph traversal

2. Implement a strategy pattern:
  - Two callback methods called for each node
  - Callback 1: Process Node
    + Some work on the node
    + Argument(s): object reference
    + Return: result
  - Notify Result
    + Argument(s): object reference, result of Process Node

3. Change Tracker
  - Start tracking
    + Pass object root to graph traverser
    + Pass callbacks:
      - Iterate properties, construct state snapshot
  - Detect changes

4. State Snapshot
  - Object reference
  - Dictionary of property names and values
  - Snapshots for reference and collection properties

5. Change State
  - Reference to object
  - Dictionary: property names and values
  
