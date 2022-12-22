# Contact book

Performed refactoring of the Contact Book application code. Removed the code
responsible for storing and reading contacts from the local storage, and added
communication with the backend for storing contacts.

## Backend

Created my own personal backend for development with the UI service
[mockapi.io](https://mockapi.io/projects/638386a41ada9475c80213da).

## State Form

Added the load and error indicator handling to the Redux state. For do this, I
have changed the state form.

`{ contacts: { items: [], isLoading: false, error: null }, filter: "" }`

## Operations

Used createAsyncThunk to declare asynchronous action generators and make HTTP
requests. I have do processing of the actions and change data in Redux state
with createSlice.

Declared the following operations:

1. fetchContacts - get an array of contacts (GET method) by GET request. The
   basic type of action "contacts/fetchAll".
2. addContact - add contact (POST method). Basic type of action
   "contacts/addContact".
3. deleteContact - deletes a contact (DELETE method). Basic type of action
   "contacts/deleteContact".
