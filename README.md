Output screenshots:
<img width="1137" alt="Снимок экрана 2025-03-06 в 23 58 30" src="https://github.com/user-attachments/assets/59e16933-1e64-4e80-b6dd-b2a8d1f6fc47" />
<img width="1137" alt="Снимок экрана 2025-03-06 в 23 58 52" src="https://github.com/user-attachments/assets/931c7817-c51e-4334-965b-be0ee2e556cd" />

Documentation:
In this assignment, we implement two structural design patterns:

Singleton for managing global configuration settings.

Adapter for integrating a legacy chat service with a new interface.

The goal is to create classes demonstrating these patterns and verify their functionality.

Objective

Implement a ConfigurationManager class that:

Stores configuration settings as key-value pairs.

Ensures only one instance exists throughout the application.

Allows retrieving configuration values by key.

Provides a method to print all configurations for debugging.

Part 1

Step 1: Create the Singleton Class

Create a new file: ConfigurationManager.java

Inside this file, define a class ConfigurationManager.

Declare a private static variable to hold the single instance.

Create a private constructor to prevent direct instantiation.

Implement a static method getInstance() to return the single instance.

Step 2: Store Configuration Settings

Create a HashMap to store key-value settings.

Initialize it with some default configurations inside the constructor.

Add a method getConfig(String key) to fetch a setting by key.

Add a method printAllConfigs() to print all settings.

Step 3: Create a Demo Class

Create a new file: ConfigManagerDemo.java

Inside, get an instance of ConfigurationManager using getInstance().

Retrieve and print specific settings.

Call printAllConfigs() to verify everything is working.


Part 2: Chat Service Adapter 


Step 1: Create a Legacy Chat Service

Create a new file: LegacyChatService.java

Inside, define a class LegacyChatService.

Add a method sendLegacyMessage(String message), which prints messages in the old format.

Step 2: Define a New Chat Interface

Create a new file: ChatService.java

Inside, define an interface ChatService.

Add a method sendMessage(String message), which will be the standard format.

Step 3: Create the Adapter

Create a new file: ChatServiceAdapter.java

Inside, define a class ChatServiceAdapter that implements ChatService.

Add a reference to LegacyChatService.

In sendMessage(), call sendLegacyMessage().

Step 4: Create a Demo Class

Create a new file: ChatAdapterDemo.java

Inside, create an instance of LegacyChatService.

Wrap it inside ChatServiceAdapter.

Call sendMessage("Hello world!").
