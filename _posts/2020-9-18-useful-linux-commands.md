# List of tips and tricks for using linux commands

## Cut
- This command is used to cut each line in a file into a set of fields/bytes and specify ceratin values of them to be selected.
- It uses one-indexing when specifying the characters/fields to select.

- Using the `-b` argument
  - `cat FILE | cut -b 3,4`<br>
  Prints the third and fourth characters in each line of FILE. <br>
  Note: Don't leave a space after the comma for the list of characters/indecies.

  - `cat FILE | cut -b 3-7`<br>
  Prints the characters in range 3 to 7 in each line of FILE. <br>
  Note: Don't leave a space after the dash for the range of characters/indecies. <br>
  Dropping the end index `START-` means to select all the characters from START till the end of the line.

- Using the `-f` argument
  - `cat FILE | cut -f 2`<br>
  If a delimiter isn't specified using `-d` then the command uses tabs to split the fields.
  `-f 2` selects the second field in the line (The value after the first tab in the line and before the second one)
  - `cat FILE | cut -d " " -f 2`<br>
  Splits each line using spaces ` ` and selects the second value after splitting
  
