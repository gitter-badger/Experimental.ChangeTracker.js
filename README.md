# Experimental.ChangeTracker.js

Experimental repository for implementing change tracking in a JavaScrpt library.

## Design goals

1. Leverage a library which performs object graph traversal

2. Implement a strategy pattern
  - Traverser should invoke a callback method
  - Callback arguments:
    + Object reference
    + Result of property iteration
      
3. Change Tracker
  - Passes object graph to object traverser
  - Provides callback method
  - On callback, should construct change state object
  
4. Change State
  - Reference to object
  - Dictionary: property names and values
  
