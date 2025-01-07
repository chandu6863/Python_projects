# Python_projects :13
# PROJECT TITLE: Caesar Cipher (Project Number: 1)

## Algorithm

1. **Input Selection**:
   - Prompt the user to select the operation by typing `'encode'` for encryption or `'decode'` for decryption.

2. **User Input**:
   - Prompt the user to input the message (`text`) they want to encode or decode.
   - Ask for the shift amount (`shift`) as an integer, which will determine the number of positions each letter in the message is shifted.

3. **Define the Caesar Cipher Function**:
   - Create a function called `caeser(text, shift, direction)`, which will process the text based on the chosen `direction`:
     - If `direction` is `"encode"`, each letter in the `text` will be shifted **forwards** in the alphabet by the shift amount.
     - If `direction` is `"decode"`, each letter in the `text` will be shifted **backwards** by the shift amount.

4. **Character Shifting**:
   - For each letter in the `text`:
     - Find its position in the `alphabet` list.
     - Calculate the new position by adding (for encoding) or subtracting (for decoding) the shift amount.
     - Replace the original letter with the letter at the new position.
   - Non-alphabet characters are ignored and added to the output as they are.

5. **Output Result**:
   - Display the encoded or decoded text to the user.

6. **Play Again Option** (Optional):
   - After showing the result, prompt the user if they want to continue. If yes, restart the process; otherwise, end the program.



# PROJECT TITLE: Basic Calculator (Project Number: 2)

## Algorithm

1. **Initialize Calculation**:
   - Prompt the user to enter the first number (`first_num`).
   - Display available operations: `+`, `-`, `*`, and `/`.
   - Ask the user to choose an operation (`operation`).
   - Prompt the user to enter the second number (`second_num`).

2. **Define the Calculation Function**:
   - Create a function named `calculator(a, b, operation)` to perform the arithmetic operation on `a` and `b`:
     - If `operation` is `+`, calculate `a + b`.
     - If `operation` is `-`, calculate `a - b`.
     - If `operation` is `*`, calculate `a * b`.
     - If `operation` is `/`, calculate `a / b`.
   - Print the result of the calculation.

3. **Continue or Restart Calculation**:
   - Ask the user if they want to continue with the current result:
     - If the user enters `"y"`, set `calculation_continue = True` to continue using the current result.
     - If the user enters `"n"`, reset the program by calling `calculator1()` for a new calculation.

4. **Loop for Continued Calculation**:
   - While `calculation_continue` is `True`, repeat the following:
     - Display the available operations.
     - Prompt the user to choose a new `operation`.
     - Ask for the next number (`second_num`).
     - Call the `calculator` function to perform the operation with the current result and `second_num`.

5. **End Program**:
   - If the user chooses not to continue (`calculation_continue = False`), the program ends.



# PROJECT TITLE: Blackjack Game (Project Number: 3)

## Algorithm

1. **Initialize Game**:
   - Prompt the user to decide if they want to play the Blackjack game by typing `'y'` to start or `'n'` to exit.
   - If the user selects `'y'`, clear the console and proceed.

2. **Setup Deck and Hands**:
   - Create a `cards` list containing all possible card values, including `11` for Ace.
   - Initialize empty lists `my_cards` and `computer_cards` for the player's and computer's cards, respectively.
   - Set `current_sum` for the player’s total and `current_total` for the computer’s total.

3. **Draw Initial Cards**:
   - Deal two cards to the player and one card to the computer:
     - For each card dealt, add its value to the player’s or computer's current total.
   - Display the player’s cards and their current total, along with the computer's first card.

4. **Check for Initial Win Condition**:
   - If the player's initial total equals `21`, declare the player as the winner.

5. **Player’s Turn**:
   - Prompt the player to either take another card (`'y'`) or pass (`'n'`):
     - If the player selects `'y'`, continue drawing cards:
       - If the player’s total is above `10` and the next card drawn is an `11` (Ace), convert it to `1`.
       - Add the new card to the player’s hand and update their total.
       - Display the updated hand and total.
       - If the player’s total is `21`, they win. If it’s over `21`, they lose.
     - If the player chooses to pass, proceed to the computer’s turn using the `black_jack()` function.

