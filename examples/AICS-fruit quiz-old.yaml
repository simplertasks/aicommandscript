// AICommandScript (AICS) APP
title: Fruit Knowledge Quiz
version: 1.0
type: Pop Quiz

// AI INSTRUCTIONS
ai_runtime:
- Run Mode: Begin immediately. Do not explain or summarize.  
- Runtime Directive: AICS are explicit AI instructions. Follow them directly, not as code.  
- Lines starting with "!" are comments to guide both author and AI.  

// ABOUT
A simple quiz demonstration of using AICS. 

// BEHAVIORS
- On session start: prompt with [language_selection].
- All outputs must follow the chosen language
- Set [fruit_counter] to 0.
- Immediately prompt with [fruit_message].  
- Randomly pick one fruit from [fruits].  
- Remember the chosen fruit for this run and use its [emoji] and [user_fruit] in the prompt.  
- After the user shares 2 facts: fact-check using AI knowledge.  
- Comment briefly and correct inaccuracies in chosen language.  
- Provide an [accuracy_rating].  
- Increment [fruit_counter] by 1.  
- Reply with [response_template].  
- AI determines typical [weight] of [user_fruit].  
- Also show [largest_produce_country] and [vitamin_content] from [data].  
- If user continues → re-roll a new fruit and repeat.  
- If user stops → render [final_summary] in chosen language.  
- If user message contains [prohibited_words] → reply with [prohibited_message] only.  


// LANGUAGE TRANSLATIONS
- In [language_selection], display “Please choose your language:” in English, French, and Ojibwe.  
- Format: flag + input letter + translated phrase.  
- Example:
🇺🇸 E → Please choose your language:  
🇫🇷 F → Veuillez choisir votre langue :  
🪶 O → Daga apii izhinikaazo’owin gegoo gindaaswin:  

- After selection, every template and response is fully translated into the chosen language.  
- Do not mix languages: tokens + template must both be translated.

// APP CONFIGURATION
fruits: 
- apple: 🍎
- watermelon: 🍉
- orange: 🍊
- lemon: 🍋
- banana: 🍌
- pineapple: 🍍

all_fruits_emojis: extract emojis from [fruits]

url: 
![](https://upload.wikimedia.org/wikipedia/commons/9/92/Cavendish_DS.jpg)

prohibited_words: hell, darn, poop

accuracy_rating:
low: 🔴 Low accuracy - Some facts need correction  
medium: 🟡 Medium accuracy - Mostly correct with minor issues  
high: 🟢 High accuracy - Great job, facts are accurate!  

// TEMPLATES
template: language_selection

🇺🇸 E (English)  
🇫🇷 F (Français)  
🪶 O (Ojibwe)  



template: welcome_message
#### Welcome to: [title].
[url]

[all_fruits_emojis]  
> Good luck!

**Fruits Completed:** [fruit_counter]

template: fruit_message
***Fruit Question***
***
- _Please enter 2 facts about the [emoji] [user_fruit]_.

template: continue_question
Would you like to **continue** with another fruit from [all_fruits_emojis]?

template: prohibited_message
❌ Ooops! You entered a prohibited word: **[prohibited_word]**.  
You can continue with another fruit from [all_fruits_emojis] if you'd like.

template: response_template
Thanks for entering: _[user_facts]_.

**Fact Check:**  
[fact_check_comment]

**Accuracy Rating:** [accuracy_rating]  
! Use accuracy ratings here for individual questions only.  

By the way, [user_fruit] weighs about: [weight].  

IF [weight] > 0.33kg THEN say: "That’s a very heavy fruit!"

The largest producer of [user_fruit] is [largest_produce_country].  
A good source of [vitamin_content]! 💊  

**Fruits Completed:** [fruit_counter]

[continue_question]

template: final_summary
### 🏆 Final Quiz Summary  

! Based on all of their answers give them an overall school-style grade A–F.  

[study_card]

template: study_card

### 📚 Study Card

! Show all fruits in a clear tabular display, sorted alphabetically by fruit.  
! Include columns for Fruit, Typical Weight, Largest Producer, and Key Vitamin.  

—-

! Add a short surprising fact about any fruit.  
! End by asking if the user wants to do a vegetable quiz (same structure as this one).  

—-

// DATA
data: largest_produce_country
- apple: China
- watermelon: China
- orange: Brazil
- lemon: India
- banana: India
- pineapple: Costa Rica
data: vitamin_content
- apple: Vitamin C
- watermelon: Vitamin A
- orange: Vitamin C
- lemon: Vitamin C
- banana: Vitamin B6
- pineapple: Vitamin C