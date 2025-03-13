# Functions, Tools and Agents with LangChain  

## Outline  
- OpenAI function calling  
- LangChain Expression Language (LCEL)  
- OpenAI function calling in LangChain  
- Tagging and extraction using OpenAI function calling  
- Tools and Routing  
- Conversational Agent  

## LangChain Expression Language  
- Defines:  
    - Allowed set of input types  
    - Required methods  
    - Allowed set of Output types 
- Composition can use Linux pipe syntax  
- Interface: invoke, stream, batch
- Runnables support: 
  - async, batch, streaming support  
  - fallbacks  
  - parallelism  
  - logging is built in  

## OpenAI Function Calling in LangChain  

- Pydantic  
  - data validation library for python  
  - provides built-in methods to serialize/ deserialize models to/from JSON, dictionaries,etc  
  - LangChain leverages Pydantic to create JSON Scheme describing functions  

## Tagging and Extraction using OpenAI functions  

- Allows for generation of strutured responses 
- Extract specific entities from the text  

## Tools and routing  

- FUnctions and services an LLM can utilize to extend its capabilities are named "tools" in LangChain  
- e.g. search tools, math tools, sql tools  


## Conversational Agent  

Agent Basics  
- Agents  
  - Are a combination of LLMs and code  
  - LLMs reason about what steps to take and call for actions  
- Agent loop  
  - Choose a tool to use  
  - Observe the output of the tool  
  - Repeat until a stopping criteria is met  
- Stopping conditions could be  
  - LLM determined  
  - Hardcoded rules  