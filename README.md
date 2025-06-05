# Windows-basic-commands-batchscript
Ex08-Windows-basic-commands-batchscript

# AIM:
To execute Windows basic commands and batch scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Windows environment installed on the system or installed inside a virtual environment like virtual box/vmware 

### Step 2:

Write the Windows commands / batch file . Save each script in a file with a .bat extension. Ensure you have the necessary permissions to perform the operations. Adapt paths as needed based on your system configuration.
### Step 3:

Execute the necessary commands/batch file for the desired output. 




# WINDOWS COMMANDS:
## Exercise 1: Basic Directory and File Operations

---
## Create a directory named "my-folder"

 __COMMAND AND OUTPUT__


![image](https://github.com/user-attachments/assets/7d2bd1e8-aecc-4e7f-9dba-f4fd5ad9340a)


## Remove the directory "my-folder"

**COMMAND AND OUTPUT**

![image](https://github.com/user-attachments/assets/b9ef7d68-8b0b-4c3e-b63c-b93a1f0815e4)

## Create the file Rose.txt

**COMMAND AND OUTPUT**

![image](https://github.com/user-attachments/assets/728edde9-c680-4a8b-b3f3-4031aa539b1a)


## Create the file hello.txt using echo and redirection

 __COMMAND AND OUTPUT__


![image](https://github.com/user-attachments/assets/beeab841-f7d4-4a7b-9b29-6eefc178a4cd)

## Copy the file hello.txt into the file hello1.txt

__COMMAND AND OUTPUT__


![image](https://github.com/user-attachments/assets/88660347-f15c-4acd-a669-54f5c2e43fed)

## Remove the file hello1.txt

 __COMMAND AND OUTPUT__


![image](https://github.com/user-attachments/assets/f7518833-0c37-4efd-98d3-2c5386933649)

## List out the file hello1.txt in the current directory

 __COMMAND AND OUTPUT__


![image](https://github.com/user-attachments/assets/8ae3f4a9-a3b0-4240-b6de-452e9c0bdc47)

## List out all the associated file extensions 

__COMMAND AND OUTPUT__


![image](https://github.com/user-attachments/assets/783c7931-044b-4c65-bbac-8a547b2809be)

![image](https://github.com/user-attachments/assets/71584231-7ab9-4673-91a1-92ac0f810046)


## Compare the file hello.txt and rose.txt

 __COMMAND AND OUTPUT__


![image](https://github.com/user-attachments/assets/eb8a16ed-a1dd-4f93-9e55-c5923433bc23)



## Exercise 2: Advanced Batch Scripting
__1__.Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".

### BATCH PROGRAM

``` batch
@echo off
set name=John
echo Hello, %name%
pause
```



### OUTPUT

![image](https://github.com/user-attachments/assets/eafd9dbf-7a1d-4a7d-9b09-3bf499417972)



__2__.Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
Prompt the user to enter a number.
Calculate the remainder when the number is divided by 2.
Display whether the number is odd or not.
Ask the user if they want to check another number.
Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
Handle invalid inputs for the continuation prompt (Y/N) gracefully.

### BATCH PROGRAM
``` batch
@echo off
:loop
set /p num=Enter a number: 
set /a rem=%num% %% 2

if %rem%==0 (
    echo %num% is Even
) else (
    echo %num% is Odd
)

:ask
set /p ans=Do you want to check another number? (Y/N): 
if /I "%ans%"=="Y" goto loop
if /I "%ans%"=="N" goto end
echo Invalid input. Please enter Y or N.
goto ask

:end
echo Thank you!
pause
```

### OUTPUT


![image](https://github.com/user-attachments/assets/a34f63db-3a1a-47d4-81d6-814c452e4774)



__3__.Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.

### BATCH PROGRAM

``` batch
@echo off
for /L %%i in (1,1,5) do (
    echo Number: %%i
)
pause
```

### OUTPUT


![image](https://github.com/user-attachments/assets/513605b7-8fe9-4227-b9d9-5730f1ffa083)


__4__.Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

__Instructions:__
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):

### BATCH PROGRAM

``` batch
@echo off
if exist sample.txt (
    echo sample.txt exists.
) else (
    echo sample.txt does not exist.
)
pause
```

### OUTPUT


![image](https://github.com/user-attachments/assets/87390f90-8046-4042-9fe7-524d953b7935)

__5__.Write a batch script that displays a simple menu with three options:
Say Hello – Displays the message Hello, World!
Create a File – Creates a file named newfile.txt with the content This is a new file
Exit – Exits the script with a goodbye message
The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.

### BATCH PROGRAM

``` batch
@echo off
:menu
cls
echo 1. Say Hello
echo 2. Create a File
echo 3. Exit
set /p choice=Choose an option (1-3): 

if "%choice%"=="1" goto hello
if "%choice%"=="2" goto create
if "%choice%"=="3" goto exit
echo Invalid choice.
pause
goto menu

:hello
echo Hello, World!
pause
goto menu

:create
echo This is a new file > newfile.txt
echo File newfile.txt created.
pause
goto menu

:exit
echo Goodbye!
pause
exit
```

### OUTPUT


![image](https://github.com/user-attachments/assets/c189750d-8afe-4f39-a2e2-c4459dbe275f)


![image](https://github.com/user-attachments/assets/d8536300-79cc-446b-8653-33362431114b)

![image](https://github.com/user-attachments/assets/d3323282-8e1b-4f5c-9454-506771c6dfe2)


# RESULT:
The commands/batch files are executed successfully.
