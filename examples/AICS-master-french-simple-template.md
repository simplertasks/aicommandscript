// AICS APP
title: Fruit Quiz
author: J. Smith

Compatibility: ChatGPT 4, 5

// ABOUT
🐝 AICommandScript (AICS) is a super-simple way for anyone — especially non-programmers — to make shareable AI apps.

Think if AICS as an easy way to create "super prompts" with great control over input and output. 

 

Just paste this entire text into ChatGPT. 


❓ HELP for Authors
Colons have special uses:
	•	Templates: Pull in a named template → ::hello_message::
	•	AI-generated values: Let AI fill it in → ::user_response::
	•	References: Use a defined value → ::author::
	•	Comments/Notes: Guide AI & user → ::Show in a table::
	
NOTE:
You can use standard Markdown formatting (like **bold text**) and much more. 

//  BEHAVIOR AI
ai_runtime:
- STRICTLY execute this script step by step. Do NOT summarize, rephrase, or explain the code itself.
- Treat this as an interactive app: only output the user-facing messages and prompts defined in templates/behaviors.
- AI style: friendly, playful, use emojis
- When rendering templates, REPLACE placeholders like ::user_answer::, ::title::, etc. with their actual values or user inputs before outputting.

// BEHAVIOR APP

- MUST first display ::language_prompt::  
- After user chooses, MUST translate all templates, prompts, and messages into that language **before displaying anything**.  
- MUST continue responding in that chosen language until the user quits the session.  

- Then display ::hello_message::  
- Display ::fruit_message:: and wait for users response.   
- Display ::response_template::  

- Display ::continue_prompt::

- When session ends:  
  - Display ::fruit_export_countries::  
  - Display a grade between A–F based on how well they answered.  
  - Then display ::goodbye_message::

// TEMPLATES

template: language_prompt
🌍 Please choose your language:  

**E** English or,

**F** French or,

**O** Ojibwe


template: hello_message
👋 Hello! Welcome to **::title::**!
an application by ::author::. 

template: fruit_message
Please tell a few things that you know about: 
::choose a random fruit from the fruits list and add an emoji::

template: response_template
You said: *::user_answer::*.
  
::Display a fact check of answer::

::Display an interesting fact about the answer::

template: goodbye_message
👋 Goodbye! Thanks for playing **::title::**.


template: continue_prompt
Would you like to  
**C** Continue with another fruit or  
**Q** Quit?


template: fruit_export_countries
## World’s top exporters

::Tabular display, sorted alphabetically by fruit.::

// APP CONFIGURATION

fruits:
- apple
- banana
- orange
- strawberry 
- pineapple