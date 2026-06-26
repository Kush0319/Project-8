📊 NumPy Analyzer Toolkit

## 📌 Project Objective
The **NumPy Analyzer** is a Python-based, menu-driven toolkit that integrates NumPy functionalities with Object-Oriented Programming (OOP) principles. It empowers users to perform a wide range of data operations, statistical analyses, and mathematical computations on datasets using NumPy arrays through an interactive console interface.

---

## 🚀 Features & Capabilities

This toolkit is modularized into several core functionalities encapsulated within the `DataAnalytics` class:

### 1. Array Management
*   **Creation**: Dynamically generate 1D, 2D, or 3D arrays based on user-defined dimensions and elements.
*   **Combination**: Vertically stack (combine) an existing array with a new array of matching dimensions.
*   **Splitting**: Divide an array into multiple smaller, equal-sized sub-arrays.

### 2. Mathematical Operations
Perform element-wise computations between arrays of identical shapes:
*   Addition
*   Subtraction
*   Multiplication
*   Division
*   **Dot Product**: Computes the matrix multiplication (strictly for 2D arrays).

### 3. Search, Sort, and Filter
*   **Search**: Find specific values and return their exact indices within the array structure.
*   **Sort**: Flatten and sort the array elements in ascending order.
*   **Filter**: Extract elements that meet specific user-defined conditions (e.g., values greater than a certain threshold).

### 4. Aggregates and Statistics
Compute deep statistical properties of the active dataset:
*   Sum, Mean, Median
*   Standard Deviation & Variance
*   Minimum & Maximum values
*   Percentiles (user-defined, 0-100)
*   Correlation Coefficient (for 2D arrays)

---

## 🛠️ Object-Oriented Programming (OOP) Concepts Utilized

This project adheres strictly to OOP best practices to maintain clean, scalable, and robust code:
*   **Classes & Objects**: The entire application runs through an instance of the `DataAnalytics` class.
*   **Constructors (`__init__`)**: Safely initializes the main array state (`self.main_array = None`) upon object creation.
*   **Encapsulation (Private Methods)**: Utilizes `__is_array_created()` to internally validate if an array exists before allowing operations, preventing crash-inducing errors.
*   **Class Methods (`@classmethod`)**: Accesses class-level attributes to display overarching project metadata (e.g., `display_project_info()`).
*   **Static Methods (`@staticmethod`)**: Handles utility functions independent of the class state, such as console UI formatting (`print_separator()`).

---

## 📋 Assumptions Made

As per the project instructions, the following assumptions were made during development:
1.  **Data Types**: All array elements inputted by the user are assumed to be integers (`int`). Floating-point inputs will raise a `ValueError` in the current iteration to keep the beginner-level scope clean.
2.  **Dimensional Matching**: For mathematical operations (Addition, Subtraction, etc.), it is assumed the user will input elements that perfectly match the shape of the initially created array. (Basic `try-except` blocks are included to catch shape mismatches).
3.  **Dot Product Dimensions**: The dot product specifically validates for 2D arrays, as dot products on 1D or 3D arrays behave differently (inner vs tensor products) and fall outside standard matrix multiplication scope.
4.  **Sorting Output**: Sorting operations flatten the array prior to sorting and return a 1D sorted array, which is standard behavior for `np.sort(axis=None)`.
5.  **Console Limitations**: Array inputs are space-separated strings handled in a single line. It is assumed the datasets being tested are small enough to be manually typed into the terminal.

---

## 💻 Installation & Usage

### Prerequisites
*   Python 3.x installed on your machine.
*   The `numpy` library. 

### Setup Instructions
1.  Clone this repository to your local machine:
    ```bash
    git clone <your-github-repo-link>
    ```
2.  Install the required dependencies:
    ```bash
    pip install numpy
    ```
3.  Run the Python script:
    ```bash
    python numpy_analyzer.py
    ```
    *(Note: If you are using Google Colab, simply run the cells sequentially).*

### Example Interaction
Upon running the program, you will be greeted by the main menu:
```text
--- NumPy Analyzer Toolkit ---
========================================
Welcome to the NumPy Analyzer!
========================================

Choose an option:
1. Create a Numpy Array
2. Perform Mathematical Operations
3. Combine or Split Arrays
4. Search, Sort, or Filter Arrays
5. Compute Aggregates and Statistics
6. Exit
