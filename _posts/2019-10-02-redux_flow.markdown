---
layout: post
title:      "Redux Flow"
date:       2019-10-02 15:26:04 +0000
permalink:  redux_flow
---



The simplest way to look at redux is to remember that at the core, the flow is always the same. 

**Action -> Reducer -> Updated State**

The first step is to call a function that takes in the arguments of (state, action). An action object is a POJO consisting of a key value pair. Our action object is passed into our reducer. The key (type) is called in our switch statement, which then (based on the type of key) updates state and returns it. Below is an example of a reducer. A reducer is a pure function, meaning 1. it always returns the same output if given the same input, and 2. it does not have any side effects outside of the function, only returns a value.

`function changeState(state, action){      
  switch (action.type) {
    case 'INCREASE_COUNT':
      return {count: state.count + 1}
    case 'DECREASE_COUNT':
      return {count: state.count - 1}
    default:
      return state;
  }
}
 
let state = {count: 0}

changeState(state, {type: 'INCREASE_COUNT'})
// => {count: 1}
 
changeState(state, {type: 'DECREASE_COUNT'})
// => {count: -1}`

