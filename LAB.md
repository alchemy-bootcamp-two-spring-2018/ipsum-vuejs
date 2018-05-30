Vue: Ipsum Viewer
===

## Code Wars Challenge

Complete [today's Kata.](https://www.codewars.com/kata/fixme-replace-all-dots)

## Lab

Recreate the ipsum viewer in VueJS. Displays a lists of ipsum's and when an ipsum is clicked, it shows a 
detail view with full information.

## Components

Your app components should be structured as follows (notice new `Ipsum` component):

```
App
  |
  + IpsumList
  |   |
  |   + Ipsum
  |
  + IpsumViewer
```

## Component Details

* `App` 
    * owns the "selected" state (initially `null`)
    * passes `IpsumList` a callback function, `onSelect`
    * displays the two child components
* `IpsumList`
    * owns the "ipsum list" state (initially import of `js/data.js`)
    * calls the passed `onSelect` when an ipsum is selected, _passing the corresponding object_ to the `onSelect` function
    * show name and category (maybe find images?)
* `Ipsum`
    * owns the "ipsum list" state (initially import of `js/data.js`)
    * calls the passed `onSelect` when an ipsum is selected, _passing the corresponding object_ to the `onSelect` function
    * show name and category (maybe find images?)
* `IpsumViewer`
    * gets passed the `selected` (only via `update`)
    * if `selected` is `null` displays message to make a selection

## Requirements

* Use Vue CLI to create project (choose "merge" option)
* Move `data.js` to appropriate place in project
* Use single-file vue components

## Rubric

* Project Structure and Organization **1pts**
* Use of VueJS components **3pts**
* Data passing and events **3pts**
* Feature/Functionality correct/works **3pts**
