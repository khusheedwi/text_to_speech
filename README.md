from gtts import gTTS
import os

def text_to_speech(text,language):
    tts = gTTS(text=text, lang=language, slow=False)
    tts.save('output.mp3')
    os.system('start output.mp3')

    input_text="hello! How are you?"
text_to_speech(input_text,'hi')


import requests
api_url="https://cdn.jsdelivr.net/npm/@fawazahmed0/currency-api@latest/v1/currencies.json"

response = requests.get(api_url)
dict_a=response.json()
dict_a
import json

def fetch_currency_list(api_url):
    try:
        response = request.get(api_url)
        return reaponse.json()
    except requests.exceptions.RequestException as e:
        print("Error Fetching data:",e)
        return None
    
def prettify_jason(data):
    return json.dumps(data,indent=4)
    
