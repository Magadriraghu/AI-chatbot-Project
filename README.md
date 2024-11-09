# AI-chatbot-Project
import google.generativeai as ai
#api key
API_KEY = "AIzaSyB7J2w6S8EfmextBUw5dKnVkGNdYAYoRd8"
#configure the API
ai.configure(api_key=API_KEY)
#Create a new model
model = ai.GenerativeModel("gemini-pro")
chat = model.start_chat()
#start a conversation
while True:
    message = input("You: ")
    if message.lower() == 'bye':
        print('Chatbot: Goodbye!')
        break
    response = chat.send_message(message)
    print('Chatbot:', response.text)
