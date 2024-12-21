# Prime Game



For this project, you will need to leverage your understanding of prime numbers, game theory, and algorithm optimization to solve a competitive game scenario. The challenge involves determining the winner of a game based on the strategic removal of prime numbers and their multiples from a set of consecutive integers.

# Concepts Needed:
Prime Numbers:

Understanding what prime numbers are.
Efficient algorithms for identifying prime numbers within a range.
Sieve of Eratosthenes:

An efficient algorithm for finding all prime numbers up to any given limit, which can be particularly useful for this task.
Game Theory:

Basic principles of competitive games where players take turns and the concept of optimal play.
Understanding win conditions and strategies that lead to a win or loss.
Dynamic Programming/Memoization:

Using previous results to make future calculations faster, potentially necessary for optimizing the solution for multiple rounds of the game.
Python Programming:

Loops and conditional statements for implementing game logic and algorithms.
Arrays and lists for storing the integers and tracking removed numbers.
Resources:
Prime Numbers and Sieve of Eratosthenes:

Khan Academy: Prime Numbers: Introduction to prime numbers.
Sieve of Eratosthenes in Python: A step-by-step guide to implementing the sieve algorithm in Python.
Game Theory Basics:

Game Theory Introduction: A simple explanation of game theory and strategic decision-making.
Dynamic Programming:

What Is Dynamic Programming With Python Examples: An introduction to dynamic programming with Python examples.
Python Official Documentation:

Python Lists: Managing lists in Python, useful for tracking the game state.
By grasping these concepts and making use of the recommended resources, you will be well-equipped to approach the problem with a solid understanding of both the mathematical and programming challenges involved. The key to success in this project lies in applying efficient algorithms to manage the game’s state and making optimal decisions based on the game’s rules.

# procedure:
Maria and Ben are playing a game. Given a set of consecutive integers starting from 1 up to and including n, they take turns choosing a prime number from the set and removing that number and its multiples from the set. The player that cannot make a move loses the game.

They play x rounds of the game, where n may be different for each round. Assuming Maria always goes first and both players play optimally, determine who the winner of each game is.

     - Prototype: def isWinner(x, nums)
     - where x is the number of rounds and nums is an array of n
     - Return: name of the player that won the most rounds
     - If the winner cannot be determined, return None
     - You can assume n and x will not be larger than 10000
     - You cannot import any packages in this task

## My take

For each round, find the number of primes in the range 1 to num.
Since each player takes out a prime number and it's multiples, the number of available moves equals the number of prime numbers in that range (1 to num).
Since Maria always starts, then if number of primes in range is odd, Maria will have the last move, thus she wins. If number of primes is even, Ben will have the last move, thus he wins.
Track each player's number of wins for all the rounds and return player with most wins. if they have equal no. of wins, return None since a winner cannot be found.

### Edge cases

    - if x is 0 or None, a winner cannot be found. Return None.
    - if nums is None or empty, a winner cannot be found. Return None
