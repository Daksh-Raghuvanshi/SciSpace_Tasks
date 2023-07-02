# SciSpace_Tasks
Hello, the assignment for prompt engineering consists of 3 different but small problems. These
problems will give you a glimpse of some of the complex prompt engineering done here at
SciSpace.

In all the problems you are expected to write a python script which calls the Open AI service and
prints the expected output from GPT to the console. You have to use the ChatGPT (GPT-3.5-turbo) model with a chat completion API.

The assignment should ideally be done in one day. For any queries you can send an email to
Rohan Tondulkar (rohan@typeset.io).

Have a happy prompt engineering time! 

## Problem 1: Paraphraser
You are expected to build a prompt for GPT to act as a paraphraser. The inputs would be
1. Input text paragraph
2. Output tone (Academic / Creative / Aggressive)
3. Output length (1x i.e. same length / 2x i.e. twice the length / 3x i.e. thrice the length).
The output should not be a text paragraph. It needs to be a list of sentences in JSON that
should be easily processed by using below code.
import json
json.loads(gpt_output)

## Problem 2: Chatbot QnA
You have to build a prompt where ChatGPT answers questions about the researcher Tirthankar
Ghosal using the information given to ChatGPT. You can use any data from google scholar page
for Tirthankar Ghosal to send in the prompt. You can select the data that you want to provide in
the prompt based on the number of tokens.
The chatbot should be able to answer the below questions accurately:
1. What are the most influential papers by this author?
2. How many papers did the author publish in the last year?
3. What are the takeaways from those papers?
4. Who are the coauthors of the Tirthankar?

## Problem 3: Answer with citation
Researchers like answers which also give the citations or original sources with them. It makes it
easier to trust the answer and verify the answer using the cited source. We want ChatGPT to do
the same for our use case.
In research use-case, the citations are research papers which are usually represented in the
format of Author, et al. For a given question we will be giving context from multiple research
papers. ChatGPT should answer the question using only those contexts and give citations
based on the context used in the answer for every line.

Bonus marks if you submit a zero shot prompt.

You can use the below example for testing your prompt.

Example scenario:

Question: What is the difference between GPT and BERT models?

Context 1 author: Trinita Roy 

Context 1 text: BERT is an encoder transformer model which is trained on two tasks - masked
LM and next sentence prediction.

Context 2 author: Asheesh Kumar

Context 2 text: GPT is a decoder model which works best on sequence generation tasks.

Context 3 author: Siddhant Jain

Context 3 text: LSTMs have been very popular for sequence to sequence tasks but have
limitations in processing long texts.

Sample Answer: While GPT is a decoder model (Kumar et al.), BERT is an encoder transformer
model (Roy et al.). Based on their training tasks, GPT is more suitable for sequence generation
(Roy et al). BERT is more suited for next sentence prediction (Kumar et al.).
