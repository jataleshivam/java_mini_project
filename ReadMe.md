# Simple Card Game

Hey there! 👋 Welcome to this simple card game in Java. The idea behind this little project is to simulate a card game where two players randomly draw a card, and then we compare those cards to see who wins based on the rank. It's a fun little exercise in randomization and basic comparisons. Let's dive in!

## What It Does

- **Two players** draw a card randomly from a deck.
- The deck has **four suits**: Hearts, Diamonds, Clubs, and Spades, and **13 ranks**: 2 through Ace.
- The cards are compared by their rank (not their suit), and the player with the higher-ranked card wins.
- If both players draw the same rank, the game is a **tie**.

## How It Works

1. **Card Drawing**:  
   Each player draws one random card from a deck. The deck is represented by two arrays: one for suits and one for ranks.

2. **Rank Comparison**:  
   The game compares the ranks of the two cards. Ranks are ordered from `2` (lowest) to `Ace` (highest). If Player 1 draws a higher card, they win. If Player 2 draws a higher card, they win. If both players draw the same rank, it's a tie!

3. **Game Outcome**:  
   After both players draw their cards, the program tells you who the winner is—or if it's a tie!

## Code Walkthrough

Here’s how the code is set up:

### Main Class: `SimpleCardGame`

- **Deck Setup**:  
  The deck is split into two arrays:
  - `suits` (Hearts, Diamonds, Clubs, Spades)
  - `ranks` (2, 3, 4, 5, ..., Jack, Queen, King, Ace)

- **Random Card Draw**:  
  The `Random` class is used to pick random cards for both players. Each player gets one random card.

- **Comparing Cards**:  
  The ranks of the drawn cards are compared using a method that assigns each rank a numeric value. This way, we can easily determine which card is higher.

- **Deciding the Winner**:  
  The program checks which player drew the higher card and prints the result. If both players draw the same rank, it’s a tie!

### Key Methods:
- `compareRanks(String rank1, String rank2, String[] ranks)`:  
  Compares the ranks of two cards and returns:
  - `1` if Player 1 wins,
  - `2` if Player 2 wins,
  - `0` if it's a tie.

- `getRankValue(String rank, String[] ranks)`:  
  Turns each rank (e.g., "Jack", "2", "Ace") into a number so we can compare them. For example, "2" is the smallest (rank 0) and "Ace" is the largest (rank 12).

## Example Output

Here's what the output might look like when you run the game:

