# Getting started with Git
**California State University, Northridge**  
**Department of Electrical and Computer Engineering**  

## Objective

Help students become familiar with basic Git commands and Git workflow.

## Requirements

- Git >= 2.33
- GitHub account
- Link to GitHub classroom assignment

## References
- https://git-scm.com/
- https://guides.github.com/

## Introduction

## What is Git
Git is a free and open source distributed version control system.
Source: https://git-scm.com/

## What is GitHub
GitHub is a code hosting platform for version control and collaboration.
GitHub is built on Git version control system. It provides a web-based 
user interface and cloud storage for open source projects. It also provides
Enterprise version for private code hosting.

Source: https://guides.github.com/activities/hello-world/

## What is Markdown language:
Markdown is a lightweight and easy-to-use syntax for styling all forms 
of writing on the GitHub platform using a plain-text.

Source: https://guides.github.com/features/mastering-markdown/

## Tasks

:point_right: **Task 1**: Clone git repo to your local

Use the following command to clone the assignment repo to your local machine:

```bash
$ git clone name-of-the-repo
```

Note: Make sure to replace `name-of-the-repo` with your assignment git link.  
Note: The `$` sign is not part of the command. It is a convensional way to say 
this command should be run in the command prompt of a terminal.

Updae the README.md file with the following markdown tags:

:point_right: **Task 2**: Make the following text a heading 1 on the first line of README.md file in the main folder:
```
CSUN ECE your-class-number
```

:point_right: **Task 3**: Make the following text a heading 2 on the second line of README.md file in the main folder:
```
Getting started with Git
```

:point_right: **Task 4**: Make the following text bold on the lines 3 to 4 README.md file in the main folder:
```
Name: your-name
Date: submission-date
```

In the above make sure to preview your README file to make sure each 
`Name` and `Date` are on separate lines.

*Note: Do not use `<br/>` to create line break.*  
*Hint: Use 2 spaces at the end of line to create break.*  

:point_right: **Task 5**: Create and ordered list on line 6 to 8

```
FPGA
VHDL
Verilog
```

:point_right: **Task 5**: Add CSUN logo image on line 10. The image is located in
`./img/csun_eng_logo.png`. Use `CSUN ENG` as alternative name of the image.

:point_right: **Task 6**: Add your GitHub profile link to line 12 with your name as the link title
Make sure the link is on separate line and not on the same line as image.

*Hint: Having an extra line will let Markdown compiler to use a line break.*

:point_right: **Task 7**: Add the following VHDL code on line 14. Make sure to
use `vhdl` keyword at the code block to highlight VHDL syntax.

```
library ieee;
use ieee.std_logic_1164.all;
use ieee.std_logic_unsigned.all;

entity counter is
    port (
        clk : in std_logic;
        reset : in std_logic;
        enable : in std_logic;
        count : out std_logic_vector(3 downto 0)
    );
end counter;

architecture Behavioral of counter is
    signal pre_count : std_logic_vector(3 downto 0);
begin
    process (clk, enable, reset)
    begin
        if reset = '1' then
            pre_count <= "0000";
        elsif (clk = '1' and clk'event) then
            if enable = '1' then
                pre_count <= pre_count + "1";
            end if;
        end if;
    end process;
    count <= pre_count;
end Behavioral;
```

:point_right: **Task 9**: Use the following command to see all unstaged files

```
$ git status
```
See here for syntax info: https://git-scm.com/docs/git-status

:point_right: **Task 10**: Take a screenshot from your git status output terminal
and save the file as `git_stat.png` in the `./img` folder. 
On line 45 of README add the screenshot image to show up in your file. 
Use `git status before stage` as alternate name of your image.

:point_right: **Task 11**: Press enter to add a new line which would be line 46 
in your README file. Files should have an empty line at the end. No whitespace 
or other character should be on the last line.

:point_right: **Task 12**: Use the following command to stage all files

```
$ git add .
```

See here for syntax info: https://git-scm.com/docs/git-add


:point_right: **Task 13**: Use the following command to commit your changes

```
$ git commit -m 'your-git-user-name: a shor message describing your change'
```

See here for syntax info: https://git-scm.com/docs/git-commit

:point_right: **Task 14**: Use the following command to push your changes to remote repo

```
$ git push origin master
```

Note: Verify your changes look correct in the GitHub page.
If changes are not correct make the necessary changes and repeat tasks 
12, 13, and 14 to push your update to the repo.

Hint: Your output should look like the following:  

![final output](./img/final_output.png)
