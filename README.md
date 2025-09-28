# FizzBuzz Game
# Print numbers from 1 to N (user should input N).
# For multiples of 3, print "Fizz". For multiples of 5, print "Buzz".
# For multiples of both 3 and 5, print "FizzBuzz".
# Instead of just printing, store the results in a list and print the final list at the end.
# Bonus 🚀: Write the results into a text file named fizzbuzz_output.txt.
number = int(input("Enter a number: "))
list_fizzbuzz = []
list_fizz = []
list_buzz = []

for i in range(1, number + 1):
    if i % 3 == 0 and i % 5 == 0:
        list_fizzbuzz.append(i)

    elif i % 3 == 0:
        list_fizz.append(i)

    elif i % 5 == 0:
        list_buzz.append(i)

print(f"The fizzbuzz numbers are: {list_fizzbuzz}")
print(f"The fizz numbers are: {list_fizz}")
print(f"The buzz numbers are: {list_buzz}")

with open("fizzbuzz_output.txt", "w") as f:
    f.write(f"FizzBuzz numbers: {list_fizzbuzz}\n")
    f.write(f"Fizz numbers: {list_fizz}\n")
    f.write(f"Buzz numbers: {list_buzz}\n")
