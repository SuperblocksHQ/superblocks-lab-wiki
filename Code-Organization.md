# Folder Structure and source organization
At this moment, the application is in a small enough stage in which allow us to distribute the code in a folder by layer fashion. 

* Folder by layer: Each folder contains items that usually are not closely related to each other. This results in folders with low cohesion and low modularity, with high coupling between packages. As a result, editing a feature involves editing files across different packages. In addition, deleting a feature can almost never be performed in a single operation.

![Project folder structure](https://github.com/SuperblocksHQ/studio-wiki/blob/master/images/folder-structure.png)

**Note** This is not written in stone and as the project progresses and grows in complexity, we might revise this decision and start organising the code in a different way. 


# Redux and State Management
We decided to start using [Redux](https://redux.js.org/) to handle state across different components and write code which can grow in size and it is easy to test. 

Redux related logic is divided in the following folders:
 - **actions**: As the folder suggests, here we will include all the action functions required to be dispatch into our redux reducers. 
 - **reducers**: Our reducers will specify how the application's state changes in response to actions sent to the store. Remember that actions only describe what happened, but don't describe how the application's state changes.
 - **selectors**: Constant function which computes derived data from the state, allowing Redux to store the minimal possible state.
 - **store**: Object that brings `actions` and `reducers` together. The store has the following responsibilities:
    - Holds application state
    - Allows access to the state via getState()
    - Allows state to be updated via dispatch(action)
    - Registers listeners via subscribe(listener)
    - Handles unregistering of listeners via the function returned by subscribe(listener).


# CSS Styling (LESS)
We are using [Less](http://lesscss.org/) for all of our component's styling. They are compiled into CSS in build time, so be aware that when making changes to the styles included in a component, it will trigger an entire reload of the application itself. 

**NOTE:** Make sure when you are creating a new component, the style file is placed right next to the component's javascript implementation following the convention name of style.less.


