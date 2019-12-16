# Redux-Basic-Exampe
Redux-Basic-Exampe

const redux = require(&#39;redux&#39;)

const createStore = redux.createStore;

const BUY\_CAKE = &#39;BUY\_CAKE&#39;;

function byCake() {

    return {

        type: BUY\_CAKE,

        info: &#39;First Redux Action&#39;

    }

}

const initialState = {

    numOfCakes: 10

}

const reducer = (state = initialState, action) =\&gt; {

    switch (action.type) {

        case BUY\_CAKE: return {

            ...state,

            numOfCakes: state.numOfCakes - 1

        }

        default:

            return state

    }

}

const store = createStore(reducer)

console.log(&quot;Initial State: &quot;, store.getState());

const unsubscribe =  store.subscribe(() =\&gt; console.log(&quot;Updated State: &quot;, store.getState()));

store.dispatch(byCake());

store.dispatch(byCake());

store.dispatch(byCake());

store.dispatch(byCake());

unsubscribe();
