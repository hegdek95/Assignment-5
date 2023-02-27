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

# 3
  
