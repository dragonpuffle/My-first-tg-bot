# https://t.me/MininCinemaBot
It was my first tg bot
I started from this:

 import time
 import logging
 import telebot

 from aiogram import Bot, Dispatcher, executor, types

#TOKEN = "6197930855:AAHSQKZ8WkbsX77MF97taw09vGMqfNhjeug"

bot = telebot.TeleBot('6197930855:AAHSQKZ8WkbsX77MF97taw09vGMqfNhjeug')


@bot.message_handler(commands=['start'])
def start(message):
     user_id = message.from_user.id
     u_name = message.from_user.first_name
     user_full_name = message.from_user.full_name
     logging.info(f'{user_id} {user_full_name} {time.asctime()}')
    bot.send_message(message.chat.id, '<b>Привет</b>', parse_mode='html')


bot.polling(none_stop=True)

But in the end I've made it via https://robochat.io/dashboard/projects 
Here's the link https://t.me/MininCinemaBot
