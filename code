import discord
from discord.ext import commands

bot = commands.Bot(command_prefix="<")

@bot.event
async def on_ready():
    print("Bot running with:")
    print("Username: ", bot.user.name)
    print("User ID: ", bot.user.id)
    print('Servers connected to:')
    for guild in bot.guilds:
        print(f'{guild.name}({guild.id})')

@bot.command(name='serverlist')
async def serverlist(ctx):
    for guild in bot.guilds:
        await ctx.send(f'Conected to: **{guild.name}**({guild.id})')


bot.run("bot-token")
