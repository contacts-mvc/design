# Contacts MVC Design

> Let's implement a contacts app!

## Goal
Goal of Contacts MVC is to compare different implementations of the same web
applications using different technology stacks. It's inspired by
[TodoMVC](http://todomvc.com/) and it is trying to push the envelope further
and compare a more complex application that has more features than a simple Todo
Application.

## Design
The Contact MVC app is a simple contact management app which allows user to find,
edit and add new contacts to their contacts book.

There are three main sections
* List of contacts
* Details of selected contact
* Search box

Compared to TodoMVC this app has following extra features:
* routing
* search
* backend

## CSS
CSS of the application is provided in
[`contacts-mvc-css`](https://www.npmjs.com/package/contacts-mvc-css) package.

## HTML
A [reference HTML structure](#TODO) of this app is provided in
[`contacts-mvc-css`](https://github.com/contacts-mvc/contacts-mvc-css) GitHub repository.

All implementations should generate the same HTML structure so that the common CSS
functions properly.

## Routing
Contacts MVC does not use URL fragment for routing. all of routes should be in path name
section of the URL.

#### Routing table

| Route             | View                                                                                                           |
|-------------------|----------------------------------------------------------------------------------------------------------------|
| `/`               | List of contacts with no contact selected in details view                                                      |
| `/{id}`           | Contact with associated `id` is selected in list and it's details are show in the details view                 |
| `/new`            | No contact is selected in list and an empty form for creating a new contact is rendered in details view        |
| `/{id}/edit`      | Contact with associated `id` is selected in list and it's details are rendered in editing form in details view |
| `/search/{query}` | List of contacts only shows contacts that match the query and first result is selected.                        |

## Backend
TODO: A standard RESTful backend server is provided for all implementations.

The backend API should run in the same port under `/api` base path. The backend
server comes with a standard preset data.

## Testing
TODO: Automated end-to-end testing using WebDriver is provided to run against any implementation.

## Dependencies