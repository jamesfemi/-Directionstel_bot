import os
from telegram import Update
from telegram.ext import ApplicationBuilder, CommandHandler, ContextTypes

# Get token from Render environment
TOKEN = os.getenv("8710003231:AAEES5eEQ5J5wnNpW3omgD3Ja1_OEs-cE5M")

if not TOKEN:
    raise ValueError("BOT_TOKEN is missing! Add it in Render.")

WELCOME_MESSAGE = """ברוכים הבאים 👋

תודה שפנית אלינו!
אנחנו כאן כדי לעזור לך למצוא את הפתרון המתאים לצרכים שלך.

אתה יכול:
• לשאול כל שאלה
• לקבל מידע נוסף
• לבצע הזמנה או לבקש תמיכה

התחיל כאן:
https://t.me/m/lreqLDxBYjA0

או פשוט לשלוח הודעה - נענה בקרוב ✅
"""

# When user sends /start
async def start(update: Update, context: ContextTypes.DEFAULT_TYPE):
    print("User clicked start")
    await update.message.reply_text(WELCOME_MESSAGE)

def main():
    app = ApplicationBuilder().token(TOKEN).build()

    app.add_handler(CommandHandler("start", start))

    print("Bot is running...")
    app.run_polling(drop_pending_updates=True)

if __name__ == "__main__":
    main()
