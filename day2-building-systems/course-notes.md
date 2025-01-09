### Large language models 
- A language model is trained via supervised learning to repeatedly predict the next word.
- Two types of LLMs: Base LLM, Instruction Tuned LLM  
  - __Base LLM__: repeatedly predicts next word based on training data  
  - __Instruction Tuned LLM__: start with a Base LLM trained on a lot of data.
    Then, fine-tune the model on a smaller set of examples where the output  
    follows an input example. 
    - To improve the output, collect human ratings on the quality of different LLM outputs  
    - Tune LLM to increase probability that it generates more highly-rated outputs (usling RLHF)  
- Note: LLM predicts next _token_, not word! 
  - Prompting tip: create tokens using delimiters  
  - Different LLMs have different limits on input "context" + output "completion"  
  - gpt3.5-turbo: approximately 4,000 token limit 
  
 
### Process of building an application  

- Tune prompts on a handful of examples  
- Add additional "tricky" examples opportunistically  
- Develop metrics to measure performance on examples  
- Collect randomly sampled set of examples to tune to (development set/ hold-out cross validation set)  
- Collect and use a hold-out test set  

### LLM Evaluation rubric

Compare the factual content of the submitted answer with the expert answer. Ignore any differences in style, grammar, or punctuation.
    The submitted answer may either be a subset or superset of the expert answer, or it may conflict with it. Determine which case applies. Answer the question by selecting one of the following options:
    (A) The submitted answer is a subset of the expert answer and is fully consistent with it.
    (B) The submitted answer is a superset of the expert answer and is fully consistent with it.
    (C) The submitted answer contains all the same details as the expert answer.
    (D) There is a disagreement between the submitted answer and the expert answer.
    (E) The answers differ, but these differences don't matter from the perspective of factuality.
  choice_strings: ABCDE