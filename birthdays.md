# Birthdays app challenge

The aim is to create a small app that allows you to keep track of birthdays.

When you open the app, you'll be able to see whose birthdays are today, or coming up in the next 2 weeks. It will also tell you how old they are (or will be).

Important: Make sure you also view our [coding challenge guidelines](README.md).

## Main features

- A single UI page that shows you today's birthdays, upcoming birthdays (next 2 weeks), and a list view of all the people whose birthdays you're keeping track of.
- For today's birthdays and upcoming, show how old that person is (or will be).
- The list should show the person's name and date of birth.
- The ability to add a new birthday to the list, requiring the person's name and date of birth (add some validation).
- It should also be possible to delete birthdays from the app.

## The technical requirements

- The UI should be a web client or mobile app. The person setting the challenge will specify the expected language/runtime.
- We will provide an API for you to build against, see below.
- It's fine to bring in a UI components library or to use native components. We are looking for good usability, visual hierarchy, focus, and layout, but not a polished design.
- There should be tests for the client, use whatever testing frameworks/libraries you prefer.
- You don't need to provide thorough test coverage, but cover the basics and show what your approach would be.

## API

You can choose to use either of the following APIs for this challenge.

### GraphQL

https://birthday-api.hasura.app/v1/graphql can be used a working GraphQL API to use as a backend for the app. This allows for birthdays to be listed, created, and deleted.

The data on this API is reset daily.

You can use the following queries and mutations:

#### List

```graphql
query {
  person {
    id
    name
    date_of_birth
  }
}
```

#### Add person

```graphql
mutation {
  insert_person_one(
    object: { date_of_birth: "1925-03-31", name: "Peter Paul" }
  ) {
    name
    date_of_birth
  }
}
```

#### Delete person

```graphql
mutation {
  delete_person(where: { id: { _eq: "< user uuid >" } }) {
    affected_rows
  }
}
```

### REST

https://my-json-server.typicode.com/teamchalkboard/chalkboard-coding-challenges can be used a working REST API to use as a backend for the app. This allows for birthdays to be listed, created, and deleted.

All HTTP methods are supported. You can use http or https for your requests.

GET /users
GET /users/1
POST /users
PUT /users/1
PATCH /users/1
DELETE /users/1

_PLEASE NOTE_: Changes are faked and aren't persisted, but request should behave as expected when requests are made.

## Time limit

Please spend no more than 3 hours on this challenge.

## Skills tested

- Client side development practices
- Designing a simple UI
- Testing
