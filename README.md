# Tic Tac Toe

> You can play Tic-Tac-Toe with this application. My purpose was to only build it with Javascript. There are no global variables. Almost every method is single responsible. 

## Live Demo

[Live Demo Link](https://rawcdn.githack.com/kubilaycaglayan/tic-tac-toe-js/fcac74cfe0a3afc07899fbc84834747b63b76b7b/tictactoe.html)

![screenshot](./images/ttt.png)

### How To Remove Event Listeners?

> I am storing event listeners in an array at the moment of creation.
> When I want to remove them, I am using that array to address them.


## Here is my modules, their public properties and responsibilities:

#### NewBoard
> Responsibility: generates a new board.
- board

#### GameBoard
> Responsibility: Checks the spot and makes the move. Other modules can ask these questions to this module: (-Who's turn is it? -What is the state of the board? -Can you reset board? -Can you make this move?)
- getBoard
- move
- getTurn
- resetBoard

#### GamePlay
> Responsibility: It tries to make the move and returns one of the followings: (-true: means the move was successful and game is still going on , -tie, -player1 won, -player2 won, -false: means move is not possible)
- moveAndCheck

#### BoardListener
> Responsibility: Changes the visual of the squares on click. This module has no idea who's turn is it. It gets this information from GameBoard module.
- changeSquare

#### PlayOnPage
> Responsibility: All the eventlisteners, message feedback system and game engine is in this module. By using other modules API(public methods)s, PlayOnPage creates a user interface which makes it possible to play this game with mouse clicks. `If this module wouldn't exist, you could still play the game with moveAndCheck method in the GamePlay module with the help of the console. Try it! GamePlay.moveAndCheck(index you want to make your move)` 
- `returns nothing`

## Built With

- HTML
- CSS
- JAVASCRIPT
- BOOTSTRAP
- SASS

## Getting Started

### Usage

- Click the Live Demo link and enjoy my website.

### Prerequisites

- A modern browser, up to date.

### Run tests

- There is no automated tests for this project.

### Future Features

- Ability to play across the internet with your friends.

## Author

👤 **Kubilay Caglayan**

- Website: [kubilay](https://kubilaycaglayan.com)
- Github: [@kubilaycaglayan](https://github.com/kubilaycaglayan)
- Twitter: [@kbcaglayan](https://twitter.com/kbcaglayan)
- Linkedin: [linkedin](https://linkedin.com/in/kubilaycaglayan)

## 🤝 Contributing

Contributions, issues and feature requests are welcome!

Feel free to check the [issues page](https://github.com/kubilaycaglayan/library/issues).

## Show your support

Give a ⭐️ if you like this project!

## Acknowledgments

- https://www.theodinproject.com/courses/javascript/lessons/library

## 📝 License

This project is [MIT](LICENCSE) licensed.
