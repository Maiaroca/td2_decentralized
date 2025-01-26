# td2_decentralized
# Tic-Tac-Toe Game

This repository contains a simple Tic-Tac-Toe game built using HTML, CSS, and JavaScript. The game allows two players to play against each other in turns. The repository also includes a GitHub Actions workflow for deploying the project to Pinata, a decentralized file storage platform based on IPFS.

---

## Features

- Interactive Tic-Tac-Toe game board.
- Highlights the winner or announces a draw when the game ends.
- Ability to restart the game at any time.
- Automated deployment to Pinata via GitHub Actions.

---

## How to Use

### Locally
1. Clone the repository:
   ```bash
   git clone <repository-url>
   ```

2. Navigate to the repository directory:
   ```bash
   cd <repository-folder>
   ```

3. Open `index.html` in your web browser to play the game.

---

## Deployment

The project is automatically deployed to Pinata using the provided `deploy.yml` GitHub Actions workflow. Follow these steps to enable deployment:

### Requirements

1. Create a Pinata account at [Pinata](https://pinata.cloud/).
2. Generate your Pinata API Key and Secret Key from the Pinata dashboard.
3. Add the following secrets to your GitHub repository:
   - `PINATA_API_KEY`
   - `PINATA_SECRET_API_KEY`

### Workflow

The workflow is triggered on every push to the `main` branch. The key steps include:

1. Checking out the code.
2. Deploying the contents of the `src` folder to Pinata.
3. Pinning the files to ensure they remain accessible on IPFS.

To manually trigger the deployment, ensure your changes are pushed to the `main` branch:
```bash
git push origin main
```

---

## File Structure

```
.
├── .github/workflows/deploy.yml   # GitHub Actions workflow for Pinata deployment
├── README.md                      # Documentation for the repository
└── src/index.html                 # Main HTML file for the Tic-Tac-Toe game
```

---

## Technologies Used

- **HTML**: Markup for the game interface.
- **CSS**: Styling for the game board and buttons.
- **JavaScript**: Game logic, player interactions, and winner detection.
- **GitHub Actions**: CI/CD pipeline for Pinata deployment.
- **Pinata**: Decentralized storage platform for hosting the game files.

---

## How to Play

1. Open the game in a browser.
2. Players take turns clicking on the cells of the 3x3 grid to place their markers (X or O).
3. The first player to align three of their markers horizontally, vertically, or diagonally wins.
4. If all cells are filled without a winner, the game declares a draw.
5. Use the "Recommencer" button to restart the game.

---

## License

This project is licensed under the MIT License. See the LICENSE file for details.

---

## Contributing

Contributions are welcome! Feel free to open an issue or submit a pull request if you have suggestions or improvements.

---

## Acknowledgments

- [Pinata](https://pinata.cloud/) for providing decentralized file storage solutions.
- GitHub Actions for simplifying CI/CD workflows.
- Everyone who contributed feedback and suggestions for this project.
