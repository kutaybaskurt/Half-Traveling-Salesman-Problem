TSP Verifier

This project is a Python script to verify solutions for the Traveling Salesman Problem (TSP), specifically checking the correctness of a given solution based on an input file describing the cities and a solution file listing the tour and its total distance.

Features

Verifies if the given TSP solution is valid based on the cities and their coordinates.
Ensures that each city is visited once.
Checks for invalid city IDs and duplicate cities.
Calculates the total distance of the tour and compares it with the given solution's total distance.
Provides feedback on whether the solution is verified or not.
Usage

To use the TSP Verifier, run the script as follows:

bash

python tsp-verifier.py <instancefile> <solutionfile>
Parameters:
instancefile: A file containing the list of cities with their coordinates.
solutionfile: A file containing the proposed solution (total distance and tour order).
Example:
bash

python tsp-verifier.py cities.txt solution.txt
Input File Format

Instance File (instancefile)
Each line in the instance file represents a city with three integers:
identifier (starting from 0 and consecutive)
x-coordinate
y-coordinate
Example:


0 10 20
1 15 25
2 30 35
Solution File (solutionfile)
The first line is the total distance of the tour.
The remaining lines list the cities in the order they are visited (each city is listed once).
Example:


75
0
1
2
How It Works

The script reads the list of cities from the instancefile.
It then reads the proposed solution from the solutionfile.
It verifies the following:
Each city is visited exactly once.
The city IDs are valid.
The total distance of the tour matches the solution.
If all checks pass, it prints Your solution is VERIFIED.; otherwise, it prints an error message with details.
Dependencies

Python 3.x
Numpy: Install via pip install numpy
License

This project is open-source and available under the MIT License.

