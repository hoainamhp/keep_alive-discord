# keep_alive-discord python
Keep_alive Discord


from flask import Flask
from threading import Thread

app = Flask('')

@app.route('/')
def home():
    return "Bot is Up!"

def run():
  app.run(host='0.0.0.0',port=8080)

def keep_alive():
    t = Thread(target=run)
    t.start()




add code replit:
python3 -m poetry init --no-interaction
python3 -m poetry add discord
