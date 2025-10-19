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


# Module 2 Video 1: State Schema

Learnings:

I learnt from this video that LangGraph uses typed state schemas to maintain a structured flow of data across all nodes.
I understood the three ways to define a schema in LangGraph: using TypedDict, Dataclass and Pydantic.
Pydantic is the most reliable as it validates the data at runtime and it also prevents invalid values so this helps to confirm that the graph behaves correctly and follows the defined structure.

Changes:

I updated the name Lance to my nickname Shan in all the code cells.
In all the code cells, I replaced the given moods with new moods: happy with wholesome, sad with nervous and mad with unbothered.

Original source code file:
https://github.com/Shantanu2003-alt/ShantanuMishra-langgraph-MAT496/blob/main/SourceCode/state_schema.ipynb

Edited code file:
https://github.com/Shantanu2003-alt/ShantanuMishra-langgraph-MAT496/blob/main/Module2/state_schema%20(1).ipynb

# Module 2 Video 2: State Reducers

Learnings:

I learnt from this video that the reducers decide how updates are made in the state of a graph. 
Instead of replacing old values, they can add or merge the new values safely. 
I also learnt to use custom reducers and message IDs to rewrite or remove specific messages whenever it is needed.

Changes:

I replaced the placeholder 'foo' with 'data' in all the code cells.
I also changed the user name from "Lance" to my nickname "Shan" to make it more personal.
I changed the question from asking about marine biology to asking how AI is used in sports.
I added another human message as a follow up to my question, asking which sport uses AI the most.
Then I changed the message from talking about whales to talking about football to match the topic of AI in sports.

Original source code file:
https://github.com/Shantanu2003-alt/ShantanuMishra-langgraph-MAT496/blob/main/SourceCode/state_reducers.ipynb

Edited code file:
https://github.com/Shantanu2003-alt/ShantanuMishra-langgraph-MAT496/blob/main/Module2/state_reducers%20(1).ipynb

# Module 2 Video 3: Multiple Schemas

Learnings:

Private states help to hide the intermediate steps of nodes when we do not need to show their outputs.
Private states help the nodes to share temporary data without affecting the main graph output.
I also learned how input and output schemas let us control exactly what data enters and leaves the graph.
Overall, multiple schemas give us more control over how the information moves and how it is showed in the workflow.

Changes:

I changed all mentions of Lance to Shan in the node outputs and notes.
I replaced foo and baz with data and temp.
I added print() statements in the nodes to show messages like "Thinking about the question" and "Giving the final answer!".
I updated the output strings to phrases like processing: and "Bye bye, Shan!" and adjusted the notes text a bit.
I changed the input questions in graph.invoke() to more natural sentences like "Hello there, who is Shan?" and hello.

Original source code file:
https://github.com/Shantanu2003-alt/ShantanuMishra-langgraph-MAT496/blob/main/SourceCode/multiple_schemas.ipynb

Edited code file:
https://github.com/Shantanu2003-alt/ShantanuMishra-langgraph-MAT496/blob/main/Module2/multiple_schemas%20(1).ipynb

# Module 2 Video 4: Trim and Filter Messages

Learnings:

I learned how message reducers, filters and trimmers control how much of the chat history is sent to the model each time.
I understood how the reducers get implemented first, then filtering is used to pass only the last message while still showing the full conversation.
Then also I explored trimming, which allows to keep only part of the past context when sending input to the model.
I understood that the main goal is to reduce token usage and get faster responses while keeping the chat flow consistent.

Changes:

I changed the topic from ocean mammals and whales to space exploration and planets.
I replaced the original questions by adding new questions like "Tell me more about black holes", "How is Jupiter?" and "What is the biggest star in the universe?".
I replaced the name Lance to my nickname Shan.
I updated and stored these new space-related messages to keep the conversation consistent.

Original source code file:
https://github.com/Shantanu2003-alt/ShantanuMishra-langgraph-MAT496/blob/main/SourceCode/trim_filter_messages.ipynb

Edited code file:
https://github.com/Shantanu2003-alt/ShantanuMishra-langgraph-MAT496/blob/main/Module2/trim_filter_messages%20(1).ipynb

