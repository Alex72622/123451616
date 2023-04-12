from telegram.ext import Updater, MessageHandler, Filters

updater = Updater(token='5804754597:AAG_BKYXcnrw4iZqRb8cvAHa91eLmt9o2xw')
dispatcher = updater.dispatcher
def process_msg(bot, update):
    chat_id = update.message.chat_id
    message = update.message.text
    response = {"text": chat_bot.call(message), "chat_id": chat_id}
    bot.send_message(**response)
   
message_handler = MessageHandler(Filters.text, process_msg)
dispatcher.add_handler(message_handler)
updater.start_polling()
