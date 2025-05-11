# Chatbot_using_Langchain_with_memory


# LangChain Google Gemini Chatbot

This Colab notebook demonstrates a chatbot built using LangChain and Google Gemini.  It showcases several key features of LangChain, including:

* **Google Gemini Integration:** Utilizes the Gemini API for natural language processing.
* **Message History Management:** Implements chat history using `InMemoryChatMessageHistory`, demonstrating how to maintain context across multiple user interactions.
* **Customizable Sessions:** Allows for multiple chat sessions with separate histories.
* **Prompt Templates:**  Uses `ChatPromptTemplate` for structured prompts, enhancing interaction quality.
* **Message Trimming:** Demonstrates message trimming to manage context window limits, ensuring efficient token usage.
* **Runnable Chains:**  Combines components (prompt template, model, and message history) into a streamlined `Runnable` for simplified interaction flow.


## Setup and Dependencies

The notebook installs necessary libraries:

* `langchain_google_genai`
* `langchain`
* `langchain_community`

It also sets environment variables for API keys and LangChain tracing, which are crucial for running the chatbot. **Remember to replace the placeholder API keys with your actual keys.**

## Usage

The chatbot starts with an initial greeting and enters a loop, prompting the user for input until the user types "bye".

The notebook then provides examples of different functionalities:

1. **Basic Interaction:** Demonstrates a simple interaction with the Gemini model.

2. **Message History:** Shows how to use `InMemoryChatMessageHistory` to store and retrieve chat history, thus keeping track of previous interactions within a conversation.

3. **Multiple Sessions:** Highlights how to create and manage multiple independent chat sessions, each with its own history.

4. **Prompt Templates:** Explains the use of prompt templates for formatting messages to the Gemini model, leading to more coherent responses.

5. **Message Trimming:**  Demonstrates how to limit the number of tokens used in the context window using `trim_messages`. This is important to avoid exceeding token limits.

6. **Runnable Chains with Memory:** Shows how to create a runnable chain that includes the message history, enabling the model to use the current chat session data.


## API Keys and Environment Variables

Ensure that you have set the following environment variables before running the notebook:

*   `GEMINI_API_KEY`: Your Google Gemini API key.
*   `LANGCHAIN_API_KEY`: Your LangChain API key.
*   `LANGCHAIN_TRACING_V2`, `LANGCHAIN_PROJECT`, `LANGCHAIN_END_POINT`: Required for LangChain tracing.
*   `TAVILY_API_KEY`:  Your Tavily API key (if used).
*   `HUGGINGFACEHUB_API_TOKEN`: Your Hugging Face API key (if used).

**Important:**  Replace the placeholder values with your actual API keys.

## Running the Notebook

1.  Open the notebook in Google Colab.
2.  Replace the placeholder API keys with your own.
3.  Run all the cells.

You'll be able to interact with the chatbot and observe how the different LangChain features work.


## Contributing

Feel free to enhance the code, add more functionalities, or improve the documentation.
