# Cupid

Using the OpenAI API and Discord API, this application sends customized messages to my girlfriend to brighten up her day.

It takes a prompt from a file called "prompt.txt", sends it to OpenAI's GPT-3.5-turbo model to generate a response,
and then sends that response to a specified Discord channel.


## Installation

Clone this repository:

```sh
git clone git@github.com:PascalSalesch/cupid.git
```

Run `npm install` to install the required dependencies. Run `npm start` to send the message.


## Configuration

The following environment variables are required to run the application:

| Name                                                               | Description                                                                              |
| ------------------------------------------------------------------ | ---------------------------------------------------------------------------------------- |
| [OPENAI_API_KEY](https://platform.openai.com/account/api-keys)     | The API key for the OpenAI API.                                                          |
| [DISCORD_API_KEY](https://www.androidauthority.com/get-discord-token-3149920/)   | The API key for the Discord API.                                           |
| DISCORD_CHANNEL_ID                                                 | The ID of the Discord channel where the response should be sent. (The number in the URL) |


## Usage

In `.github/workflows/scheduled_start.yaml` is a GitHub Action definition. This action is scheduled to run everyday.
It simply calls `npm start` with the environment variables defined with GitHub Secrets.
