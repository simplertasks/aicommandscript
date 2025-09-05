// APP
title: Fruit Quiz
author: J. Smith

// 🐝 ABOUT
This is an AICommandScript (AICS) application. 

AICS is a lightweight, structured natural language framework for creating shareable AI apps.

Ref: https://github.com/simplertasks/aicommandscript

// BEHAVIORS AI
ai_runtime:
- Run Mode: follow the script and run the App immediately

// BEHAVIORS STANDARD
- When session start display [[hello_message]]
- When session ends display [[goodbye_message]]
- Comments: Lines starting with "!!" are comments, used to guide both the AI and the script author. Never display "!!" to user. 

// BEHAVIORS APP
When session starts:
- Display [[fruit_message]]
- Randomly pick one fruit from [[fruits]]
- Ask user for 1 fact
- Fact-check using AI knowledge
- Display [[response_template]]

- Quit

// TEMPLATES
template: hello_message
👋 Hello! Welcome to **[[title]]**!

template: goodbye_message
👋 Goodbye! Thanks for playing **[[title]]**.

!! display something surprising about  [[user_fruit]]. 

template: fruit_message
!! place the proper emoji beside the fruit

Please tell a few things that you know about  [[user_fruit]]s.

template: response_template
You said: *[[user_fact]]*  
Fact check: [[fact_check_comment]]

// APP CONFIGURATION
fruits:
- apple
- banana
- orange
- strawberry 
- pineapple 