6. **Computer’s Turn (black_jack function)**:
   - Draw cards for the computer while its total is below `21`:
     - If the computer’s total is over `10` and it draws an Ace (`11`), convert the Ace to `1`.
     - Add the drawn card to the computer's hand and update its total.
     - Display the computer's current hand and total.
   - Determine the game outcome:
     - If the computer's total exceeds `21`, the player wins.
     - If the computer's total is higher than the player’s but under `21`, the computer wins.
     - If both totals are the same, the game is a tie.

7. **End Game**:
   - Display the final result based on conditions, and ask the player if they’d like to start a new game.


# PROJECT TITLE: Number Guessing Game (Project Number: 4)

## Algorithm

1. **Welcome Message**:
   - Display a welcome message introducing the number guessing game.

2. **Select Difficulty Level**:
   - Prompt the user to select a difficulty level: `'easy'` or `'hard'`.
   - If the user selects `easy`, set `attempts` to `10`.
   - If the user selects `hard`, set `attempts` to `5`.

3. **Generate Random Number**:
   - Generate a random number between `1` and `10` (inclusive) as the target number for the user to guess.

4. **Start Guessing Loop**:
   - Set a variable `i` to the number of `attempts`.
   - While `i` is greater than `0`, do the following:
     - Display the number of remaining attempts.
     - Prompt the user to make a guess (`guess_number`).

5. **Check Guess**:
   - If the user’s guess is equal to the `random_number`, print a success message indicating that they guessed the correct number, and break the loop.
   - If the user’s guess is lower than the `random_number`, inform the user with a message “Too low” and ask them to guess again.
   - If the user’s guess is higher than the `random_number`, inform the user with a message “Too high” and ask them to guess again.

6. **Reduce Attempt Count**:
   - After each guess, reduce `i` by `1`.
   - If `i` reaches `0`, display a message indicating that the user is out of attempts and end the game.
  

# PROJECT TITLE: High-Low Guessing Game (Project Number: 5)

## Algorithm

1. **Initialize Game**:
   - Set a variable `game` to `True` to keep the main game loop running.
   - Initialize a variable `i` to `0` to keep track of the player’s score.

2. **Define Function for Guessing**:
   - Create a function `highlow(a_dict, b_dict, i)` that:
     - Prompts the player to guess which option has more followers, either `A` or `B`.
     - Based on the player’s choice, sets the `guess` variable to `a_dict` or `b_dict`, and the `other` variable to the remaining choice.
     - Calls the `guessing` function to verify the player’s guess.

3. **Main Game Loop**:
   - Import the data from `day_14_data`.
   - Randomly select a data item (`a_dict`) and display its name, description, and country.
   - Randomly select a second data item (`b_dict`) and check that it’s not the same as `a_dict`.
   - Display the details for both choices: "Compare A" and "Against B".
   - Prompt the player to guess which item has more followers, either `A` or `B`.
   - Based on the guess, set the variables `guess` and `other` and call the `guessing` function.

4. **Define Guess Validation Function**:
   - Create a function `guessing(guess, other, i)` that:
     - Compares the follower count of `guess` and `other`.
     - If the guess is correct (i.e., `guess["follower_count"] >= other["follower_count"]`):
       - Increment the score (`i`), display the updated score, and randomly select a new `b_dict` to compare against.
       - Display details of the new pair and call `highlow` again with the updated score.
     - If the guess is incorrect:
       - Display the final score.
       - Ask if the player wants to play again:
         - If yes, return `True` to restart the game.
         - If no, display a thank-you message and return `False` to end the game.

5. **Run the Game**:
   - Start the game loop with `game=guessing(guess, other, i)`, allowing the player to continue guessing until they choose to stop.


# PROJECT TITLE: Password Generator (Project Number: 6)

## Algorithm

