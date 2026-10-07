# Homework 1

## Problem 1

| Criteria | Description | Points |
| --- | --- | --- |
| Function Setup | Correctly defines calculate_factorial(n) and returns the calculated value using return. | 10 |
| Loop & Product Logic | Implements a for or while loop to multiply numbers 1 through n correctly. | 15 |
| Special Case (n=0) | Correctly handles 0!=1 without crashing or returning 0. | 10 |
| Input/Output | "Prompts user for an integer, calls the function, and prints output matching requirements." | 7.5 |
| Code Quality | "Proper indentation, clean variable naming (e.g., product, result), and readable style." | 7.5 |
| Total | | 50 |

## Problem 2

| Criteria | Description | Points |
| --- | --- | --- |
| Function Setup | Correctly defines count_vowels(text) and returns the total vowel count using return. | 10 |
| Loop & Character Check | Loops through each character in the string and checks if it is in 'aeiou'. | 15 |
| Case Insensitivity | Handles uppercase and lowercase vowels using .lower() or checking both cases. | 10 |
| Input/Output | "Prompts user for a string, calls the function, and prints output matching requirements." | 7.5 |
| Code Quality | "Proper indentation, clean variable naming (e.g., vowel_count, char), and readable style." | 7.5 |
| Total | | 50 |

# Homework 2

| Category | Criteria / Indicators | Point Value |
| --- | --- | --- |
| Core Functionality & Logic | 1. Program runs from start to finish without crashing. <br>2. Successfully creates and accesses required data structures (dictionaries/lists).<br>3. Core calculations (total price / averages) are accurate.<br>4. Loops control flow correctly and terminate on command ("quit"). | 40 Points |
| Exception Handling & Validation | Problem 1: Safely checks for missing dictionary keys (in keyword or .get()).<br>Problem 2: Successfully catches ValueError for invalid string inputs.<br>Problem 2: Successfully catches ZeroDivisionError when a student has no grades. Informative error messages are shown to the user instead of raw Python traces. | 30 Points |
| User Input & Interaction | 1. Prompts are clear and explicit about expected input.<br>2. Handles input case sensitivity (e.g., .lower() or .capitalize()).<br>3. User output formatting matches expected sample output. | 15 Points |
| Code Structure & Formatting | 1. Proper indentation throughout all blocks (if, try, loops).<br>2. Variables use meaningful names (e.g., fruit_prices, student_name).<br>3. Includes clean code comments explaining tricky sections or exception blocks. | 15 Points |

# Homework 3
| Category | Criteria / Requirements | Points |
| --- | --- | --- |
| File Handling (Read & Write) | • Correctly imports and uses the csv module to read input data.<br>• Successfully creates and writes output using standard file writing (open('...', 'w')). | 20 pts |
| Data Structures (Dictionaries & Lists) | • Constructs a dictionary using city names as keys.<br>• Accurately appends valid float temperatures to list values in the dictionary. | 20 pts |
| Exception Handling (try/except) | • Gracefully handles FileNotFoundError if the CSV file is missing.<br>• Catches ValueError on bad numeric conversions, skips corrupt data, and continues processing without crashing. | 20 pts |
| Libraries & Calculations | • Uses statistics.mean() (or equivalent mathematical logic) to calculate city averages correctly.<br>• Formats calculated averages cleanly (e.g., rounded to 1 decimal place). | 15 pts |
| Control Flow & Loops | • Uses for loops correctly to read through CSV rows and process dictionary contents. | 15 pts |
| Code Style & Formatting | • Meaningful variable names (city_temps, avg_temp, etc.).<br>• Clean indentation, structure, and helpful comments explaining error-handling logic. | 10 pts |

## Test Cases
Input:<br>
City,Temperature<br>
New York,72.0<br>
Chicago,60.0<br>
New York,78.0<br>
Chicago,64.0<br>
Miami,80.0<br>

Output:<br>
=== WEATHER SUMMARY REPORT ===<br>
New York: 2 readings, Avg Temp: 75.0°F<br>
Chicago: 2 readings, Avg Temp: 62.0°F<br>
Miami: 1 readings, Avg Temp: 80.0°F<br>

Input:<br>
City,Temperature<br>
Dallas,85.5<br>
Seattle,invalid<br>
Dallas,N/A<br>
Seattle,62.0<br>
Houston,<br>
Seattle,58.0<br>

Output:<br>
Skipping invalid temperature for Seattle: invalid<br>
Skipping invalid temperature for Dallas: N/A<br>
Skipping invalid temperature for Houston:<br>
=== WEATHER SUMMARY REPORT ===<br>
Dallas: 1 readings, Avg Temp: 85.5°F<br>
Seattle: 2 readings, Avg Temp: 60.0°F<br>

Input:<br>
None

Output:<br>
Error: The file 'weather_data.csv' was not found. Please check the file path.

Input:<br>
City,Temperature<br>
Boston,67.333333

Output:<br>
=== WEATHER SUMMARY REPORT ===<br>
Boston: 1 readings, Avg Temp: 67.3°F

Input:<br>
City,Temperature<br>
Denver , 50.0<br>
Denver, 54.0

Output:<br>
=== WEATHER SUMMARY REPORT ===<br>
Denver: 2 readings, Avg Temp: 52.0°F
