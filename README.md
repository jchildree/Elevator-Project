
# Elevator Simulation

This Python script simulates the travel time for an elevator as it moves through different floors. The program calculates the total travel time based on the number of floors the elevator visits and the time taken to travel between each floor. It also tracks the order of visited floors.

## Features:
- Calculate total travel time based on the number of floors.
- Track the order of floors visited during the elevator's journey.
- Provides command-line usage for easy input.

## Requirements:
- Python 3.x

## Usage:

To run the script, use the following command:

```bash
python elevator.py <start_floor> <floor1,floor2,...>
```

### Arguments:
- `<start_floor>`: The floor from which the elevator starts its journey (integer).
- `<floor1,floor2,...>`: A comma-separated list of floors to visit in order (e.g., `2,5,8`).

### Example:
```bash
python elevator.py 1 2,5,8
```

### Output:
The script will output the total travel time in seconds and the order of floors visited.

Example output:
```
50 1,2,5,8
```

### Example Explanation:
- The elevator starts at floor 1.
- Travels to floor 2 (10 seconds).
- Then moves from floor 2 to floor 5 (30 seconds).
- Finally, it moves from floor 5 to floor 8 (10 seconds).
- The total travel time is 50 seconds.

## How it works:
1. The script calculates the travel time based on the number of floors to be traveled to, and a fixed travel time of 10 seconds per floor.
2. It keeps track of the order of floors entered, to be visited.
3. The result is printed in the format: `total_travel_time, visited_floors`.

## Assumptions:
- The elevator always moves directly from one floor to the next, without stopping until all entered floors are reached.
- Assumes each floor is after the other, with no skipped floors (Floors: 1, 2,3, 4 = Floors: 1, 4, 8, 2).
- The time to travel between any two floors is set to a fixed 10 seconds.

## Example:
```bash
python elevator.py 3 5,1,8
```
Output:
```
50 3,5,1,8
```

## Future Enhancements:
- Add the ability to customize the travel time per floor.
- Implement handling traveling to one specific floor and the travel time (e.g., Go from Floor 1 - 30)
- Implement handling traveling back to floor 1 (Bi-directional Formatting)
- Improve input validation (e.g., non-integer inputs).


