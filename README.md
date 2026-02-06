import datetime

print("🤖 Chatbot: Hello! Type 'bye' to exit.")

while True:
    user = input("You: ").lower()

    # Greetings
    if user in ["hello", "hi", "hey", "hii", "good morning", "good evening"]:
        print("🤖 Chatbot: Hello! How can I help you? 😊")

    # How are you
    elif "how are you" in user:
        print("🤖 Chatbot: I am fine 😊 What about you?")

    # Bot name
    elif "your name" in user or "who are you" in user:
        print("🤖 Chatbot: I am a simple AI Chatbot made in Python.")

    # Help
    elif "help" in user or "what can you do" in user:
        print("🤖 Chatbot: I can chat, tell time/date, do simple math, and answer basic questions.")

    # Time
    elif "time" in user:
        time = datetime.datetime.now().strftime("%H:%M:%S")
        print("🤖 Chatbot: Current time is", time)

    # Date
    elif "date" in user or "today" in user:
        date = datetime.datetime.now().strftime("%d-%m-%Y")
        print("🤖 Chatbot: Today's date is", date)

    # Simple math
    elif "add" in user:
        print("🤖 Chatbot: Please enter two numbers.")
        a = int(input("First number: "))
        b = int(input("Second number: "))
        print("🤖 Chatbot: Result =", a + b)

    # Small talk
    elif "thank" in user:
        print("🤖 Chatbot: You're welcome 😊")

    elif "love you" in user:
        print("🤖 Chatbot: That's sweet 😄")

    # Exit
    elif user == "bye" or user == "exit" or user == "quit":
        print("🤖 Chatbot: Goodbye! Have a nice day 👋")
        break

    # Unknown input
    else:
        print("🤖 Chatbot: Sorry, I didn't understand that. Try asking something else.")
