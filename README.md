# ShantanuMishra-langgraph-MAT496
This repository is for my video-by-video progress of different modules of the Introduction to LangGraph course by LangChain Academy. 
I have written my learnings and my work of each video of the Modules below:

# Module 1 video 1: Motivation
Learnings:

So from this video, I learned that LangGraph is an open-source orchestration framework which helps to design custom agent workflows using states, nodes and edges for better control and reliability. 
LangGraph is an MIT-licensed open-source library and is free to use. LangGraph does not require LangChain but works well with it to build complex and stateful agents. 
I got to learn about the basic LangGraph components- about what the states, nodes and edges do.
LangChain is for quick model interactions but LangGraph gives deeper control and flexibility. 
I also learned how LangGraph enables developers to create reliable human-in-the-loop systems with durable and long-running task execution.

Changes:

This lesson was a theoretical explanation of the topic and did not have any source code to make changes to.

# Module 1 video 2: Simple Graph

Learnings:

I learned how to define the State of a graph using 'TypedDict' to share information between nodes and edges. 
I understood that nodes are Python functions that update the state and edges connect them, either directly or based on conditions. 
Also learned how to build a StateGraph, add START and END nodes, compile it and visualize it. 
Finally, I learned how to run the graph using 'invoke' that executes each node in order and returns the final updated state.

Changes:

I changed the code by adding another node. So, this new node here is the "nervous" node.
Then, I changed the probability to 1/3 because of the added node.

Original source code file:
https://github.com/Shantanu2003-alt/ShantanuMishra-langgraph-MAT496/blob/main/SourceCode/simple_graph.ipynb

Edited code file:
https://github.com/Shantanu2003-alt/ShantanuMishra-langgraph-MAT496/blob/main/Module1/simple_graph%20(1).ipynb

<img width="271" height="234" alt="image" src="https://github.com/user-attachments/assets/474236bf-bc4b-43fa-ba07-43dcee6f2953" />

This is how my graph is looking

<img width="440" height="99" alt="image" src="https://github.com/user-attachments/assets/3024a70b-8722-45fc-b68a-7d19a5105af0" />

This is my output.


