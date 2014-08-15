crossword
=========

Python library for handling crossword puzzles. This library provides a canonical data structure
that can be used to represent crosswords in your application. It provides a Pythonic way to
perform common operations on the grid, the words and the clues of the puzzle.

You can create a crossword:

    from crossword as Crossword

    puzzle = Crossword(15, 15)

You can iterate over rows and cells:

    for row in puzzle:
        for cell in row:
            pass

You can access a puzzle's metadata:

    creator = puzzle.meta.creator

You can also access all metadata attributes using dictionary syntax as meta is a dictionary:

    creator = puzzle.meta['creator']
    print(puzzle.meta.items())

You can set a clue for an entry:

    puzzle.clues.across[1] = "This is a clue"
    puzzle.clues.down[2] = "This is a clue"

You can iterate over a crossword's clues by using:

    for number, clue in puzzle.clues.across.items():
        print(number, clue)
