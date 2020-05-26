# String parser challenge

The aim is to create a string parser which replaces one or more pieces of placeholder text with data from an object map.

Important: Make sure you also view our [coding challenge guidelines](README.md).

## The brief

Your parser will take a string (example below), and replace one or more pieces of placeholder text with data held in an object (example below). It should give the expected output shown below.

You can assume that the example object's top-level keys will always be a hexadecimal key of length 8 characters.

If there is no matching object for a placeholder, you should insert the string '\<nothing\>'.
  
## Example string

```
This is a string with {{ ab49fd20.key_1 }}, including {{ 9822df87.another_key }} and
also {{ ab49fd20.key_2 }}.
```

## Example object

```
{
  'ab49fd20': {
    key_1: 'some data'
  },
  '9822df87': {
    another_key: 'big data',
    yet_another_key: 'small data'
  }
}
```

## Expected output

```
This is a string with some data, including big data and also <nothing>.
```

## The technical requirements

- We will specify the language/runtime to write the code in.
- You should include tests, written in whatever testing frameworks/libraries you prefer.

## Skills tested

- Language understanding
- General coding skills
- Testing