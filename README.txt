Given a list of integers, output an integer-valued list of equal length such that the output element at index 'i' is the product of all input elements except for the input element at 'i'

From Question #3 on http://evernote.com/careers/challenge.php


--------------------------------------------------
Pseudo code

# Collect & process input
Input => int n
numbers = []
For i = 1..n
  Input => String num
  numbers[i] = num

# Multiply all numbers in the list
product = numbers.mapReduceMaybe{ | product, element | product *= element }

# Calculate elements in new array
numbers.each{ | index, element |
  numbers[index] = product / element
}

# Print outputArray
print outputArray.join("\n")


--------------------------------------------------
