# Note
This is a fork of [DialoKEY](https://github.com/Lucas-Munz/DialoKEY_Codebase), updating it to the current openAI API version and changing the fine-tune targets to be gpt3.5-turbo and gpt4-turbo respectively.

## Careful
The code inside the directory `Evalution\` was not tested and the current requirements file does not include requirements for this code.

# About this project
This repository contains all code necessery to fine-tune DialoKEY, a GPT based model which can answer any question (or continue any conversation) given a set of keywords about the answer.
The original DialoKEY is the output of the following master thesis: [Transforming keywords into conversation](https://utheses.univie.ac.at/detail/67331/).

All prompts to DialoKEY have to end with `Answer\n\n###\n\n`. This makes it easier for GPT to recognize that the prompt has ended.

All completions DialoKEY makes end with `END` this allows you to specify it as a stop token.

# Example interactions with DialoKEY

## Interaction 1

Simple interaction with DialoKEY.

### Prompt:
```
Question: What is the nature of your complaint?
Keywords: neighbor illegally dumping garbage
Answer:\n\n###\n\n
```

### DialoKEY output:
```
My neighbor is illegally dumping garbage in my yard. END
```

## Interaction 2

A more complex interaction with DialoKey, including a dialogue history.
```
Question: Where are you heading to?
Answer: I'm trying to go downtown.
Question: I could tell you where to get off.
Answer: You can? That would be very nice of you. Thank you.
Question: I'm happy to help a stranger anytime.
Keywords: street
Answer:\n\n###\n\n
```

```
What's the street that I should get off on? END
```


# Installation

Create a python 3.11 environment and install the packages in the requirements.txt
(The code was tested on python 3.11.7)

Linux:
(Inside the root of this repository)
```
python3.11 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

Other OS analogously


