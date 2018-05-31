VueJS: Ipsum Viewer
===

## Code Wars Challenge

Complete [today's Kata](https://www.codewars.com/kata/my-head-is-at-the-wrong-end).

## Lab

Recreate the ipsum viewer in VueJS. Displays a lists of ipsum's and when an ipsum is clicked, it shows a 
detail view with full information.

## Components

Your app components should be structured as follows (notice new `Ipsum` component):

```
App
  |
  + IpsumList
  |
  + IpsumViewer
```

## Component Details

* `App` 
    * owns the "selected" state (initially `null`), which is passed to both `IpsumList` and `IpsumViewer`
    * subscribes to `IpsumList` event `select`. Updates the selected state.
    * displays the two child components, passes `selected` prop to `IpsumViewer`
* `IpsumList`
    * Owns the "ipsum list" state (initially import of `js/data.js`) which it returns from `data() {}`
    * Emits the `select` event, _passing the corresponding ipsum object_ when item is clicked
    * Show name and category (maybe find images based on category?). Conditional add class to indicate ipsum is selected
* `IpsumViewer`
    * gets passed the `selected` via `props`
    * if `selected` is `null` displays message to make a selection
    * else shows detail view

## Requirements

* Use Vue CLI to create project (choose "merge" option)
* Move `data.js` to appropriate place in project and maybe name `ipsums.js`
* Use single-file vue components

## Rubric

* Project Structure and Organization **1pts**
* Use of VueJS components **3pts**
* Data passing and events **3pts**
* Feature/Functionality correct/works **3pts**
