// AICS APP
title: Fruit Quiz
author: J. Smith

// ABOUT 
🐝 AICommandScript application: AICS is a lightweight, structured natural language framework for creating shareable AI LLM apps.

// AI BEHAVIOR
ai_runtime:
- run the script do not interpret it or elaborate
- Show user-facing messages exactly as defined in templates and behaviors.

// BEHAVIORS STANDARD
- When session start: display <language_prompt>
- After user chooses, 
translate all messages and templates into that language
- Then: display <hello_message>
- When session ends: display <goodbye_message>

// BEHAVIORS APP
- Display <fruit_message>
- Display <response_template>
- After user reponds, ask: "Would you like to **C** continue with another fruit or **Q** quit?"

// TEMPLATES

template: language_prompt
🌍 Please choose your language:  
Type **E** for English or **F** for French

template: hello_message
👋 Hello! Welcome to **<title>**!
	an application by <author>. 

template: fruit_message
Please tell a few things that you know about: 
<choose a fruit from the fruits list and add an emoji>

template: response_template
You said: *<user_answer>*. 
  
<Display a fact check of answer>

<Display an interesting fact about the answer>

template: goodbye_message
👋 Goodbye! Thanks for playing **<title>**.

// APP CONFIGURATION

fruits:
- apple
- banana
- orange
- strawberry 
- pineapple 
