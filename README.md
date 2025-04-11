# LP1SpeedType​



## UML Diagram

```mermaid
classDiagram
    class Program {
        +static void Main(string[] args)
    }

    class Game {
        +string userInput
        +SentenceProvider sentenceProvider
        +GameResult[] gameStats
        +void StartGame()
        +void ShowMenu()
        +void ShowPrecision()
        +void ShowGameStats()
    }

    class GameResult {
        +double wpm
        +double TimeTaken
        +int accuracy
    }

    class SentenceProvider {
        +string[] sentences
        +Random random
        +string GetRandomSentence()
    }
    class Evaluator {
        +int wordsTyped
        +int correctChars
        +double CalculateWPM()
        +int CalculateAccuracy()
    }

    Program --> Game
    Game --> Evaluator
    Game --> GameResult
    Evaluator --> GameResult
    Game --> SentenceProvider