1. **Define Character Pools**:
   - Create lists of characters for different categories:
     - `letters`: Contains lowercase alphabet characters from 'a' to 'z'.
     - `symbols`: Includes special characters like `!`, `@`, `$`, `#`.
     - `number`: Contains numeric characters from '0' to '9'.

2. **Get User Input**:
   - Prompt the user to input the desired number of letters, symbols, and numbers for the password:
     - `n_letters`: The number of letters.
     - `n_symbols`: The number of symbols.
     - `n_numbers`: The number of numbers.

3. **Generate Password Components**:
   - Initialize an empty list `password_list` to store the characters of the password.

   - **Add Letters**:
     - Use a loop to randomly select `n_letters` characters from `letters`, adding each selected character to `password_list`.

   - **Add Numbers**:
     - Use a loop to randomly select `n_numbers` characters from `number`, adding each selected character to `password_list`.

   - **Add Symbols**:
     - Use a loop to randomly select `n_symbols` characters from `symbols`, adding each selected character to `password_list`.

4. **Randomize Password Order**:
   - Use `random.shuffle(password_list)` to randomize the order of the characters in `password_list`.

5. **Convert to String**:
   - Initialize an empty string `password`.
   - Concatenate each character in `password_list` to `password`.

6. **Display Password**:
   - Print the generated password.


# PROJECT TITLE: Coffee Machine Simulation (Project Number: 7)

## Algorithm:

1. **Define Menu and Resources**:
   - Define a `MENU` dictionary containing coffee options (espresso, latte, cappuccino), each with required ingredient quantities and cost.
   - Define a `resources` dictionary with available amounts of `water`, `milk`, `coffee`, and `money`.

2. **Start Coffee Machine**:
   - Set a variable `machine` to `"on"` to keep the machine running.
   - Enter a `while` loop that runs while `machine` is `"on"`.

3. **Prompt User for Coffee Choice**:
   - Ask the user to choose an option (`espresso`, `latte`, `cappuccino`, `report`, or `off`).
   - If the choice is `"report"`, print current `resources`.
   - If the choice is `"off"`, set `machine` to `"off"` to exit the loop.

4. **Handle Coffee Selection**:
   - Based on the user’s choice (`espresso`, `latte`, or `cappuccino`), retrieve the corresponding coffee configuration from `MENU` and pass it to the `compare` function along with `resources` and the selected coffee (`trail`).

5. **Compare Resources** (`compare` function):
   - Check if `resources` contain enough ingredients (`water`, `coffee`, and `milk`) to make the selected coffee.
      - If all resources are sufficient, call the `coins_collector` function.
      - If any resource is insufficient, print a message indicating the shortage and return to the main loop.

6. **Collect Coins** (`coins_collector` function):
   - Prompt the user to insert coins (`quarters`, `dimes`, `nickels`, `pennies`) and calculate the total `coins_collected`.
   - If `coins_collected` is greater than or equal to the coffee’s cost:
      - Calculate and display `change` (difference between `coins_collected` and coffee cost).
      - Deduct required ingredients from `resources`.
      - Add coffee’s cost to `resources["money"]`.
      - Print a message confirming the transaction and providing the selected coffee to the user.
   - If `coins_collected` is insufficient, display an error message and refund.

7. **Loop Back or Exit**:
   - The program loops back to allow the user to select another coffee option or turn off the machine.

  # Project Title: Coffee Machine(By using OOP's concept) (Project Number: 8)

## Overview
This Coffee Machine program simulates a coffee vending machine, allowing users to select a drink, process payments, and check resource availability.

---

## Algorithm

1. **Import Modules and Classes**
   - Import `MenuItem` and `Menu` from `menu`.
   - Import `CoffeeMaker` from `coffee_maker`.
   - Import `MoneyMachine` from `money_machine`.

2. **Initialize Machine Components**
   - Create an instance of `CoffeeMaker` called `coffee_machine` to manage coffee resources.
   - Create an instance of `MoneyMachine` called `money_machine` to handle payment processing.
   - Create an instance of `Menu` called `menu` to manage drink options.

