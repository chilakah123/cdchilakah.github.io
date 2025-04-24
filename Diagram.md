flowchart TD
    A[Start] --> B[/Input: numbers array/]
    B --> C[out = numbers.size - 1]
    C --> D{out >= 0?}
    D -->|Yes| E[in = 1]
    D -->|No| K[out = 0]
    E --> F{in <= out?}
    F -->|Yes| G{numbers[in-1] > numbers[in]?}
    F -->|No| J[out = out - 1]
    G -->|Yes| H[temp = numbers[in-1]<br>numbers[in-1] = numbers[in]<br>numbers[in] = temp]
    G -->|No| I[in = in + 1]
    H --> I
    I --> F
    J --> D
    K --> L{out < numbers.size?}
    L -->|Yes| M[Output numbers[out]<br>Output space]
    L -->|No| N[End]
    M --> O[out = out + 1]
    O --> L
