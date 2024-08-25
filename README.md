# Zoleta_Exp-1

## Part 1
    def alphabet_soup (s): #Defining alphabet soup
    return ''.join(sorted(s))

## Part 2

    def emotify(input):
    # Assigning the words to their corresponding emoticons
    emoticons = {
        'smile': ':)',
        'grin': ':D',
        'sad': ':(',
        'mad': '>:( '
    }    
    # Splitting words in the inputted sentence
    words = input.split()
    
    # Replace words with emoticons if it matches
    result = []
    for word in words:
        # Replace word with emoticon if it matches
        if word in emoticons:
            result.append(emoticons[word])
        else:
            result.append(word)

    return ' '.join(result)

## Part 3
    def get_user_input():
    #Prompt the user for input
    user_input = input("Enter numbers separated by spaces: ")

    # Convert the input string to a list of integers
    try:
        # Convert input to list of integers
        numbers = [int(x) for x in user_input.split()]
    except ValueError:
        print("Please enter numbers only!")
        return

    #Number of elements
    if len(numbers) < 3:
        print("The input must contain at least 3 numbers.")
        return

    #Getting first, last, and middle numbers
    first = numbers[0]
    last = numbers[-1]
    middle = numbers[1:-1]

    #Print
    print(f"first: {first}    middle: {middle}    last: {last}")

    # Function call
    get_user_input()

