# Python_projects
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


