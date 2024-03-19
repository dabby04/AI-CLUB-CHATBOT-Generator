# Task 11 - Adding Custom Patterns Using AIML

So far, we have learned how to make our chatbot using Alicebot and AIML. In this Task we will focus on making our own basic aiml file to customize the bot’s responses and add more intelligence to its interactions.

As we learned in Task 8 basic structure of an AIML file looks like:
```
<?xml version="1.0" encoding="UTF-8"?>
<aiml>
  <category>
    <pattern>Hello</pattern>
    <template>Hi there!</template>
  </category>
</aiml>
```
where
- `<aiml>`: Defines the beginning and end of an AIML document
- `<category>`: Defines a pattern-response pair for the chatbot
- `<pattern>`: Defines the question to match what a user may input to Alicebot
- `<template>`: Defines the response of Alicebot to the user's input


Using this, We can make our own .aiml files and add them to the Chatbot

## Steps
1) Follw this path in your project `src\main\resources\bots\super/aiml` and create a new file called basic.aiml
![](/images/task11_img1.png)
![](/images/task11_img2.png)
2) Write this basic syntax into our aiml file
```
<?xml version="1.0" encoding="UTF-8"?>
<aiml>


</aiml>

```
3) We can now create our own categories with basic questions and responses
```
<?xml version="1.0" encoding="UTF-8"?>
<aiml>

    <category>
        <pattern>how many campuses does UBC have</pattern>
        <template>UBC currently has 2 campuses- Vancouver and Kelowna</template>
    </category>

    <category>
        <pattern>Is there an AI Club </pattern>
        <template>Yes there is an AI club on the Kelowna campus</template>
    </category>
</aiml>

```
4) After you are done with creating this AIML file, Make sure to run the AddAiml class once before running our App class. This will make sure our Chatbot is updated with the newly added AIML file
5) Note- You can find the AddAiml.java file along with the tasks on Github.Please download the file and copy it to your project before proceeding. It should be in the same parent package as our App.java file


## Onto Task-12 -->
