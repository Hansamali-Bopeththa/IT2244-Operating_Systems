# IT2244-Operating_Systems

1) File Management (Windows Command Line)
This part uses Windows CMD commands to create directories, files, copy, move, and hide files.

Step-by-step breakdown:
Navigate to Desktop

cd %USERPROFILE%\desktop
Moves to the user's desktop.

Create directories

mkdir CSC2244
mkdir Marks
mkdir Exam
Creates three folders: CSC2244, Marks, and Exam.

Create subdirectories and files

Inside CSC2244, folders practical, theory, and "exam papers" are created.

Within these folders, text (.txt), document (.docx), and presentation (.pptx) files are created using echo. > filename.

Create Excel files and move them

echo. > Icae_Marks.xlsx
echo. > Final_Exam_Marks.xlsx
copy "%USERPROFILE%\Desktop\Icae_Marks.xlsx" "%USERPROFILE%\Desktop\Marks"
copy "%USERPROFILE%\Desktop\Final_Exam_Marks.xlsx" "%USERPROFILE%\Desktop\Marks"
echo. > filename.xlsx creates empty Excel files.

copy moves these files to the Marks folder.

Copy the Marks folder to Exam

xcopy "%USERPROFILE%\Desktop\Marks" "%USERPROFILE%\Desktop\Exam\" /E /I
/E copies all files and subdirectories.

/I treats destination as a folder.

Hide the Exam folder

attrib +h "%USERPROFILE%\Desktop\Exam"
Adds the hidden attribute to the Exam folder.

2) AWK (Data Processing)
This part filters data and calculates an average GPA using awk.

Filter rows where GPA > 3.5
bash
awk -F, 'NR==1 || $4 > 3.5' data.csv
-F, → Sets the delimiter to a comma (CSV file format).

NR==1 → Keeps the header row.

$4 > 3.5 → Filters rows where column 4 (GPA) is greater than 3.5.

Calculate the average GPA
bash
awk -F, 'NR>1 {sum+=$4; count++} END {if (count > 0) print "Average GPA:", sum/count}' data.csv
NR>1 → Skips the first row (header).

sum+=$4; count++ → Accumulates GPA values and counts rows.

END {print sum/count} → Computes and prints the average GPA.

3) Bash Script (String Comparison)
This script reads two strings, compares their length, and prints which is longer.

Step-by-step breakdown:
Read input strings

bash
echo "Enter String_1"
read string1
echo "Enter String_2"
read string2
Uses read to get two user-input strings.

Compute string lengths

bash
strlength1=${#string1};
strlength2=${#string2};
${#string} gets the length of the string.

Compare lengths and print results

bash
if [ $strlength1 -gt $strlength2 ]; then
    echo "$string1 is larger than $string2"
elif [ $strlength1 -eq $strlength2 ]; then
    echo "$string1 and $string2 are in equal length"
else
    echo "$string2 is larger than $string1"
fi
Compares the lengths and prints which string is longer.

If they are equal, it prints that they are the same length.

Example Run:
Enter String_1
apple
Enter String_2
banana
banana is larger than apple
"banana" has 6 characters, while "apple" has 5, so "banana" is longer.
