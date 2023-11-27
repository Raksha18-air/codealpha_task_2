# codealpha_task_2
import nltk
from nltk.chat.util import Chat, reflections


pairs = [
    ["hi|hello|hey", ["Hello!", "Hi there!", "Hey!"]],
    ["how are you", ["I'm good, thanks. How about you?", "I'm a bot, so I don't have feelings, but I'm here to help!"]],
    ["what is your name", ["I'm a chatbot. You can call me ChatGPT."]],
    ["your age", ["I don't have an age. I'm just a computer program."]],
    ["bye|goodbye", ["Goodbye!", "See you later!", "Bye!"]],
    ["default", ["I'm not sure how to respond to that. Can you ask me something else?"]]
]

#create a chatbot
chatbot=Chat(pairs,reflections)
def start_chat():
    print("hello! I'm a simple chatbot.Please type Goodbye to end conversation.")
    while True:
        user_input=input()
        if user_input.lower()== 'bye':
            print("bye! have a great day")
            break
        response=chatbot.respond(user_input)
        print("Chat:",response)
start_chat()
