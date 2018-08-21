# Folder Structure and source organization
At this moment, the application is in a small enough stage in which allow us to distribute the code in a folder by layer fashion. 

* Folder by layer: Each folder contains items that usually are not closely related to each other. This results in folders with low cohesion and low modularity, with high coupling between packages. As a result, editing a feature involves editing files across different packages. In addition, deleting a feature can almost never be performed in a single operation.

![Project folder structure](https://github.com/SuperblocksHQ/studio/blob/master/resources/images/folder-structure.png)

**Note** This is not written in stone and as the project progresses and grows in complexity, we might revise this decision and start organising the code in a different way. 


# Redux and State Management
We decided to start using [Redux](https://redux.js.org/) to handle state across different components and write code which can grow in size and it is easy to test. 

Redux related logic is divided in the following folders:
 - actions: As the folder suggests, here we will include all the action functions required to be dispatch into our redux reducers. 
 - reducers: Our reducers will specify how the application's state changes in response to actions sent to the store. Remember that actions only describe what happened, but don't describe how the application's state changes.
 - selectors: Constant function which compute derived data from the state, allowing Redux to store the minimal possible state.
 - store: Finally the **Store** is the object that bring actions and reducers together. The store has the following responsibilities:
    - Holds application state
    - Allows access to state via getState()
    - Allows state to be updated via dispatch(action)
    - Registers listeners via subscribe(listener)
    - Handles unregistering of listeners via the function returned by subscribe(listener).



