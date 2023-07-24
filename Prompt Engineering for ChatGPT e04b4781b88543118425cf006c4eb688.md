# Prompt Engineering for ChatGPT

# Week 1

## What are Large Language Models?

A large Language model ( LLM ) predicts the next word from the words we are given until it thinks it’s enough.

- It takes **context.**
- They all have inherent **randomness.**
- We need to provide **additional information** to get a better result.
- Remember that we will have **different answers** every time

# Week 2

- Prompt has **memory**
- Sometimes we need to **remind the model** what to do.
- Make the model **ask a quotation** so you can give the information.
- You can give the **model new and updated information as a prompt.**

### TIME

- **From now on** ( all the following prompts will do  what we have told )

### [Intuition Behind Prompts](https://www.coursera.org/learn/prompt-engineering/lecture/ZLlRW/intuition-behind-prompts)

- LLM uses **patterns** to answer questions [ Strong pattern = better answer ]
- Use **detailed words** / ~~**not use generic words**~~ to get the best answers.
- We can also provide the structure to a prompt.
- Prompt  for structure
    
    Title: <Title of the article>
    
    Author : <Author>
    
    Summary : <Summary>
    

---

### [**Everyone Can Program with Prompts**](https://www.coursera.org/learn/prompt-engineering/lecture/it7m2/everyone-can-program-with-prompts)

We can program how the output can be presented. Like CSV, we can also give additional information on what output to present.

- **CSV [ Example 1 ]**
    
    Whatever you generate output turn it into a comma separate value list. 
    

---

### **[Prompt Patterns](https://www.coursera.org/learn/prompt-engineering/lecture/XQJQf/prompt-patterns)**

### [The Persona Pattern](https://www.coursera.org/learn/prompt-engineering/lecture/MgJp2/the-persona-pattern)

`ACT AS`     

The persona you give it is really important. FI you give a positive one it will be a positive one and vice versa. 

Act as a sceptic that is well-versed in <**Persona>** and provide output that  they will 

- **Examples**
    1. **Act as a**  sceptic that is **well-versed in computer science** and provides output as they will 
    2. **Act as a Linux terminal f**or a computer that has been hacked. I will type in Linux terminal commands, and you will respond with the output that the Linux terminal would produce.

# Format of the Persona Pattern

To use this pattern, your prompt should make the following fundamental contextual statements:

- Act as Persona X
- Perform task Y

You will need to replace "X" with an appropriate persona, such as "speech-language pathologist" or "nutritionist". You will then need to specify a task for the persona to perform.

- Examples
    - Act as a speech-language pathologist. Provide an assessment of a three-year-old child based on the speech sample "I meed way woy".
    - Act as a computer that has been the victim of a cyber attack. Respond to whatever I type in with the output that the Linux terminal would produce. Ask me for the first command.
    - Act as a the lamb from the Mary had a little lamb nursery rhyme. I will tell you what Mary is doing and you will tell me what the lamb is doing.
    - Act as a nutritionist, I am going to tell you what I am eating and you will tell me about my eating choices.
    - Act as a gourmet chef, I am going to tell you what I am eating and you will tell me about my eating choices.
    

