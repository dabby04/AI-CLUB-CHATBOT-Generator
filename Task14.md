# Task 14 - Personalizing Responses with AIML "that"

Task 14 focuses on leveraging the "that" tag in AIML to make chatbot conversations more contextually aware and dynamic. By incorporating the "that" tag, you can enable your chatbot to consider its previous response when determining how to reply to the current user input, facilitating a more coherent and natural dialogue flow. Example:

```
<category>
      <pattern>WHAT ABOUT MOVIES</pattern>
      <template>Do you like comedy movies</template>  
   </category>
   
   <category>
      <pattern>YES</pattern>
      <that>Do you like comedy movies</that>
      <template>Nice, I like comedy movies too.</template>
   </category>
   
   <category>
      <pattern>NO</pattern>
      <that>Do you like comedy movies</that>
      <template>Ok! But I like comedy movies.</template>
   </category> 

```
As you can see the last line printed on console by the  chatbot becomes the content in <that> tag


## Onto Task-15 -->
