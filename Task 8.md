## Task-8 : Introduction to AIML
So far, we have written code which would help launch our chatbot by calling files from the libraries. Now, we need to load those libraries unto our project. For this, we will be using AIML.

## AIML (Artificial Intelligence Markup Language)
AIML is a markup language which is used to create chatbots and conversational agents. It is based on XML which is a markup language that allows you to store data in a shareable manner.

This is a simple structure of an AIML document:
```
<aiml>
  <category>
    <pattern>Hello</pattern>
    <template>Hi there!</template>
  </category>
</aiml>

```
## Understanding AIML structure:
- `<aiml>`: Defines the beginning and end of an AIML document
- `<category>`: Defines a rule or a pattern-response pair for the chatbot
- `<pattern>`: Defines the pattern to match what a user may input to Alicebot
- `<template>`: Defines the response of Alicebot to the user's input

## User Inputs
AIML supports wildcards like * (matches any number of words) and _ (matches a single word). Here is an example:
```
<category>
  <pattern>How * you</pattern>
  <template>I'm doing well, thank you!</template>
</category>
```
In this example, when the user asks a question in that format such as "How are you" or "How is you", the chatbot replies,"I am doing well, thank you!"

## Responses
### Personalized responses:
For creating personalized responses, you can use `<star/>`. This allows the chatbot, to return certain text from the user input. Here is an example:
```
<category>
  <pattern>My name is *</pattern>
  <template>Nice to meet you, <star/></template>
</category>
```

**Console output:**
```
User: My name is Jaden
Chatbot: Nice to meet you, Jaden
```
### Random responses:
You can give the chatbot, an option to pick a response. Here is an example:
```
<category>
  <pattern>Tell me a joke</pattern>
  <template>
    <random>
      <li>Why did the chicken cross the road? To get to the other side!</li>
      <li>What do you call a fish with no eyes? Fsh!</li>
    </random>
  </template>
</category>
```

You have now learnt AIML syntax, let's add this to our project!
