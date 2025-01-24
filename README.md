def quiz_game():
    print("Welcome to the 10-Question Quiz Game!")
    print("Answer each question by typing the letter of your choice (a, b, c, or d).")
    print("Each correct answer gives you 10 points. Good luck!")

    # Questions and answers
    questions = [
        {
            "question": "What is the national bird of India?",
            "options": ["a) Crow", "b) eagle ", "c) Peacock ", "d) pigeon "],
            "answer": "c"
        },
        {
            "question": "Which planet is known as the Red Planet?",
            "options": ["a) Venus", "b) Mars", "c) Jupiter", "d) Saturn"],
            "answer": "b"
        },
        {
            "question": "What do bees produce?",
            "options": ["a) Milk", "b) Water", "c) Honey", "d) Alcohol "],
            "answer": "c"
        },
        {
            "question": "What is the largest ocean on Earth?",
            "options": ["a) Indian Ocean", "b) Atlantic Ocean", "c) Arctic Ocean", "d) Pacific Ocean"],
            "answer": "d"
        },
        {
            "question": "What is the square of 81?",
            "options": ["a) 6216", "b) 6561", "c) 6001", "d) 6651"],
            "answer": "b"
        },
        {
            "question": "What is the chemical symbol of water?",
            "options": ["a) CO2", "b) He", "c) H2O", "d) N"],
            "answer": "c"
        },
        {
            "question": "What is the capital of India?",
            "options": ["a) Andhra Pradesh", "b) Hyderabad ", "c) Bengolore ", "d) New Delhi"],
            "answer": "d"
        },
        {
            "question": "In which sport is the term \"home run\" used?",
            "options": ["a) Cricket ", "b) Volleyball ", "c) Base ball", "d) Football "],
            "answer": "c"
        },
        {
            "question": "What is the boiling point of water in Celsius?",
            "options": ["a) 75", "b) 100", "c) 107", "d) -100"],
            "answer": "b"
        },
        {
            "question": "What is the rarest blood type?",
            "options": ["a) O positive ", "b) AB negative ", "c) B positive ", "d) A negative "],
            "answer": "b"
        }
    ]

    score = 0

    # Loop through questions
    for i, q in enumerate(questions, start=1):
        print(f"Question {i}: {q['question']}")
        for option in q["options"]:
            print(option)

        user_answer = input("Your answer: ").lower()
        if user_answer == q["answer"]:
            print("Correct!\n")
            score += 1
        else:
            print(f"Wrong! The correct answer was {q['answer']}.\n")

    # Display the final score
    print(f"Your final score is {score}/{len(questions)}")
    if score == len(questions):
        print("Congratulations! You got a perfect score!")
    elif score > len(questions) // 2:
        print("Well done! You did great!")
    else:
        print("Better luck next time!")

# Run the game
quiz_game()