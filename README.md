import discord

client = discord.Client()

@client.event
async def on_ready():
    print('Logged in as')
    print(client.user.name)
    print(client.user.id)
    print('------')

@client.event
async def on_message(message):
    
    if message.content.startswith("/D"):
        
        if client.user != message.author:
            
            m = "私ワアナタヲ見テイマス" + message.author.name + "！"
            
            await message.channel.send(m)

client.run("Nzk0NzkzNjkyNjQ0MjQ1NTE0.X-__Tg.AF6cxakke7BWIiST2c-J7rDA5m4")
