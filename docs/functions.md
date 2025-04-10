import random

def load_quotes(filename):
    """
    Loads quotes from a file and returns them as a list.
    Parameters:
    filename (str): The path to the file containing quotes.
    The function reads the file line by line, strips whitespace, and appends
    non-empty lines to a list. Each line in the file should contain one quote.
    Returns:
    list: A list of quotes loaded from the file.
    Example:
    load_quotes('quotes.txt')
    This function reads the file 'quotes.txt' and returns a list of quotes.
    """
    quotes = []
    with open(filename, 'r') as file:
        lines = file.readlines()
    for line in lines:
        line = line.strip()
        if line:
            quotes.append(line)
    return quotes

def random_quote(quotes):
    """
    Returns a random quote from the provided list of quotes.
    Parameters:
    quotes (list): A list of quotes from which a random quote will be selected.
    The function uses the random.choice() method to select a random quote.
    Returns:
    str: A randomly selected quote from the list.
    Example:
    random_quote(['Quote 1', 'Quote 2', 'Quote 3'])
    This function returns a random quote from the provided list.
    """  
    return random.choice(quotes)

def print_quote(quote):
    """
    Prints a single quote to the console.
    Parameters:
    quote (str): The quote to be printed.
    The function formats the quote with asterisks and prints it to the console.
    Returns:
    None
