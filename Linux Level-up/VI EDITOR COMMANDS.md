# VI EDITING COMMANDS


    1) i – Insert at cursor (goes into insert mode)

    2) a – Write after cursor (goes into insert mode)
    
    3) A – Write at the end of line (goes into insert mode)
    
    4) ESC – Terminate insert mode
    
    5) u – Undo last change
    
    6) U – Undo all changes to the entire line
    
    7) o – Open a new line (goes into insert mode)
    
    8) dd – Delete line
    
    9) 3dd – Delete 3 lines.
    
    10) D – Delete contents of line after the cursor
    
    11) C – Delete contents of a line after the cursor and insert new text. Press ESC key to end insertion.
    
    12) dw – Delete word
    
    13) 4dw – Delete 4 words

    14) cw – Change word
    
    15) x – Delete character at the cursor
    
    16) r – Replace character
    
    17) R – Overwrite characters from cursor onward
    
    18) s – Substitute one character under cursor continue to insert
    
    19) S – Substitute entire line and begin to insert at the beginning of the line
    
    20) ~ – Change case of individual character


Note: You should be in the “command mode” to execute these commands. VI editor is case-sensitive so make sure you type the commands in the right letter-case.

Make sure you press the right command otherwise you will end up making undesirable changes to the file. You can also enter the insert mode by pressing a, A, o, as required.


# Commands for Saving and Closing the file

    1) Shift+zz – Save the file and quit

    2) :w – Save the file but keep it open

    3) :q – Quit without saving
    
    4) :wq – Save the file and quit