3. **Set Up Main Loop**
   - Initialize a boolean variable `is_on` and set it to `True` to keep the machine running until the user chooses to stop.

4. **User Input**
   - Use a loop to continuously prompt the user for input:
     - Retrieve the list of drink options from `menu.get_items()`.
     - Ask the user to input their choice (e.g., coffee type or commands like "off" or "report").

5. **Process User Input**
   - If the user inputs "off":
     - Set `is_on` to `False` to turn off the machine.
   - If the user inputs "report":
     - Call `coffee_machine.report()` to print available resources.
     - Call `money_machine.report()` to print the current earnings.

6. **Process Drink Order**
   - If the user inputs a valid drink name:
     - Find the drink using `menu.find_drink(order)`.
     - Check if resources are sufficient using `coffee_machine.is_resource_sufficient(is_there)`.
     - If resources are sufficient:
       - Prompt for payment using `money_machine.make_payment(is_there.cost)`.
       - If payment is successful, call `coffee_machine.make_coffee(is_there)` to make the drink.
     - If payment fails, notify the user that funds are insufficient.
   - If resources are insufficient, notify the user that the order can't be completed.

# Project Title: Quiz Game (Project Number: 9)

## Overview
This is a simple quiz game that reads questions from a data source, presents them one by one, and keeps track of the player's score based on correct answers.

---

## Algorithm

1. **Import Modules and Classes**
   - Import the `Question` class from `question_model`.
   - Import `question_data` from `data`, which holds the question and answer data.
   - Import the `QuizBrain` class from `quiz_brain` to manage the flow of the quiz.

2. **Create Question Bank**
   - Initialize an empty list called `question_bank` to store `Question` objects.
   - For each dictionary in `question_data`:
     - Retrieve the `text` and `answer` fields.
     - Create a new `Question` object using the retrieved text and answer.
     - Append the `Question` object to `question_bank`.

3. **Initialize QuizBrain Object**
   - Create an instance of `QuizBrain`, passing `question_bank` to initialize it with the question list.

4. **Run Quiz**
   - Start the quiz by calling `quiz.next_question()`, which:
     - Presents each question in sequence.
     - Accepts user input for each question.
     - Checks if the user’s answer is correct and updates the score if it is.

5. **End of Quiz**
   - After all questions are asked, the program will display the final score and indicate the end of the quiz.
  

# Project Title: Turtle Racing Game (Project Number: 10)

This project is a fun, interactive turtle racing game using Python’s Turtle graphics library. Players can place bets on which colored turtle they think will win the race, and then watch to see if their chosen turtle reaches the finish line first.

## Algorithm

1. **Setup Game Environment**:
   - Import required libraries (`turtle`, `random`) and create a screen for the game.
   - Configure the screen dimensions to 500 pixels wide and 400 pixels high.

2. **Get User's Bet**:
   - Prompt the player to enter their bet on the turtle color they believe will win, using `textinput`.
   - Store the player's input in a variable `win`.

3. **Initialize Turtle Objects**:
   - Define two lists:
     - `colours`: A list of six colors for each turtle.
     - `list1`: Contains y-coordinates to position each turtle in a unique starting lane.
   - Use a loop to:
     - Create six turtle objects, each with a color from the `colours` list.
     - Set each turtle's shape to "turtle" and move each one to its starting position using `penup()` and `goto()`.
     - Append each turtle object to the `all_turtles` list for easy reference.

4. **Start Race**:
   - If the player has made a bet, set `is_game_on` to `True` to start the race.

5. **Race Simulation Loop**:
   - Run a loop while `is_game_on` is `True`:
     - For each turtle in `all_turtles`:
       - Check if the turtle has crossed the finish line (x-coordinate > 230):
         - If a turtle crosses the finish line, stop the game by setting `is_game_on` to `False`.
         - Save the winning turtle’s color to `winning_colour`.
         - Check if `winning_colour` matches the player's bet:
           - If they match, display a message indicating the player won.
           - If they don’t match, display a message indicating the player lost.
         - Exit the loop to end the race.
       - If no turtle has crossed the finish line, move each turtle a random distance between 0 and 10 pixels.

