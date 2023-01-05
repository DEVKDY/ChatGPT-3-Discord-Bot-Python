# ChatGPT-3 Discord Bot
This clientsided chatbot with multiple commands uses OpenAI's and Discord's APIs to participate in server channels in real time. 

# Functionality and commands
Each command should be typed prior to your prompt (ex. !code create a python script that prints out the HWID for the HDD)

**!image:**

The !image command uses OpenAI's image-alpha-001 model to produce a 512x512 image based on the given prompt

**!chat:**

The !chat command uses OpenAI's text-davinci-003 model to generate a response based on a prompt. It will split up the generated response into parts that are sent to discord channel in order to increase engagement. 

**!code:**

!code command is the same as the chat command except it sends a response in a code block. This makes copying text and code easy as doing so with the !chat command will result in too many time stamps and structuring issues.

**!creative:**

The !creative command is the same as the !chat command except it uses a temperature of 1 instead of 0.5. Look up OpenAI's explanation of the temperature variable.

**!cc:**

The !cc command combines the functionality of the !creative and !code commands.

# Installation
Step 1:
```
Set openai.api_key to your OpenAI API key
Set your discord server channel ID in client.get_channel(HERE)
Set your discord bots secret token in client.run("HERE")
```
Step 2:
```
Run ChatGPT-DiscordBot.py
```

# Changelog and notes
The bot can sometimes glitch or take more time to respond usually because of the nature of the prompt. All of the issues I've encountered have resolved themselves by waiting and giving the bot more time to process a response. If the response is stuck at "generating response" then retype the prompt or slightly modify it.

1-5-2023: added !help command
