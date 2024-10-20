import discord
import os
from dotenv import load_dotenv
import ezcord
intents = discord.Intents.all()

bot = ezcord.Bot(intents=intents)





if __name__ == "__main__":
    bot.load_cogs(subdirectories=True)

    load_dotenv()
    bot.run(os.getenv("TOKEN"))
