# Sylvanus-Ochieng-
Plp Assignments on Python
import random
#Create a simple Python program that asks the user to input two numbers and a mathematical operation (addition, subtraction, multiplication, or division).

def greeting_app():
    name = input("What's your name? ")
    color = input("What's your favorite color? ")
    print(f"Hello, {name}! Your favorite color, {color}, is awesome!\n")

#Perform the operation based on the user's input and print the result.

def quiz_game():
    questions = {
        "What is the capital of France?": "a",
        "What is 5 + 3?": "b",
        "Which language is known as the language of the web?": "c"
    }
    options = [
        "a) Paris  b) London  c) Rome",
        "a) 10  b) 8  c) 5",
        "a) C++  b) Java  c) JavaScript"
    ]
    score = 0
    
    for i, (question, answer) in enumerate(questions.items()):
        print(question)
        print(options[i])
        user_answer = input("Your answer (a/b/c): ")
        if user_answer.lower() == answer:
            print("Correct! ✅\n")
            score += 1
        else:
            print("Wrong! ❌\n")
    
    print(f"Your final score: {score}/{len(questions)}\n")

def joke_generator():
    jokes = [
          "Why do programmers prefer dark mode? Because light attracts bugs!",
        "Why was the Python programmer so good at coding? Because he had snake-like skills!",
        "What do you call a programmer from Finland? Nerdic!"
    ]
    print(random.choice(jokes) + "\n")

    
    #Example: If a user inputs 10, 5, and +, your program should display 10 + 5 = 15.

def basic_calculator():
    try:
        num1 = float(input("Enter the first number: "))
        num2 = float(input("Enter the second number: "))
        operation = input("Enter an operation (+, -, *, /): ")
        
        if operation == '+':
            result = num1 + num2
        elif operation == '-':
            result = num1 - num2
        elif operation == '*':
            result = num1 * num2
        elif operation == '/':
            if num2 != 0:
                result = num1 / num2
            else:
                print("Error: Division by zero is not allowed.")
                return
        else:
            print("Invalid operation. Please enter +, -, *, or /.")
            return
        
        print(f"{num1} {operation} {num2} = {result}\n")
    except ValueError:
        print("Invalid input. Please enter numerical values.\n")

def main():
    while True:
        print("Choose a program to run:")
        print("1. Greeting App")
        print("2. Quiz Game")
        print("3. Joke Generator")
        print("4. Basic Calculator")
        print("5. Exit")
        
        choice = input("Enter your choice (1-5): ")
        print()
        
        if choice == "1":
            greeting_app()
        elif choice == "2":
            quiz_game()
        elif choice == "3":
            joke_generator()
        elif choice == "4":
            basic_calculator()
        elif choice == "5":
            print("Goodbye!")
            break
        else:
            print("Invalid choice. Please try again.\n")

if __name__ == "__main__":
    main()
