# Task 13 - Creating Wildcard Responses 

In this Task, we will be using wildcards in AIML to enable the chatbot in handling a wider range of user inputs with a single pattern.

 Wildcards allow us to capture and respond to a broad variety of user inputs, making the chatbot capable of understanding and responding to questions or statements that follow a similar structure but contain different specifics.

 AIML supports wildcards like * (matches any number of words) and _ (matches a single word). Example:
 ```
  <category>
    <pattern>TELL ME ABOUT EVENTS IN *</pattern>
    <template>
        While I don't have real-time data, checking online resources like event listings or local news sites for <star/> could be really helpful.
    </template>
</category>
 ```
We can also use multiple wildcards in a single pattern. Example:
 ```
<category>
        <pattern>do you know * about *</pattern>
        <template>
            I know a bit about <star index="2"/>, especially when it comes to <star index="1"/>. Can I help you with any specific information on <star index="2"/>?
        </template>
    </category>
 ```


## Onto Task-14 -->
