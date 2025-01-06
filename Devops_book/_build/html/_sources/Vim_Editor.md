# Vim Editor in Linux

- Generally Vim Editor is used to edit the files present in the linux system. By default Ubuntu Linux distros have Vim Editor installed on it. But centos Os doesn't have Vim editor installed on it. To install vim editor in centos we need to use te following syntax :

  **Syntax** : `sudo yum install vim -y`

- To open a file in Vim Editor then we use the following syntax.

  **Syntax** : `vim <filename>`

  **Ex** : `vim testfile1.txt`

## Modes of Vim Editor

- Vim editor has 3 modes. Those are :

  1) Command Mode

  2) Insert Mode

  3) Extended Command mode.

- When you run `vim testfile1.txt` then it will open that file in command mode initially. When you are in command move you cannot do anything. If you want to write something in that file then you have move into insert mode. To move into insert mode you just press `i` in the keyboard. Then You can see `--INSERT--` at the bottom of the file which indicates you are in insert mode, now you can start write anything in that file. Once you have written whatever you want in that file then click `esc` button in the keyboard which take back you to command mode. Now to move to extended command mode then you to press colon (`:`) on the keyboard. Now a colon (`:`) is displayed at the bottom of the file which indicates you are in extended command mode. Extended command mode is generally used to save and quit from the file.

- We have some operations which we can perform in extended command mode. Those are :

  1) **Esc+ :w** : This is used to save the changes.

  2) **Esc+ :q** : This is used to quit from the file.

  3) **Esc+ :wq** : To save and quit.

  4) **Esc+ :w!** : To save forcefully.

  5) **Esc+ :q!** : To quit forcefully.

  6) **Esc+ :wq!** : To save and quit forcefully.

  7) **Esc+ :se nu** : To set line numbers in the file.

  8) **Esc+ :set nonu** : To remove the set line numbers in the file.

  9) **Esc+ :x** : To save and quit the file.

  10) **Esc+ :x!** : To save and quit the file forcefully.

  **Note** : Actually we will be in extended command mode only after we click `Esc+ :`. So from above you just use those symbols after colon to do respective tasks. But for full syntax i have written like that.

## Some more operations that you can perform on Vim Editor

- **gg** : To go to begining of the page.

- **G** : To go to end of the page. (In windows for Capital G use `Shift+g`)

- **w** : To move the cursor forward, word by word.

- **b** : To move the cursor backword, word by word.

- **nw** : To move cursor forward to n words . Ex : click `2+w` for moving 2 words forward.

- **nb** : To move cursor backword to n words.

- **u** : To undo the last change (it will do in word level only.) 

- **U** : To undo the previous changes (It will undo entire line).

- **yy** : To copy a line where cursor is pointed out.

- **nyy** : To copy n line from the current line. Ex : 4yy which copies 4 lines from the current line where cursor is pointed now.

- **p** : To paste line below the cursor position.

- **P** : To paste the line above the cursor position.

- **dd** : To delete the entire line. It actually cuts the line where cursor is pointed out, so that you can paste wherever you want it.If you want to delete that line then just don't paste it once you deleted.

- **ndd** : To delete n no of line from cursor position.

- **/** : Search a word in the file.

  