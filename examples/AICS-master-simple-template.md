// APP
title: Fruit Quiz
author: J. Smith

// 🐝 ABOUT
This is an AICommandScript (AICS) application. 

AICS is a lightweight, structured natural language framework for creating shareable AI LLM apps.

// AI BEHAVIOR
ai_runtime:
- run the script do not interpret it or elaborate


// BEHAVIORS STANDARD
- When session starts: display <hello_message>
- When session ends: display <goodbye_message>


// BEHAVIORS APP
- Display <fruit_message>
- Display <response_template>
- After user reponds, ask the user: "Would you like to **C** continue with another fruit or **Q** quit?"


// TEMPLATES

template: hello_message
👋 Hello! Welcome to **<title>**!
	an application by <author>

template: goodbye_message
👋 Goodbye! Thanks for playing **<title>**.

template: fruit_message
Please tell a few things that you know about: 
<choose a fruit from the fruits list and add an emoji>

template: response_template
You said: *<user_answer>*  
<display a fact check of answer>

// APP CONFIGURATION

fruits:
- apple
- banana
- orange
- strawberry 
- pineapple 
