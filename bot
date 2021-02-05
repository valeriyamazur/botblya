import telebot

from config import token
bot = telebot.TeleBot(token)

@bot.message_handler(commands=['start'])
def start_message(message):
    bot.send_message(message.chat.id, 'Привет, ты хочешь увидеть фото милой животинки?')


@bot.message_handler(content_types=['text'])
def send_text(message):
    if 'да' in message.text.lower() or 'угу' in message.text.lower() or 'ага' in message.text.lower() or 'хочу' in message.text.lower():
        bot.send_message(message.chat.id, 'Надейся и жди, однажды она сможет меня дописать')
    else:
        bot.send_message(message.chat.id, 'Очень жаль :С')


bot.polling()
