# Birthdays app challenge

The aim is to create a small app that allows you to keep track of birthdays.

When you open the app, you'll be able to see a list of peoples birthdays in order. You will also be able to view a person and it will also tell you how old they are (or will be).

Important: Make sure you also view our [coding challenge guidelines](README.md).

## Main features

- A single UI page that shows a list view of all the people whose birthdays you're keeping track of.
- A page that shows a single person's name, date of birth and current age in years.

## The technical requirements

- The UI should be a web client or mobile app. The person setting the challenge will specify the expected language/runtime.
- We will provide an API for you to build against, see below.
- It's fine to bring in a UI components library or to use native components. We are looking for good usability, visual hierarchy, focus, and layout, but not a polished design.
- There should be tests for the client, use whatever testing frameworks/libraries you prefer.
- You don't need to provide thorough test coverage, but cover the basics and show what your approach would be.

## API

You can choose to use either of the following APIs for this challenge.

### REST

https://randomuser.me/api/?results=1000&seed=chalkboard&inc=name,dob can be used a working REST API to use as a backend for the app. You must use https for your requests.

### GraphQL

https://birthday-api.hasura.app/v1/graphql can be used a working GraphQL API to use as a backend for the app. This allows for birthdays to be listed.

The data on this API is reset daily.

You can use the following queries:

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

## Design

A figma design can be found here:
https://www.figma.com/file/HL6gSMUiedhVQhJSUHx4Rt/Birthdays-Challenge?node-id=0%3A1

PNGs for this design can also be found in the `designs` directory.

## Time limit

Please spend no more than 3 hours on this challenge.

## Skills tested

- Client side development practices
- Implementing a simple UI design
- Testing
