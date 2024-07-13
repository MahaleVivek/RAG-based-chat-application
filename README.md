# RAG-based-chat-application

**Challenge: Python + Gen-AI**

**Tech Challenge: RAG-based Chat Application**

## Objective
Develop a chat application using Jupyter Notebook and Retrieval-Augmented Generation (RAG) with OpenAI's GPT-4o model or any other OpenAI model. The application will utilize a predefined conversation history stored in an array. Implement RAG using Pinecone to fetch relevant context.

## Requirements
- Use OpenAI's GPT-4o model or any other OpenAI model for text generation.
- Use Pinecone Serverless Spec.
- Implement embedding-based storage of the last 20 chat history entries into Pinecone.
- Implement RAG to fetch relevant past messages from Pinecone.
- Ensure the Final Test Prompt (including context) + Final Test Prompt Response together do not exceed 225 tokens.

## Instructions
1. **Set up the environment:**
   - Install necessary libraries: OpenAI, Pinecone.
   - Example: `pip install openai pinecone-client`
   - Ensure all installs are only in cell 1.
   - Define any imports in the 1st cell.

2. **Define the conversation history:**
   - Store the conversation history in an array with each message approximately 20 tokens long and numbered.

3. **Functions to implement:**
   - **Add Embeddings to Pinecone:** Encode each message in the history and upsert into the Pinecone index.
   - **Retrieve Relevant History:** Query Pinecone to retrieve relevant messages based on encoded queries.
   - **Prepare Prompt:** Combine retrieved messages with the test prompt, ensuring token limits are respected.
   - **Test Final Prompt:** Generate the final test prompt, print referred context, and validate response relevance manually.

4. **Security Note:**
   - Replace placeholder API keys (`OPENAI_API_KEY`, `PINECONE_API_KEY`, etc.) with actual keys securely.

## Final Validation Instructions
- Ensure the Final Test Prompt references the correct historical messages contextually.
- Manually check if the Final Test Prompt Response correctly references the past context.
- Only valid responses should pass validation.
