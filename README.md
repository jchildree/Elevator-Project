# Elevator Simulation

## Overview
This script will simulate an elevator's travel time, as it moves through different floors. The program calculates the total time required for the elevator's journey based on the number of floors visited and the time taken to travel between each floor. It also tracks the order the floors are visited. The system output will display the total time required to visit all specified floors and the sequence in which they were visited.

## Features:
- Computes total travel time based on the number of floors visited.
- Tracks the sequence of visited floors.
- Handles user input errors gracefully.
- Provides a simple command-line interface.

## Requirements:
- Python 3.x

## Usage:
To run the script, use the following command:
```sh
python elevator.py <start_floor> <floor1,floor2,...>
```

### Arguments:
- `<start_floor>`: The floor from which the elevator starts its journey (integer).
- `<floor1,floor2,...>`: A comma-separated list of floors to visit in order (e.g., `2,5,8`).

### Example:
```sh
python elevator.py 1 5,3,10
```

### Output:
The script will output the total travel time in seconds and the order of floors visited.
```
Total Travel Time: 130 seconds
Visited Floors: 1, 5, 3, 10
```

### Calculation Explanation:
The script calculates travel time using a fixed time of **10 seconds per floor**:
1. **From Floor 1 to Floor 5:**
   - Distance: `|5 - 1| = 4 floors`
   - Time: `4 * 10 = 40 seconds`
2. **From Floor 5 to Floor 3:**
   - Distance: `|3 - 5| = 2 floors`
   - Time: `2 * 10 = 20 seconds`
3. **From Floor 3 to Floor 10:**
   - Distance: `|10 - 3| = 7 floors`
   - Time: `7 * 10 = 70 seconds`
4. **Total Time:** `40 + 20 + 70 = 130 seconds`

## How it works:
1. The script calculates travel time using a fixed **10 seconds per floor**.
2. It keeps track of the order of floors visited.
3. The result is printed in the format:
   ```
   Total Travel Time: <time> seconds
   Visited Floors: <floor_order>
   ```

## Error Handling:
- If the script is run with missing arguments, it will display an error message:
  ```
  Error: Usage: python elevator.py <start_floor> <floor1,floor2,...>
  ```
- If invalid (non-numeric) input is provided, the script will notify the user and exit safely.

## Assumptions:
- The elevator always moves directly from one floor to the next in the provided order.
- The time to travel between any two sequential floors is a fixed **10 seconds**.
- Negative floors (e.g., basements) are allowed as long as they are valid integers.

## Future Enhancements:
- Add the ability to customize the travel time per floor.
- Implement handling for traveling to a specific floor.
- Implement calculations for wait times at each floor.
- Improve input validation for better error handling.

## Purpose:
Developed for an interview project, to be used to demonstrate my Python scripting and algorithm implementations for simulation-based calculations.
