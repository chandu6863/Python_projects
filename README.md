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
