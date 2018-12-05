#!/usr/bin/env python3.6

import discord

TOKEN = 'XXXXXXXX'

client = discord.Client()

@client.event
async def on_message(message):
    # we do not want the bot to reply to itself
    if message.author == client.user:
        return

    if message.content.startswith('!Rick Rolled'):
        msg = 'get rolled {0.author.mention}'.format(message)
        await client.send_message(message.channel, msg)
        msg2 = '!play https://www.youtube.com/watch?v=dQw4w9WgXcQ{'
        await client.send_message(message.channel, msg2)

@client.event
async def on_ready():
    print('Logged in as')
    print(client.user.name)
    print(client.user.id)
    print('------')

client.run(TOKEN)
