# indexing-

# Part 1: Identify the Secret Code
# 1. Ask the user to enter a secret code
code = input("Enter a secret code: ")

# 2. Use len() to determine how many characters were entered
length = len(code)

# 3 & 4. Convert to int if 1 character long, otherwise leave as string
if length == 1:
    code = int(code)

# 5. Use type() to display the resulting data type
print("Data type:", type(code))

# 6. Display the code's length
print("Code length:", length)

# Store the code as a string so you can index it
code = "84920"

# Get the first character using positive indexing
first_char = code[0]

# Get the last character using negative indexing
last_char = code[-1]

# Display the results using f-strings
print(f"First character: {first_char}")
print(f"Last character: {last_char}")

code = input("Enter the security code: ")
length = len(code)

if length > 2:
    mid = length // 2
    
    # Check if the length is even or odd
    if length % 2 == 0:
        # Even length: slice from (mid - 1) up to (mid + 1) to get 2 characters
        middle_chars = code[mid - 1 : mid + 1]
    else:
        # Odd length: grab the single character at the middle index
        middle_chars = code[mid]
        
    print(f"Security identifier: {middle_chars}")
else:
    print("No middle identifier is needed.")

def main():
    # Get input from the user
    raw_input = input("Enter your secret code: ")
    length = len(raw_input)

    # Check if the input is a single digit to set the type as int
    if length == 1 and raw_input.isdigit():
        typed_code = int(raw_input)
    else:
        typed_code = raw_input

    # Display basic information using f-strings, len(), and type()
    print(f"Code length: {length}")
    print(f"Code type: {type(typed_code)}")

    # Use positive (0) and negative (-1) string indexing for first and last characters
    if length >= 1:
        print(f"First character: {raw_input[0]}")
        print(f"Last character: {raw_input[-1]}")

    # Check length to display middle character(s) for codes longer than 1 character
    if length > 1:
        mid_index = length // 2
        if length % 2 == 1:
            # Odd length: 1 middle character
            print(f"Middle character: {raw_input[mid_index]}")
        else:
            # Even length: 2 middle characters
            print(f"Middle characters: {raw_input[mid_index - 1]} and {raw_input[mid_index]}")


if __name__ == "__main__":
    main()
