# Day-03

# MATLAB Practicals: String Functions & Conditional Statements

**Author:** Dinuka Avindra Silva  
**Date:** 2025-06-03  

---

## 🧩 Practical Overview

This practical set explores:

- MATLAB **string manipulation functions**  
- **User input handling**  
- Conditional statements to determine **vowels**, **largest numbers**, and **grades**  

---

## 🔍 Code Highlights

### String Manipulation

- Concatenation of strings:
  ```matlab
  str1 = 'apple';
  str2 = 'banana';
  result = strcat(str1, str2);
  disp(result) % Output: applebanana
% MATLAB Practical: String Functions & Conditional Checks
% Author: Dinuka Avindra Silva
% Date: 2025-06-03

%% String Manipulation Examples

% Concatenate two strings
str1 = 'apple';
str2 = 'banana';
result = strcat(str1, str2);
disp(['Concatenated string: ', result]);

% Concatenate elements of a cell array
x = {'hello', 'world', 'sri'};
result2 = strcat(x{:});
disp(['Concatenated cell array: ', result2]);

% Join strings with ':' and with space
result3 = strjoin(x, ':');
disp(['Joined with colon: ', result3]);

result4 = strjoin(x, ' ');
disp(['Joined with space: ', result4]);

% Compare two strings
str1 = 'age';
str2 = 'tryr';
isEqual = strcmp(str1, str2);
disp(['Are "', str1, '" and "', str2, '" equal? ', mat2str(isEqual)]);

% Find substring index
stri1 = 'the cat sat on the mat';
index = strfind(stri1, 'cat');
disp(['"cat" found at position(s): ', num2str(index)]);

% Replace substring
old = 'cat';
new = 'dog';
newStr = strrep(stri1, old, new);
disp(['After replacement: ', newStr]);

% Split string into parts
inputstring = 'apple,banana,orange,grapes';
parts = strsplit(inputstring, ',');
disp('Split strings:');
disp(parts);

% Change case
st1 = 'apPLE';
disp(['Lowercase: ', lower(st1)]);
disp(['Uppercase: ', upper(st1)]);

% Trim whitespace
trimmed = strtrim(' hello world ');
disp(['Trimmed string: "', trimmed, '"']);

%% User Input: Vowel or Consonant Check

char = input('Enter your letter: ', 's');
disp(['Your letter is: ', char]);

if length(char) ~= 1 || ~isletter(char)
    disp('Invalid input! Please enter a single letter.');
elseif any(lower(char) == ['a','e','i','o','u'])
    disp('Your letter is a Vowel letter');
else
    disp('Your letter is a Consonant letter');
end

%% Find the Largest Number from User Input

num1 = input('Enter number 1: ');
num2 = input('Enter number 2: ');
num3 = input('Enter number 3: ');

maxVal = max([num1, num2, num3]);
disp(['The largest number is: ', num2str(maxVal)]);

%% Grade Calculator Based on Marks

marks = input('Enter your marks: ');
disp(['Your marks are: ', num2str(marks)]);

if marks > 100 || marks < 0
    disp('Invalid marks');
elseif marks >= 90
    disp('Your grade is A+');
elseif marks >= 80
    disp('Your grade is A');
elseif marks >= 70
    disp('Your grade is B');
elseif marks >= 60
    disp('Your grade is C');
elseif marks >= 50
    disp('Your grade is D');
else
    disp('Your grade is F');
end
