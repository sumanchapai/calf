## Installation

```sh
pip install fcal
```

## Usage

```sh
# Print the last 10 days in the default format
fcal -b 10

# Print the last 10 days in MM-DD format 
fcal -b 10 -f '%m-%d'

# Print the last 10 days and next 10 days in local datetime format %c  
fcal -b 10 -a 10 -f '%c'

# Skip the dates until the next year skiping every 7 days.
fcal -a 365 -s 7
```

## Date Directives

| Directive | Meaning                                                   | Example                        |
| --------- | --------------------------------------------------------- | ------------------------------ |
| `%A`      | Weekday as locale’s abbreviated name.                     | Sun, Mon,                      |
| `%A`      | Weekday as locale’s full name.                            | Sunday, Monday, …, Saturday    |
| `%d`      | Day of the month as a zero-padded decimal number.         | 01, 02, …, 31                  |
| `%-d`     | Day of the month as a decimal number.                     | 1, 2, …, 31                    |
| `%B`      | Month as locale’s full name.                              | January, February, …, December |
| `%m`      | Month as a zero-padded decimal number.                    | 01, 02, …, 12                  |
| `%-m`     | Month as a decimal number.                                | 1, 2, …, 12                    |
| `%y`      | Year without century as a zero-padded decimal number.     | 00, 01, …, 99                  |
| `%Y`      | Year with century as a decimal number.                    | 2001, 2010, …, 2093            |
| `%%`      | A literal `'%'` character.                                | %                              |


## Development

To build the package locally, run

```python -m build```

Uploading to twine, which only package authors can do, is done using twine. To test the package locally, run `pip install .`
