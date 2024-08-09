# Stanley Result Timer

Stanley Result Timer is a simple Vue.js application designed to measure the reaction time of users. The app presents a card to the user after a random delay, and the user has to click on the card as quickly as possible. The app then calculates and displays the reaction time along with a ranking based on performance.

## Features

- **Randomized Delay**: The app introduces a delay between 2 and 7 seconds before displaying the card to be clicked.
- **Reaction Time Measurement**: Calculates the time taken for the user to react to the appearance of the card.
- **Ranking System**: Based on the user's reaction time, the app assigns a rank:
  - "Ninja Fingers" for reaction times under 250 ms.
  - "Rapid Reflexes" for reaction times between 250 ms and 400 ms.
  - "Snail Pace..." for reaction times above 400 ms.

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/stanleywanjau/reaction-time-vuejs
    cd stanley-result-timer
    ```

2. Install the dependencies:
    ```bash
    npm install
    ```

3. Start the development server:
    ```bash
    npm run serve
    ```

4. Open your browser and navigate to `http://localhost:8080`.

## Usage

1. Click the **Play** button to start the game.
2. Wait for the card to appear on the screen.
3. Click on the card as quickly as possible.
4. Your reaction time will be displayed, along with your rank.

## Components

- **App.vue**: The main component that handles the game state.
- **BlockView.vue**: Displays the card and measures the reaction time.
- **ResultView.vue**: Displays the user's reaction time and rank.

## Project Structure

├── public
├── src
│   ├── assets
│   ├── components
│   │   ├── BlockView.vue
│   │   └── ResultView.vue
│   ├── App.vue
│   ├── main.js
├── package.json
├── README.md
└── vue.config.js


markdown
Copy code

## Customization

- **Delay Time**: You can adjust the random delay time in the `start` method inside `App.vue`.
- **Ranking Criteria**: Modify the conditions in `ResultView.vue` to change the ranking criteria.

## Contributing

Feel free to fork this project and submit a pull request with your improvements.

## License

This project is licensed under the MIT License.