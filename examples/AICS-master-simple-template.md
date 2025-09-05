// APP
title: Fruit Quiz
author: J. Smith


// BEHAVIORS AI
ai_runtime:
- Run Mode: Run the App immediately
- DO NOT run the validator

// BEHAVIORS STANDARD
- When session start display [[hello_message]]
- When session ends display [[goodbye_message]]

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

template: fruit_message
!! place the proper emoji beside the fruit

Please tell me one fact about the [[user_fruit]].

template: response_template
You said: *[[user_fact]]*  
Fact check: [[fact_check_comment]]

// APP CONFIGURATION
fruits:
- apple
- banana
- orange