6. **Exit on Click**:
   - Keep the turtle graphics window open until the player clicks on the screen to close it.



# Project Title:Snake Game (Project Number : 11)

## Project Overview
This project implements a classic **Snake Game** using Python's `turtle` module. The game includes a moving snake, randomly generated food, and a scoring system. The player controls the snake to eat food, grow in length, and avoid collisions with the walls or itself.

---

## Algorithm

 1. **Initialize the Game**
   - Import necessary modules (`Turtle`, `Screen`, `time`, and custom classes: `Food`, `Snake`, and `Score`).
   - Set up the screen:
     - Background color: black.
     - Dimensions: 600x600 pixels.
     - Title: "Snake Game".
     - Use `screen.tracer(0)` to turn off automatic screen updates for smoother animations.
   - Create instances of:
     - `Snake` for the snake's movement.
     - `Food` to generate random food positions.
     - `Score` to manage the score display.



 2. **Setup User Controls**
   - Use `screen.listen()` to capture keyboard events.
   - Map the `Up`, `Down`, `Left`, and `Right` keys to the snake's movement methods (`snake.up`, `snake.down`, `snake.left`, `snake.right`).

---

 3. **Main Game Loop**
   - Start the game loop with a `while` loop controlled by a `is_game_on` flag.
   - Inside the loop:
     - Call `screen.update()` to refresh the screen.
     - Pause for a short time using `time.sleep(0.1)` to control the speed of the snake.

 **Logic within the Loop**
1. **Move the Snake**:
   - Call `snake.move()` to move all segments of the snake.

2. **Detect Food Collision**:
   - Check if the snake's head is within 14 units of the food using `snake.head_snake.distance(food)`.
   - If true:
     - Call `food.another_food()` to relocate the food.
     - Call `snake.extend()` to add a new segment to the snake.
     - Update the score using `scoreboard.score_increase()`.

3. **Detect Wall Collision**:
   - Check if the snake's head exceeds the screen's boundaries (±290 units).
   - If true:
     - Set `is_game_on` to `False`.
     - Display "Game Over" using `scoreboard.game_over()`.

4. **Detect Self-Collision**:
   - Iterate through all snake segments except the head.
   - Check if the head's distance to any segment is less than 10 units.
   - If true:
     - Set `is_game_on` to `False`.
     - Display "Game Over" using `scoreboard.game_over()`.

---

 4. **Exit the Game**
   - Use `screen.exitonclick()` to wait for the user to click before closing the screen.

---

## File Structure
- **`snake.py`**: Contains the `Snake` class for managing the snake's creation, movement, and growth.
- **`food.py`**: Contains the `Food` class for generating food at random positions.
- **`score.py`**: Contains the `Score` class for tracking and displaying the score.



# PROJECT TITLE: Pong Game (Project Number: 12)

# Overview

The provided code implements a basic **Pong Game** using Python's `turtle` module. It creates an interactive game with paddles, a ball, and a scoring system. The game features:
- Two paddles controlled by the user via keyboard inputs.
- A ball that bounces off walls, paddles, and resets when missed.
- A scoring mechanism to track each player's points.
- A graphical interface with smooth motion and collision detection.


---

# Algorithm

## 1. **Setup**
   - **Step 1.1:** Import necessary modules: `time`, `Screen`, `Ball`, `Paddle`, and `Score`.
   - **Step 1.2:** Initialize the screen:
     - Set title as `"PONG GAME"`.
     - Set dimensions: `800x600 pixels`.
     - Set background color to black.
     - Disable automatic updates using `tracer(0)` to manually control rendering.

## 2. **Create Game Objects**
   - **Step 2.1:** Create the paddles:
     - Right paddle at `(350, 0)`.
     - Left paddle at `(-350, 0)`.
   - **Step 2.2:** Create score objects:
     - Right score tracker at `(100, 200)`.
     - Left score tracker at `(-100, 200)`.
   - **Step 2.3:** Create a ball object for movement and collision.

