## Task-6 : Processing input and generating responses

The following steps collectively create a functional and interactive chat environment, where the user can freely converse with the chatbot, receiving immediate and intelligent responses based on the chatbot's programming and knowledge base.

### Inside the try block :
* Add a while loop and set it to run until its true.

![Processing input and generating responses](/images/9.png)


### Inside the while loop :
1. Create a prompt in the console by displaying "Human : ". This sets the stage for an interactive session, signaling to the user that the chatbot is ready to receive their message. It's a crucial step for establishing a clear communication line between the user and the chatbot.
   ```
   System.out.print("Human : ");
   ```

3. Create a mechanism to capture the user's input by using IOUtils.readInputTextLine(). This command waits for the user to type their message and press enter, capturing the input in the textLine variable. It ensures the bot can process real user queries, making the interaction genuinely responsive.
   ```
   textLine = IOUtils.readInputTextLine();
   ```

5. Create a check for empty or null inputs. If the user's input is either not provided or is an empty string, default it to MagicStrings.null_input. This ensures that every input has a value, maintaining a smooth flow in the conversation even when the user's input might not be directly usable.
   ```
   if ((textLine == null) || (textLine.length() < 1))
	textLine = MagicStrings.null_input;
   ```

7. Create a way for users to exit the chat session gracefully by checking for specific commands. If the user types "q", execute System.exit(0) to terminate the program. If the user types "wq", first perform any necessary finalization with bot.writeQuit(), then exit. This provides an intuitive method for users to end the conversation when desired.
   ```
   if (textLine.equals("q")) {
	System.exit(0);
				}
   else if (textLine.equals("wq")) {
	bot.writeQuit();
	System.exit(0);
				}
   ```

9. Create the bot's response to user input. Take the user's text, process it through the chatbot's AI logic with chatSession.multisentenceRespond(request), and generate a response. Display this response in the console, prefixed by "Bot : ", to indicate that the chatbot is speaking. This completes the cycle of interaction, making the chat experience engaging by providing thoughtful and relevant responses to the user's queries.
```
else {
     String request = textLine;
     String response = chatSession.multisentenceRespond(request);
     System.out.println("Bot : " + response);
				}
```
### Your code should now look something like this :

![Processing input and generating responses](/images/8.png)

## Onto task 7 -->
