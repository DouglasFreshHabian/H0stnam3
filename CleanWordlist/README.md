# A more robust Bash script that processes a wordlist and checks if each word conforms to the rules for valid hostnames:

## What this script does: 📜

 - It takes a wordlist file as input.

 - Cleans the wordlist by stripping out carriage returns and newline characters.

 - Validates each word to ensure it conforms to the hostname rules:

 - It must only contain alphanumeric characters and hyphens (-).

 - It cannot start or end with a hyphen.

 - It must be between 1 and 63 characters long.

 - Writes valid hostnames to a cleaned wordlist file.

 - Logs invalid words with details to a log file.

## Valid Hostname Rules: 📏

A hostname can contain only alphanumeric characters (a-zA-Z0-9), and hyphens (-).

It cannot start or end with a hyphen (-).

It must be between 1 and 253 characters long, and each individual label (part separated by dots) must be no longer than 63 characters.

  ### Script Steps: 🔧

        Read each word from the wordlist.

        Check if the word contains only allowed characters.

        Check if the word starts or ends with a hyphen.

        If the word is valid, add it to a new list, otherwise, discard it.

This script is designed to clean a wordlist by ensuring that all words in the list follow the rules for valid hostnames, 
and then save a cleaned version of the wordlist to a new file. It also logs any invalid entries and outputs helpful 
information with colorized formatting.

## These are ANSI escape codes for adding color to the terminal output. Colors are used to make the script's messages stand out: 🖌

    RED: Used for error messages.

    GREEN: Used for success messages.

    YELLOW: Used for warnings or invalid entries.

    BLUE: Used for informational or status messages.

    RESET: Resets the color formatting back to default.

## Key Points: 🔑

    Error Handling: The script includes error handling via error_exit(), which will halt execution if something goes wrong.

    Logging: All actions, including invalid word checks, are logged in the wordlist_cleaning.log file.

    Wordlist Cleaning: The script validates and cleans the input wordlist, ensuring all words conform to valid hostname rules.

    User-Friendly Output: The script includes color-coded messages for user-friendliness and displays an ASCII banner to make it more engaging.