## 3. **Define Controls**
   - **Step 3.1:** Set key bindings for right paddle:
     - Move up with the "Up" arrow key.
     - Move down with the "Down" arrow key.
   - **Step 3.2:** Set key bindings for left paddle:
     - Move up with the "W" key.
     - Move down with the "S" key.

## 4. **Game Loop**
   - **Step 4.1:** Start the game loop (`while game_on`):
     - Pause execution using `time.sleep()` based on the ball's speed.
     - Update the screen with `screen.update()`.

   ### 4.2. Ball Movement
   - Move the ball using its `mov()` method.

   ### 4.3. Detect Wall Collisions
   - If the ball's vertical position (`ycor`) exceeds `280` or is less than `-280`:
     - Reverse the ball's vertical direction with `bounce_y()`.

   ### 4.4. Detect Paddle Collisions
   - Check proximity between the ball and each paddle:
     - For the right paddle:
       - If the ball's distance from the paddle is less than `50` and its horizontal position (`xcor`) exceeds `320`, reverse its direction using `bounce_x()`.
     - For the left paddle:
       - If the ball's distance from the paddle is less than `50` and its horizontal position (`xcor`) is less than `-340`, reverse its direction using `bounce_x()`.

   ### 4.5. Detect Missed Ball
   - **Step 4.5.1:** Detect right paddle miss:
     - If the ball's horizontal position (`xcor`) exceeds `380`:
       - Reset the ball to the center using `centre()`.
       - Increment the left player's score with `l_point()`.
   - **Step 4.5.2:** Detect left paddle miss:
     - If the ball's horizontal position (`xcor`) is less than `-380`:
       - Reset the ball to the center using `centre()`.
       - Increment the right player's score with `r_point()`.

## 5. **End Game**
   - Exit the game loop upon user termination and close the screen with `screen.exitonclick()`.

---


# PROJECT TITLE: Turtle Cross Game (Project Number: 13)

## Introduction

The Turtle Cross game involves a player controlling a turtle that tries to cross a road filled with moving cars. The goal is to reach the other side without colliding with any cars. The game gets progressively harder as the player progresses.

---

## Steps in the Algorithm

### 1. **Initialize Game Components**

- Import required modules (`time`, `Screen`, and custom classes `Player`, `CarManager`, `Scoreboard`).
- Create instances for:
  - `Player` to represent the turtle.
  - `CarManager` to handle car creation and movement.
  - `Scoreboard` to display the player's score.

### 2. **Set Up Screen**

- Create a `Screen` instance:
  - Set the title to "Turtle Cross."
  - Configure the dimensions (`600x600`) and background color (`black`).
  - Disable automatic updates using `screen.tracer(0)`.
- Enable key listeners to move the player using the "Up" arrow key.

### 3. **Start Game Loop**

- Initialize `game_is_on` to `True`.
- Run the game loop as long as `game_is_on` is `True`:

#### Inside the Loop:

1. **Update Screen and Pause:**

   - Pause the loop briefly using `time.sleep(0.1)` to control game speed.
   - Update the screen.

2. **Display Score:**

   - Update the scorecard using `score.scorecard()`.

3. **Manage Cars:**

   - Create new cars with `car.create_cars()`.
   - Move all cars forward with `car.move_cars()`.

4. **Detect Collisions:**

   - Loop through all cars in `car.all_cars`.
   - Check if the distance between the player and a car is less than 15 units.
   - If a collision is detected:
     - End the game by setting `game_is_on` to `False`.
     - Trigger the `player.lost()` method to display a losing message or effect.

5. **Check Win Condition:**

   - Check if the player has reached the other side of the screen using `player.reach()`.
   - If the player wins:
     - Reset the player's position to the starting point using `player.go_to_start()`.
     - Increase car movement speed with `car.movement_increase()`.
     - Clear the previous score and increment the level using `score.clear()` and `score.lvl_increament()`.

### 4. **End Game**

- Exit the game when the loop ends by calling `screen.exitonclick()`.

---



