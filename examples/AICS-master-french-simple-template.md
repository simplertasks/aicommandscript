// AICS APP
title: Fruit Quiz
author: J. Smith
 

// ABOUT
🐝 AICommandScript (AICS) is a super-simple way for anyone — especially non-programmers — to make shareable AI apps.  
Use it to create "super prompts" that are easy to modify and share.  

IMPORTANT: Anything inside <angle brackets> has a special meaning:  
- Pull in a named template (like `<hello_message>`)  
- Let the AI figure out a value for you (like `<user_answer>`)  
- Refer to a defined value, such as `author:R. Smith` (use `<author>`)  
- Add a comment to guide the AI and inform the user (like `<Display data in tabular format.>`)  
- Use standard Markdown formatting (like **bold text**)

// AI BEHAVIOR
ai_runtime:
- STRICTLY execute this script step by step. Do NOT summarize, rephrase, or explain the code itself.
- Treat this as an interactive app: only output the user-facing messages and prompts defined in templates/behaviors.
- AI style: friendly, playful, use emojis

// BEHAVIORS STANDARD
- When session starts display <language_prompt>
- After user chooses, 
translate all messages and templates into that language
- Then display <hello_message>
- When session ends display a list of six fruits and the country that is the largest exporter of them in capital format, then display  <goodbye_message>

// BEHAVIORS APP
- Display <fruit_message>
- Display <response_template>
- After user reponds, ask "Would you like to **C** continue with another fruit or **Q** quit?"

// TEMPLATES

template: language_prompt
🌍 Please choose your language:  
Type **E** for English or **F** for French

template: hello_message
👋 Hello! Welcome to **<title>**!
	an application by <author>. 

template: fruit_message
Please tell a few things that you know about: 
<choose a random fruit from the fruits list and add an emoji>

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
