# Redux-Basic-Example
Redux-Basic-Example

Run: node index.


Redux is a PREDICTABLE STATE CONTAINER for JS APPS.
can be used with react, angular, vue, venilla JS

Redux - library for JS applications.
- is state container - store the state of your application
- state of an application - means all the individual components includes data & UI logic
- store & manage appln state

Predictable

#3 core concepts of redux
Store, Action , Reducer 

#3 principles 
1=> the state of your whole appln is stored in an object tree within a single store
2=> only way to change the state is to emit an action, an obj describing what happened .
-not allowed to update the state obj directly. { type: BUY-CAKE }
3=> to specify how the state tree is transformed by actions, you write pure reducers
pure reducers = pure functions .
reducre - (previousState, action) => newState

emit = dispatch is redux .
flow=<> dispatch an action, reducers handles an action and updates state(redux store) , state value is updated then the value is passed to appln bcz app is subscibed the store .