[Reference link](https://arxiv.org/abs/2302.11382) 

---

### **[Introducing New Information to the Large Language Model](https://www.coursera.org/learn/prompt-engineering/lecture/yfI9t/introducing-new-information-to-the-large-language-model)**

### **[Prompt Size Limitations](https://www.coursera.org/learn/prompt-engineering/lecture/b7xDB/prompt-size-limitations)**

- **Create a fitter** on what information we are providing for the given task to be done.
- **Summarize the huge information** so that we can give more information.

### **[Prompts are a Tool for Repeated Use](https://www.coursera.org/learn/prompt-engineering/lecture/VzL6f/prompts-are-a-tool-for-repeated-use)**

- We should go through an **entire conversation** with LLM to get the result we want
- Make a **conversation on what to do.** If we hit a roadblock, we can give other prompts.
- Give feedback on the response and move from the roadblocks.

### **[Root Prompts](https://www.coursera.org/learn/prompt-engineering/lecture/COsyW/root-prompts)**

It is like a seed which will provide what will the future outputs be. They are always some root prompts which are hidden from the user.

# Week 3

### **[Question Refinement Pattern](https://www.coursera.org/learn/prompt-engineering/lecture/qehSB/question-refinement-pattern)**

By using this prompt, we can get better answers: 

<aside>
🛠 **“Whenever I ask a question, suggest a better question and ask me if I would like to use it instead.”**

</aside>

### **[Cognitive Verifier Pattern](https://www.coursera.org/learn/prompt-engineering/lecture/CDIpT/cognitive-verifier-pattern)**

To use the Cognitive Verifier Pattern, your prompt should make the following fundamental contextual statements:

- When you are asked a question, follow these rules.
- Generate a number of additional questions that would help more accurately answer the question.
- Combine the answers to the individual questions to produce the final answer to the overall question.
- **Examples**
    - When you are asked a question, follow these rules. Generate a number of additional questions that would help you more accurately answer the question. Combine the answers to the individual questions to produce the final answer to the overall question.
    
    **Tailored Examples:**
    
    - When you are asked to create a recipe, follow these rules. Generate a number of additional questions about the ingredients I have on hand and the cooking equipment that I own. Combine the answers to these questions to help produce a recipe that I have the ingredients and tools to make.
    - When you are asked to plan a trip, follow these rules. Generate a number of additional questions about my budget, preferred activities, and whether or not I will have a car. Combine the answers to these questions to better plan my itinerary.

### **[Audience Persona Pattern](https://www.coursera.org/learn/prompt-engineering/lecture/nH9vM/audience-persona-pattern)**

To use this pattern, your prompt should make the following fundamental contextual statements:

- **Explain X to me.**
- **Assume that I am Persona Y.**

*You will need to replace "Y" with an appropriate persona, such as "have limited background in computer science" or "a healthcare expert". You will then need to specify the topic X that should be explained.*

- **Examples**
    - Explain how the supply chains for US grocery stores work to me. Assume that I am Ghengis Khan.
    - Explain large language models to me. Assume that I am a bird.
    

### **[Flipped Interaction Pattern](https://www.coursera.org/learn/prompt-engineering/lecture/t3im4/flipped-interaction-pattern)**

> Ask LLM to ask questions + to have a goal in mind
> 

To use this pattern, your prompt should make the following fundamental contextual statements:

- I **would like you to ask me questions to achieve X**
- **You should ask questions until condition Y is met or to achieve this goal (alternatively, forever)**
- (Optional) ask me the questions one at a time, two at a time, ask me the first question, etc.

You will need to replace "X" with an appropriate goal, such as "creating a meal plan" or "creating variations of my marketing materials." You should specify when to stop asking questions with Y. Examples are "until you have sufficient information about my audience and goals" or "until you know what I like to eat and my caloric targets."

- **Examples:**
    - I would like you to ask me questions to help me create variations of my marketing materials. You should ask questions until you have sufficient information about my current draft messages, audience, and goals. Ask me the first question.
    - I would like you to ask me questions to help me diagnose a problem with my Internet. Ask me questions until you have enough information to identify the two most likely causes. Ask me one question at a time. Ask me the first question.

# Week 4

### **[Writing Effective Few-Shot Examples](https://www.coursera.org/learn/prompt-engineering/lecture/reRe6/writing-effective-few-shot-examples)**

The input should give additional context and should be meaningful.

### **[Few-shot Examples](https://www.coursera.org/learn/prompt-engineering/lecture/SRJTi/few-shot-examples)**

In **Few-shot Examples,** we give the AI a few example outputs on how the answer should be.

- **Explanation**
    
    **Input :** 
    
    **Output : 
    Give the format for r output and input** 
    

### **[Few-shot Examples for Actions](https://www.coursera.org/learn/prompt-engineering/lecture/U4In0/few-shot-examples-for-actions)**

We can explain the situation with examples, and  we should give the action 

- **Explanation**
    
    **Situation : 
    Action :**
    

### **[Few-Shot Examples with Intermediate Steps](https://www.coursera.org/learn/prompt-engineering/lecture/3s96Q/few-shot-examples-with-intermediate-steps)**

### **[Chain of Thought Prompting](https://www.coursera.org/learn/prompt-engineering/lecture/bK1RY/chain-of-thought-prompting)**

If we give proper examples with reasoning and answer, then LLM will also do the same. 

[Click here for more](https://arxiv.org/abs/2201.11903).

### **[ReAct Prompting](https://www.coursera.org/learn/prompt-engineering/lecture/sDQxD/react-prompting)**

We can give formatting examples on what to do and like search and etc. and it can do that 

[***more***](https://arxiv.org/abs/2210.03629)