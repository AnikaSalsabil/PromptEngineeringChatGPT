# Prompt Engineering ChatGPT for Developers- Course from DeepLearning.AI
2 types of LLMs:
1. Base LLM: Predicts the next word, based on text training data
2. Instruction-tuned LLM: Tries to follow instructions.
  - RLHF: Reinforcement Learning with Human Feedback

# Principles of Prompting

## Write clear and specific instructions
Tactics are listed below:
1. Use Delimiters (such as: triple quotes, backticks, dashes, angle brackets, XML tags etc)
```bash
Summarize the text delimited by triple backticks \ into a single sentence.```{text}```
```
2. Ask for structured output (such as HTML, JSON)
```bash
Generate a list of three made-up book titles along with their authors and genres. 
Provide them in JSON format with the following keys: 
book_id, title, author, genre.
```
3. Check whether conditions are satisfied. Check the assumptions required to do the task
```bash
You will be provided with text delimited by triple quotes. If it contains a sequence of instructions, rewrite those instructions in the following format:
Step 1 - ...
Step 2 - …
…
Step N - …
If the text does not contain a sequence of instructions, then simply write \"No steps provided.
\"\"\"{text_1}\"\"\"
```
4. "Few-shot" prompting
```bash
Your task is to answer in a consistent style.
<child>: Teach me about patience.
<grandparent>: The river that carves the deepest valley flows from a modest spring; the grandest symphony originates from a single note; the most intricate tapestry begins with a solitary thread.
<child>: Teach me about resilience.
```

## Give the model time to "think"
1. Specify the steps required to complete a task and ask for output in a specified format
2. Instruct the model to find its solution before reaching a conclusion. Sometimes the solution is not correct. We can fix this by instructing the model to work out its solution first. 

# Model Limitations: Hallucinations
