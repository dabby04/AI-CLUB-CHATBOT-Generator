## Add the following imports to your project
 1. import java.io.File;
 2. import org.alicebot.ab.Bot;
 3. import org.alicebot.ab.Chat;
 4. import org.alicebot.ab.MagicBooleans;
 5. import org.alicebot.ab.MagicStrings;
 6. import org.alicebot.ab.utils.IOUtils;



### What each import does : 
#### 1. import java.io.File;
This import statement includes the File class from the Java standard library's java.io (input/output) package. The File class is used to represent file and directory pathnames in a manner that is independent of the underlying operating system. It provides methods to inspect, delete, and modify files and directories. 

#### 2.import org.alicebot.ab.Bot;
This imports the Bot class from the Program AB library, a Java implementation of the AIML 2.0 (Artificial Intelligence Markup Language) specification. The Bot class represents an artificial intelligence bot, which can be configured with specific behaviors, responses, and knowledge bases loaded from AIML files. It acts as the core component handling the conversation logic.

#### 3.import org.alicebot.ab.Chat;
This import statement brings in the Chat class from the Program AB library. The Chat class is responsible for managing a conversation session with a user. It keeps track of the chat state, including the history and context of the conversation, allowing the bot to provide coherent responses.

#### 4.import org.alicebot.ab.MagicBooleans;
This imports the MagicBooleans class from Program AB. This class contains static boolean variables that control various debugging and configuration flags for the bot's operation. Adjusting these booleans can affect how the bot processes input, generates output, and logs information.

#### 5.import org.alicebot.ab.MagicStrings;
This includes the MagicStrings class from Program AB. Similar to MagicBooleans, MagicStrings contains static string variables that are used throughout the bot's operation for configuration and default values. These strings can include paths to resources, default responses, and other critical strings that influence the bot's behavior.

#### 6.import org.alicebot.ab.utils.IOUtils;
This import statement brings in the IOUtils class from Program AB, providing utility functions related to input/output operations. This can include reading from or writing to files, converting streams, and other common IO tasks that are necessary for managing the bot's resources and interactions.

