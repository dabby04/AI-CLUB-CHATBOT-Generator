## Preparing our bot and creating a task session

The following create statements  describe the process of setting up a chat session with the bot and preparing the bot for interaction by loading its AIML patterns. Each step is critical for ensuring the bot is ready to engage in meaningful conversations with users, leveraging its knowledge base for responsive dialogue.

#### Now inside our try block add : 

1. Create an instance of the Chat class named chatSession using the previously instantiated bot object. This step establishes a new chat session, enabling the bot to interact with users through this session.
   ```
   Chat chatSession = new Chat(bot);
   ```

3. Call the nodeStats() method on the bot's brain to load the AIML patterns into the bot's memory and prepare it for conversation. This operation also prints statistics about the loaded knowledge base, such as the number of categories (rules) loaded, which is helpful for understanding the scope of the bot's conversational abilities.
   ```
   bot.brain.nodeStats();
   ```

5. Initialize a String variable named textLine with an empty string. This variable will later be used to store user input for the chat session, facilitating the interaction between the user and the bot.
   ```
    String textLine = "";
   ```

### Now your code should look something like this:
![Preparing our chatbot](/images/7.png)
   
   
## Onto task 6 -->
