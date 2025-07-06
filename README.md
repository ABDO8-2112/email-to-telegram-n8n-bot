# Email to Telegram Bot Automation using n8n

Automate forwarding specific Gmail emails to a Telegram chat using n8n workflows.

## Overview

This workflow uses n8n to monitor a Gmail inbox and forwards emails whose subject contains `#telegram` to a Telegram bot as a message.

- Connects to Gmail via **Email Trigger** using a Google App Password.
- Filters emails based on subject content.
- Sends email body text to Telegram via a bot.

## Features

- Real-time email monitoring and forwarding.
- Subject-based filtering (`#telegram` keyword).
- Plain text extraction of email body for Telegram.
- Easy setup with n8n no-code automation.

## Prerequisites

- Gmail account with **App Password** enabled (for n8n access).
- Telegram account with a bot created via [BotFather](https://t.me/BotFather).
- n8n instance running and accessible.

## Setup Instructions

1. Generate an **App Password** in your Google Account for the Gmail integration.  
2. Configure the **Email Trigger** node in n8n with your Gmail and app password credentials.  
3. Add an **If** node to filter emails with subjects containing `#telegram`.  
4. Create a Telegram bot and get the Bot Token from [BotFather](https://t.me/BotFather).  
5. Configure the **Telegram** node in n8n with your Bot Token and target Chat ID.  
6. Connect the nodes so that filtered emails are sent as messages to Telegram.

## Usage

- Send an email to your Gmail with `#telegram` in the subject.  
- Receive the email body content as a message in your Telegram chat via the bot.

## Notes

- Email bodies are extracted as plain text for readability.  
- Telegram messages are limited to ~4096 characters due to API restrictions.

---

Feel free to fork and customize this workflow to suit your needs!

