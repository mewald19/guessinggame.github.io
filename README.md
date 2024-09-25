# guessinggame.github.io
```mermaid

flowchart TD
[The guessing game starts, first a random number is generated between 0 and 100.]: # 
    A[Start] --> B[Random Number Generator between 0 and 100] --> 
[User will then enter a number between 0 and 100.]: #     
    C[User entered number guess between 0 and 100] --> 
[Here we do a validation check, we determine if it is text or if it is a number.]: # 
    D{User Input Validation} --> E[Is it Text] & F[Is it a Number]
[If we determine yes it is text, it will take you back to guess a number.]: # 
    E -- Yes --> G([Please use a number for your guess])
    G --> C
    F -- Yes --> H[Is the Random Number equal to the User Guess]
[If we determine it is a number we then ask if the random number is equal to the user guess.  If this is true we will return the result Correct.]: # 
    H -- Yes -->  I[Correct]
[If it is determined the random number is not equal to the user guess, we will then ask if the random number is less then the user guess.  If this is true we will return the result Too High.]: # 
    H -- No --> J[Is the Random Number less then the User Guess]
    J -- Yes --> K[Too High]
[At this point we have the determined the random number is neither equal to or less then the user guess, but we have to ask the question of is the random number is greater then the user guess.  If that is true we will return the result Too Low.]: # 
    J -- No --> L[Is the Random Number greater then the User Guess]
    L -- Yes --> M[Too Low]
[If the user gets the result of Too Low or Too High, they will be taken back to user entered number guess to try again.]: # 
    K & M --> N([Guess Again])
    N --> C
    I --> O[End]
```