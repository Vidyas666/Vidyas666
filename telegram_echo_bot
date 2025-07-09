from telegram import Update
from telegram.ext import Updater, CommandHandler, MessageHandler, Filters, CallbackContext

TOKEN = "YOUR_BOT_TOKEN"

def start(update: Update, context: CallbackContext) -> None:
    update.message.reply_text('नमस्ते! मैं आपका बॉट हूँ')

def echo(update: Update, context: CallbackContext) -> None:
    update.message.reply_text(f"आपने कहा: {update.message.text}")

def main():
    updater = Updater(TOKEN)
    dispatcher = updater.dispatcher
    dispatcher.add_handler(CommandHandler("start", start))
    dispatcher.add_handler(MessageHandler(Filters.text & ~Filters.command, echo))
    updater.start_polling()
    updater.idle()

if __name__ == '__main__':
    main()