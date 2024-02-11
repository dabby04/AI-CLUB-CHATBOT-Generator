## Task-7 : Dynamically Determine Resource Path

Here we will learn to configure the chatbot to dynamically locate and use resource files necessary for its operation, such as AIML files. 

What is AIML?
AIML stands for Artificial Intelligence Markup Language. It's a type of XML designed specifically for creating natural language software agents, such as chatbots. AIML files contain patterns and templates that define how a chatbot should respond to user input. Essentially, these files serve as the chatbot's "brain," allowing it to recognize user queries and reply with appropriate responses. The structure of AIML makes it possible to create complex conversations, enabling chatbots to provide more human-like interactions.

### Now moving outside our main method :

1. Create a private static method getResourcesPath() that will return a string representing the path to the resources directory.

2. Create a new File object representing the current directory with new File("."). This line of code makes a new instance of File class that we imported earlier and names is “currDir”. This step is essential as it leverages the application's execution context to dynamically locate its working directory. This is the foundation for finding resource files necessary for operation, such as AIML files, by starting from the current directory the application is running in.
   ```
   File currDir = new File(".");
   ```

4. Create a String variable named path by calling currDir.getAbsolutePath() to get the absolute path of the current directory. This saves the absolute path our currDir file in path
variable in form of string.
   ```
   String path = currDir.getAbsolutePath();
   ```

5. Create a String variable named resourcesPath by appending the relative path segments "src", "main", and "resources" to the adjusted path. Use File.separator in between these segments to ensure the constructed path is valid across different operating systems. This creates a fully qualified path to the directory where the AIML files and other necessary resources are stored, enabling the chatbot to access its knowledge base and function correctly.
   ```
   path = path.substring(0, path.length() - 2);
   String resourcesPath = path + File.separator + "src" + File.separator + "main" + File.separator + "resources";
   ```

6. Print out the path.
  
7. Finally, create a return statement for the getResourcesPath method that returns the constructed resourcesPath. This ensures that any part of your application requiring access to the resources directory can dynamically obtain the correct path, regardless of where the application is deployed or executed.
   ```
   return resourcesPath;
   ```

## Your code should now look something like this :
![Determining source path](/images/10.png)

