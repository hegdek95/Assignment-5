# Assignment-5
python programs

# 1.Write a Python program to calculate the length of a string.
s ='Hello'
print(len(s))
  # output : 6 

# 2.Write a Python program to count the number of characters (character frequency) in a string.
def char_frequency(str1):
    dict = {}
    for n in str1:
        keys = dict.keys()
        if n in keys:
            dict[n] += 1
        else:
            dict[n] = 1
    return dict
print(char_frequency('hello iam karthik'))
  # output : {'h': 2, 'e': 1, 'l': 2, 'o': 1, ' ': 2, 'i': 2, 'a': 2, 'm': 1, 'k': 2, 'r': 1, 't': 1}

# 3 Write a Python program to get a string made of the first 2 and the last 2 chars from a given a string. If the string length is less than 2, return instead of the empty string. 
def strings(s):
    return s[:2]+s[-2:] if len(s) >=2 else 'empty string'
  
  # output : banana :bana, hi : empty String
  
# 4  Write a Python program to get a string from a given string where all occurrences of its first char have been changed to '$', except the first char itself.
e = "test String"
f = e[0]
for char in e[1:]:
    if char == e[0]:
        f+="$"
    else:
        f+=char

print(f)
  # output : redeem the $ewa$d $equi$ed
# 5.Write a Python program to get a single string from two given strings, separated by a space and swap the first two characters of each string.
a = 'abc'
b = 'xyz'
print("Before Swap :",a," ",b)
a1 = b[:2] + a[2:]
b1 = a[:2] + b[2:]
print("After Swap :",a1," ",b1)
# output : Before Swap : abc   xyz , After Swap : xyc   abz

# 6 Write a Python program to add 'ing' at the end of a given string (length should be at least 3). If the given string already ends with 'ing' then add 'ly' instead.
def add_string(str1):  
  length = len(str1)  
  
  if length > 2:  
    if str1[-3:] == 'ing':  
      str1 += 'ly'  
    else:  
      str1 += 'ing'  
  
  return str1  
print(add_string('ab'))  
print(add_string('abc'))  
print(add_string('string')) 

# 7 Write a Python program to find the first appearance of the substring 'not' and 'poor' from a given string, if 'not' follows the 'poor', replace the whole 'not'...'poor' substring with 'good'. Return the resulting string.
def not_poor(str1):
  snot = str1.find('not')
  spoor = str1.find('poor')
  

  if spoor > snot and snot>0 and spoor>0:
    str1 = str1.replace(str1[snot:(spoor+4)], 'good')
    return str1
  else:
    return str1
print(not_poor('The lyrics is not that poor!'))
print(not_poor('The lyrics is poor!'))

# 8 Write a Python function that takes a list of words and returns the length of the longest one.
def find_longest_word(text):
    for words in text.split():
        if len(words) > longest:
            longest = len(words)
            longest_word = words
    return longest_word, len(longest_word)

def main():
    input_string = input("Please input a list of words to evaluate: ")
    longest_word = find_longest_word(input_string)
    print("The longest word is", longest_word, "with length", len(longest_word))


def find_longest_word(text):
    longest_word = max(text.split(), key = len)
    return longest_word, len(longest_word)
# 9  Write a Python program to remove the nth index character from a nonempty string.
def remove(string, n):  
  first = string[:n]   
  last = string[n+1:]  
  return first + last

# 10 Write a Python program that accepts a comma separated sequence of words as input and prints the unique words in sorted form (alphanumerically). 
items = input("red, black, pink, green")
words = [word for word in items.split(",")]
print(",".join(sorted(list(set(words)))))

# 11 Write a Python function to reverses a string if it's length is a multiple of 4.
def reverse_string(str1):
    if len(str1) % 4 == 0:
       return ''.join(reversed(str1))
    return str1

print(reverse_string('abcd'))
print(reverse_string('python'))

# 12 Write a Python function to convert a given string to all uppercase if it contains at least 2 uppercase characters in the first 4 characters.
def to_uppercase(str1):
    num_upper = 0
    for letter in str1[:4]: 
        if letter.upper() == letter:
            num_upper += 1
    if num_upper >= 2:
        return str1.upper()
    return str1

print(to_uppercase('Python'))
print(to_uppercase('PyThon'))

# 13 Write a Python program to check whether a string starts with specified characters.
string = "Hello world"
print(string.startswith("Hello"))
  # output : True

# 14 \ Write a Python program to print the following floating numbers upto 2 decimal places 3.1415926
x = 3.1415926
y = 12.9999
print("\nOriginal Number: ", x)
print("Formatted Number: "+"{:.2f}".format(x));
print("Original Number: ", y)
print("Formatted Number: "+"{:.2f}".format(y));
print() 

# 15  Write a Python program to count repeated characters in a string.
import collections
str1 = 'thequickbrownfoxjumpsoverthelazydog'
d = collections.defaultdict(int)
for c in str1:
    d[c] += 1
for c in sorted(d, key=d.get, reverse=True):
  if d[c] > 1:
      print('%s %d' % (c, d[c]))

# 16 Write a Python program to print the index of the character in a string
myString = 'Position of a character'
print(myString.index('s'))

# 17 Write a Python program to convert a string in a list.
k = 'Hello hi my name is karthik'.split()
print (k)

#18

