# Euclidean Distance Calculator

## Overview
This Python project calculates the Euclidean distance between two points in an n-dimensional space. The program is simple yet powerful, and it serves as a handy tool for mathematical computations, machine learning preprocessing, or geometry-related applications.

## Features

### 1. **Support for n-Dimensional Space**
- Handles points in 2D, 3D, and higher dimensions seamlessly.
- Allows for custom input dimensions via lists or tuples.

### 2. **Input Validation**
- Ensures that both points have the same number of dimensions.
- Provides clear error messages for invalid inputs.

### 3. **Reusable Functionality**
- Exposes a `calculate_distance` function for integration with larger projects.

## File Structure
```
euclidean_distance_calculator/
├── main.py        # Main Python script
├── README.md      # Project documentation
└── requirements.txt # Dependencies (if any are added in future)
```

## Technologies Used
- **Python 3**: The core programming language for this project.
- **Math Module**: For square root and mathematical operations.

## Usage Instructions

### Prerequisites
- Ensure Python 3.x is installed on your system.

### Steps to Run
1. Clone the repository or download the `main.py` file.
2. Open a terminal and navigate to the project directory.
3. Run the script:
   ```bash
   python main.py
   ```
4. Enter the coordinates of the two points when prompted.

### Example
For two points in 3D space, (1, 2, 3) and (4, 5, 6):

```text
Enter the coordinates of the first point (comma-separated): 1, 2, 3
Enter the coordinates of the second point (comma-separated): 4, 5, 6
The Euclidean distance is: 5.196152422706632
```

## Customization
- Modify `main.py` to add more features, such as:
  - Support for batch processing of multiple point pairs.
  - Integration with a graphical user interface (GUI).

## Example Function
```python
def calculate_distance(point1, point2):
    """
    Calculate the Euclidean distance between two points in n-dimensional space.

    Args:
        point1 (list or tuple): Coordinates of the first point.
        point2 (list or tuple): Coordinates of the second point.

    Returns:
        float: Euclidean distance.
    """
    if len(point1) != len(point2):
        raise ValueError("Both points must have the same number of dimensions.")
    return math.sqrt(sum((x - y) ** 2 for x, y in zip(point1, point2)))
```

## Future Enhancements
- Add a web-based interface using Flask or Django.
- Integrate with scientific libraries like NumPy for enhanced performance.
- Provide visualization of the points and distance in 2D or 3D space.

## License
This project is distributed under the MIT License. Feel free to use and modify it for personal or educational purposes.
