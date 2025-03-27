# 🏦 AWS Lex Bank Bot

A conversational banking chatbot built using **Amazon Lex V2** and **AWS Lambda**, designed to handle basic user interactions like checking account balances and transferring funds.

## 🛠 Technologies Used

<p align="left">
  <img src="https://img.shields.io/badge/AWS%20Lex-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white" alt="AWS Lex">
  <img src="https://img.shields.io/badge/AWS%20Lambda-232F3E?style=for-the-badge&logo=amazonaws&logoColor=white" alt="AWS Lambda">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
</p>


This project showcases:
- Intent recognition
- Slot filling
- Context carryover between intents
- Lambda integration for fulfillment

---

## Features

### Amazon Lex Intents
- **CheckBalance** – Ask for the balance of a specific account.
- **TransferFunds** – Move money between accounts.
- **FollowupCheckBalance** – Allows users to check another balance without repeating verification.
- **FallbackIntent** – Handles unrecognized input gracefully.
- **WelcomeIntent** – Greets users when they open the chat.

### Slots
- Custom slot type for `AccountType` (e.g., checking, savings)
- Shared slot types for `sourceAccountType` and `targetAccountType` in transfers
- Slot value prompts with context awareness

### Context Carryover
- Stores user info like **birthday** for smoother multi-step interactions across intents

### Lambda Integration
- Python Lambda function handles backend logic
- Custom responses and validation using code hooks

---

## Getting Started

### 1. Import Bot
- Go to [Amazon Lex V2 Console](https://console.aws.amazon.com/lex/)
- Click **Create bot** → **Import**
- Upload `BankerBot.zip` from the `full-export` folder

### 2. Set up Lambda
- Deploy `BankingBotEnglish.py` to a new Lambda function
- Connect it to your Lex bot as a fulfillment code hook

### 3. Test
- Use the Lex console to test via text or voice
- Try utterances like:  
  - “What’s the balance in my savings?”  
  - “Transfer $500 from checking to savings.”

---

## Demo

![image](https://github.com/user-attachments/assets/c7ba66cf-88a6-419b-a694-350e003e3607)

![image](https://github.com/user-attachments/assets/028e8c03-7df0-4b32-bdf9-70dd2d52249d)

![image](https://github.com/user-attachments/assets/0d177f3a-7e7a-482f-9c14-82316ad0cde5)





