# ShantanuMishra-langgraph-MAT496

This repository is for my video-by-video progress of different modules of the Introduction to LangGraph course by LangChain Academy.

Course: https://academy.langchain.com/courses/intro-to-langgraph

I have written my learnings and my work of each video of the Modules below:

# Module 1 video 1: Motivation

Learnings:

So from this video, I learned that LangGraph is an open-source framework which helps to design custom agent workflows using states, nodes and edges for better control. 
LangGraph is an MIT-licensed open-source library and is free to use. LangGraph does not require LangChain but works well with it to build complex and stateful agents. 
I got to learn about the basic LangGraph components- about what the states, nodes and edges do. 
LangChain is for quick model interactions but LangGraph gives deeper control and flexibility. 
I also learned how LangGraph helps to build reliable systems that involve humans and to handle long taks .

Changes:

This lesson was a theoretical explanation of the topic and did not have any source code to make changes to.

# Module 1 video 2: Simple Graph

Learnings:

I learned how to define the State of a graph using 'TypedDict' to share information between nodes and edges. 
I understood that nodes are python functions that update the state and then the edges connect them, either directly or based on some conditions. 
I also learned how to build a StateGraph, how to add START and END nodes and how to visualize everything. 
Finally, I learned how to run the graph using 'invoke' that executes each node in order and returns the final updated state.

Changes:

I changed the code by adding another node. So, this new node here is the "nervous" node.
Then, I changed the probability to 1/3 because of the added node.

Original source code file:
https://github.com/Shantanu2003-alt/ShantanuMishra-langgraph-MAT496/blob/main/SourceCode/simple_graph.ipynb

Edited code file:
https://github.com/Shantanu2003-alt/ShantanuMishra-langgraph-MAT496/blob/main/Module1/simple_graph%20(1).ipynb

<img width="271" height="234" alt="image" src="https://github.com/user-attachments/assets/474236bf-bc4b-43fa-ba07-43dcee6f2953" />

This is how my graph is looking.

<img width="440" height="99" alt="image" src="https://github.com/user-attachments/assets/3024a70b-8722-45fc-b68a-7d19a5105af0" />

This is my output.

# Module 1 Video 3: 

Learnings:

So this video taught me about how to set up and use the LangGraph Studio to easily build and test graphs. 
I also learned how LangSmith helps to track each step in the workflow for our better understanding.

Work:

So with the help of this video, I basically made a new simple graph with extra node using the LangSmith studio.

<img width="273" height="344" alt="image" src="https://github.com/user-attachments/assets/0db0c18f-1d31-44c8-ac6f-44c48840156e" />

This is how my graph made using the LangSmith Studio is looking.

# Module 1 Video 4: Chain

Learnings:

I learned how to build a chain in LangGraph by combining chat messages, chat models and tools within a single workflow. 
I understood how messages store the full conversation and how tools let the model interact with external systems. 
I also learned how to use reducers like 'add_messages' to keep appending the new messages during execution. 

Changes:

I executed the graph by asking an extra question, "Where is Lamine Yamal from?" as input and then I printed all the messages in the conversation to view the full chat flow and responses.
Then I ran the graph with a human message and tested the tool by asking the model to add 98 and 107 and printed all the messages to see how the model processed the request and gave the result.

Original source code file:
https://github.com/Shantanu2003-alt/ShantanuMishra-langgraph-MAT496/blob/main/SourceCode/chain.ipynb

Edited code file:
https://github.com/Shantanu2003-alt/ShantanuMishra-langgraph-MAT496/blob/main/Module1/chain%20(2).ipynb

# Module 1 Video 5: Router

Learnings:

This video taught me how a chat model can decide its response based on the input and it can either answer directly or call a tool. 
I learned how to use messages to keep track of the conversation and bind tools so the model knows when to use them. 
I understood how to add ToolNodes and conditional edges to guide the flow based on the model’s output. 
I saw how different tools and paths can help handle different kinds of questions more effectively. I also learnt that the LangGraph Studio is currently not supported on Google Colab.

Changes:

Changed the multiplication question with different values and tested the tool.
I also asked an extra question about "Who won the fifa world cup in 2022" to test further.

Original source code file:
https://github.com/Shantanu2003-alt/ShantanuMishra-langgraph-MAT496/blob/main/SourceCode/router.ipynb

Edited code file:
https://github.com/Shantanu2003-alt/ShantanuMishra-langgraph-MAT496/blob/main/Module1/router%20(1).ipynb

# Module 1 Video 6: Agent

Learnings:

I learned how to build a ReAct agent where the chat model can decide to call a tool or respond directly based on user input. 
How to use conditional edges to route the flow between the Assistant and Tools nodes. 
Also learned how to create a loop so that the model can repeatedly call tools and give reason about their outputs before giving a final response. 
Finally, I saw how this general architecture can handle many types of tools and queries efficiently.

Changes:

I tested the tool by changing the question with bigger values to calculate and also added subtraction 
Made the question: "Add 19 and 41. Multiply the output by 2. Subtract the output by 5. Divide the output by 5"
Then, I asked another question about "How many kilometers are in 10 miles?" to test the tool in a different way.

Original source code file:
https://github.com/Shantanu2003-alt/ShantanuMishra-langgraph-MAT496/blob/main/SourceCode/agent.ipynb

Edited code file:
https://github.com/Shantanu2003-alt/ShantanuMishra-langgraph-MAT496/blob/main/Module1/agent%20(1).ipynb

# Module 1 Video 7: Agent with Memory

Learnings:

This video taught me how to add memory to an agent using a 'thread_id'. It helps the model remember past actions and continue from previous steps.
I learned how checkpoints store each step of the conversation.
In LangGraph dev, there is an in-built persistence layer that intergrates the API key and gives memory to the agent by default.

Changes:

Created a new thread and added new steps to the process to see if the model can keep track of memory over time and perform different calculations.
The final operation referenced the result from the first ever operation and the result the model gave used it correctly. 

Original source code file:
https://github.com/Shantanu2003-alt/ShantanuMishra-langgraph-MAT496/blob/main/SourceCode/agent_memory.ipynb

Edited code file:
https://github.com/Shantanu2003-alt/ShantanuMishra-langgraph-MAT496/blob/main/Module1/agent_memory%20(1).ipynb

# Module 1 Video 8: Intro to Deployment

Learnings:

I learned how to create and deploy LangGraph agents that can think, remember and respond smartly.
I also learned how to use LangGraph Studio and Cloud to run and manage my agents easily.

Changes:

I could not deploy the project because deployment is only available for users on the LangSmith Plus (paid) plan.
