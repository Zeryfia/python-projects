## Snake Game Documentation

The Snake Game is a simple implementation of the classic snake game using the Tkinter library in Python. The objective of the game is to control a snake on the screen, eat food to grow in length, and avoid colliding with itself or the boundaries of the game window.

### Game Elements

#### Snake Class

The `Snake` class represents the snake in the game. It is initialized with the following attributes:

- `body_size`: An integer representing the initial size of the snake.
- `coordinates`: A list that holds the (x, y) coordinates of each part of the snake's body.
- `squares`: A list that stores the graphical representations (squares) of the snake's body on the canvas.

#### Food Class

The `Food` class represents the food that appears on the game canvas. It is initialized with the following attribute:

- `coordinates`: A list that holds the (x, y) coordinates of the food item.

### Game Functions

#### `next_turn(snake, food)`

This function is responsible for handling the snake's movement and checking for collisions with food or the game boundaries. It takes `snake` and `food` objects as arguments.

#### `change_direction(new_direction)`

This function is triggered when the player presses one of the arrow keys (up, down, left, right). It changes the direction of the snake based on the input and restricts the snake from turning back on itself.

#### `check_collisions(snake)`

This function checks for collisions between the snake's head and its body parts or the game boundaries. It returns `True` if a collision occurs and `False` otherwise.

#### `game_over()`

This function is called when the game is over, i.e., when the snake collides with itself or the game boundaries. It displays a "GAME OVER" message on the canvas and asks the player if they want to play again. If the player chooses to play again, it resets the game; otherwise, it closes the game window.

#### `play_again()`

This function is called when the player chooses to play again after the game is over. It resets the game state, including the snake's position, food position, score, and direction.

### Game Variables

The following variables control various aspects of the game:

- `GAME_WIDTH`: Width of the game canvas in pixels.
- `GAME_HEIGHT`: Height of the game canvas in pixels.
- `SPEED`: Time delay in milliseconds between each move of the snake.
- `SPACE_SIZE`: Size of each square space on the canvas.
- `BODY_PARTS`: Initial size of the snake.
- `SNAKE_COLOR`: Color of the snake's body.
- `FOOD_COLOR`: Color of the food item.
- `BACKGROUND_COLOR`: Background color of the game canvas.

### User Interface

The game is displayed using a Tkinter window with a canvas for drawing the game elements. The score is displayed at the top of the window using a `Label` widget.

The arrow keys are bound to the `change_direction` function to control the snake's movement.

### How to Play

1. Run the Python script, and a window will appear with the snake game.
2. The snake will start moving downwards by default.
3. Use the arrow keys (up, down, left, right) to change the snake's direction.
4. The objective is to eat the food (red oval) that appears randomly on the canvas to grow the snake's length.
5. The game ends if the snake collides with itself or hits the game boundaries.
6. When the game is over, a message box will ask if you want to play again.
7. If you choose to play again, the game will be reset; otherwise, the window will close.

Enjoy playing the Snake Game!
