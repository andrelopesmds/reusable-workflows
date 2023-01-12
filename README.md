# Reusable-workflows

Set of reusable workflows to avoid code duplication


## Telegran notification

Sends a notification to a Telegram channel using its bots

### Setup

1 - Create a bot ([docs](https://core.telegram.org/bots)) and add it to the desired channel

2 - Set the repo secrets as follows:
  - `TELEGRAM_CHAT_ID` for the chat id
  - `TELEGRAM_BOT_TOKEN` for the bot token


### Usage

```
name: Telegram notification

on:
  push:
    branches:
      - main

jobs:
  send-telegram-notification:
    uses: andrelopesmds/reusable-workflows/.github/workflows/telegram-notification.yml@main
    with:
      message: 'new code merged to main'
    secrets: inherit
```
