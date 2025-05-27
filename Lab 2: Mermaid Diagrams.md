# 🎯 Random Guessing Game Flowchart

```mermaid
flowchart TD
    Start([Start]) --> Init[Initialize game variables\nSet min and max values]
    Init --> Generate[Generate random number within range]
    Generate --> Prompt[Prompt user to enter a guess]
    Prompt --> Validate{Is input a number?}
    Validate -- No --> Error[Display error and re-prompt]
    Error --> Prompt
    Validate -- Yes --> Compare{Is guess equal to random number?}
    Compare -- Yes --> Correct[Display "Correct!"]
    Correct --> End([End])
    Compare -- No --> HighLow{Is guess > or < number?}
    HighLow -- Greater --> High[Display "Too high"]
    HighLow -- Less --> Low[Display "Too low"]
    High --> Prompt
    Low --> Prompt
