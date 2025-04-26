# Analysis-Of-Algorithms Assignment#04
# Sorting Algorithms Performance Analysis

This project implements and compares the performance of four sorting algorithms:
- Bubble Sort
- Selection Sort
- Insertion Sort
- Merge Sort

## 📂 Project Structure
- `BubbleSorting.java`
- `SelectionSorting.java`
- `InsertionSorting.java`
- `MergeSorting.java`
- `GraphPlotting.py` (optional: if you used Python to plot the graph)

## ▶️ How to Run

1. Make sure you have Java installed (`javac --version` to check).
2. Compile the Java files:
   ```bash
   javac BubbleSorting.java
   javac SelectionSorting.java
   javac InsertionSorting.java
   javac MergeSorting.java
Run the Java programs one by one:
java BubbleSorting
java SelectionSorting
java InsertionSorting
java MergeSorting

For Graph:
pip install matplotlib numpy
import matplotlib.pyplot as plt
import numpy as np

# Data
input_sizes = [5, 10, 50, 100]

bubble_times = [0.00140, 0.00412, 0.04002, 0.15584]
selection_times = [0.00110, 0.00256, 0.04842, 0.18048]
insertion_times = [0.00124, 0.00274, 0.00570, 0.01426]
merge_times = [0.00334, 0.00588, 0.05044, 0.07732]

# Grouped bar settings
bar_width = 0.2
x = np.arange(len(input_sizes))  # [0,1,2,3]

# Create the bars
plt.bar(x - 1.5*bar_width, bubble_times, width=bar_width, label='Bubble Sort')
plt.bar(x - 0.5*bar_width, selection_times, width=bar_width, label='Selection Sort')
plt.bar(x + 0.5*bar_width, insertion_times, width=bar_width, label='Insertion Sort')
plt.bar(x + 1.5*bar_width, merge_times, width=bar_width, label='Merge Sort')

# Labels and Title
plt.xlabel('Input Size (N)')
plt.ylabel('Average Execution Time (ms)')
plt.title('Sorting Algorithms Performance (Bar Graph)')
plt.xticks(x, input_sizes)  # Set x-tick labels as input sizes
plt.legend()
plt.grid(True, axis='y')
plt.tight_layout()

# Show plot
plt.show()



