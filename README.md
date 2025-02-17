# Build a Chatbot with Amazon Lex

## Project Overview

This project demonstrates how to build a conversational interface (chatbot) using Amazon Lex. The example shows how to create a simple banker chatbot that can understand and respond to user queries.

**Author:** Pobbathi Amaravathi   
**Source:** NextWork.org  
**Time to Complete:** Approximately 30 minutes

## What is Amazon Lex?

Amazon Lex is a powerful service provided by AWS used for the development of conversational application interfaces. Its ability to understand various natural languages and automatic speech recognition makes it simpler for users to create interesting user interfaces that resemble real-world conversations. 

## Project Implementation

### 1. Setting up a Lex Chatbot

- Created the chatbot from scratch with Amazon Lex (setup time: less than 5 minutes)
- Created a role with basic permissions for Amazon Lex to call other AWS services
- Used the default intent classification confidence score of 0.40 (meaning the chatbot needs to be at least 40% confident to provide a response)
  !(images/img.png)


### 2. Creating Intents

An intent represents what the user is trying to achieve in their conversation with the chatbot. Examples include:
- Checking a bank account balance
- Booking a flight
- Ordering food

For this project, the first intent created was **WelcomeIntent**, designed to greet users when they say hello.

### 3. Understanding FallbackIntent

- **Testing Phase:** The chatbot responded successfully to inputs like "Hello", "hiya", etc.
- **Error Handling:** When the input "How are you?" was entered, the chatbot returned an error message: "Intent FallbackIntent is fulfilled" because it couldn't recognize the utterance with sufficient confidence.

### 4. Configuring FallbackIntent

The FallbackIntent is a default intent in every Amazon Lex chatbot that triggers when:
- The chatbot has a confidence score below the threshold (40% in this case)
- None of the defined intents match the user input

To improve the user experience, the default FallbackIntent message was modified to make it clearer that the chatbot didn't understand the request.

### 5. Adding Response Variations

To make the chatbot more conversational, variations were added to the responses:
- The configuration was done by expanding the "Closing responses" section
- Multiple message variations were created for the FallbackIntent
- This approach helps provide dynamic responses, making the interaction feel more natural

## Key Learnings

- Amazon Lex provides a straightforward way to build conversational interfaces
- Configuring proper fallback behavior is important for handling unexpected inputs
- Adding variations to responses creates a more dynamic and engaging user experience

## Next Steps

For more projects like this one, visit [nextwork.org](https://nextwork.org)

---

*NextWork.org - Everyone should be in a job they love.*
