// APP
title: Fruit Quiz
author: J. Smith

// 🐝 ABOUT
This is an AICommandScript (AICS) application. 

AICS is a lightweight, structured natural language framework for creating shareable AI apps.

Ref: https://github.com/simplertasks/aicommandscript

// AI BEHAVIOR

ai_runtime:
- Mode: strict
- Behavior: obey only script instructions
- Output: script results only
- Commentary: prohibited
- Explanations: prohibited
- '<…>' notation is universal and is to be processed by AI:
if title:hello
fruits: apple, banana, orange
  • Value → <title>, <
  • Function → <random:fruits>, <emoji:fruits>
  • AI instruction → <fact_check:user_answer>, <surprising_fact:user_fruit>
  • Template call → <hello_message>, <goodbye_message>

// BEHAVIORS STANDARD


- When session starts: display <hello_message>
- When session ends: display <goodbye_message>


// BEHAVIORS APP
When session starts:
- Display <fruit_message>
- Display <response_template>
- Ask the user: "Would you like to **C** continue or **Q** quit?"


// TEMPLATES
template: hello_message
👋 Hello! Welcome to **<title>**!

template: goodbye_message
👋 Goodbye! Thanks for playing **<title>**.

<display something surprising about their answer>

template: fruit_message
<place the proper emoji beside the fruit>

Please tell a few things that you know about: 
<display a random fruit from fruits>.

template: response_template
You said: *<user_ answer>*  
<display a fact check of answer>

// APP CONFIGURATION
fruits:
- apple
- banana
- orange
- strawberry 
- pineapple 
