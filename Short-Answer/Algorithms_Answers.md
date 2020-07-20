#### Please add your answers to the ***Analysis of  Algorithms*** exercises here.

## Exercise I

a)
a = 0                   
while (a < n * n * n):  O(n) - its a loop that is true wile a is less than n^3, n does not change only a does
a = a + n * n: Runtime = O(1) 

b)
sum = 0
    for i in range(n): # Runtime = O(n)
        j = 1          # Runtime = O(1)
    while j < n:       # Runtime = O(n)
        j *= 2         # Runtime = O(nk) or O(1)?
        sum += 1       # Runtime = O(1)

c)
def bunnyEars(bunnies):             
      if bunnies == 0:                         
        return 0

      return 2 + bunnyEars(bunnies-1)

Runtime = O(n) 

## Exercise II
Create a function that takes in an n number of building stories.
    floor zero does not exist, so you have to stop function at 0
find the middle in n and drop an egg and see if it breaks (true/false)
    if true (broken), then you know you are too high
        take the lower half and break it in a half again
        check to see if the egg breaks if true do the same as above
    if false (not broken) the you are too low to find at what floor the egg breaks go high
        take the upper half and split that again. check that floor, based on your results true/false repeat the steps above
    do this until the nth floor == true and nth floor -1 == false

Runtime = 0(n)