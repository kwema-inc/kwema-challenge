## Bacterial Population Estimation

An experimental scientific study has created a new species of bacteria in the laboratory. These bacteria have a particular life cycle. Each adult bacterium takes 3 days to divide and give rise to two new bacteria, and a newborn bacterium reaches adulthood in 1 day.

However, the bacteria are not synchronized with each other in terms of their division cycle.

Given an initial number of adult bacteria and a certain number of days, you need to determine the total number of bacteria in the population after that number of days.

If a bacteria has an internal counter of 3

- After one day it will be 2 
- After another day it will be 1
- After one more day it will be 0
- After yet another day it will be 3 again, and another two new bacterias will be born with a counter of 4

As observed, an adult bacteria resets its counter to 3, while a newborn bacteria starts at 4 (due to taking a day to reach adulthood).

Then, if we have an initial state of 5 bacterias:

```
[2, 3, 3, 1, 2]
```

After 8 days, we will have an iteration as follows:

```
Initial state:    2,3,3,1,2
After  1 day:     1,2,2,0,1
After  2 days:    0,1,1,3,0,4,4
After  3 days:    3,0,0,2,3,3,3,4,4,4,4
After  4 days:    2,3,3,1,2,2,2,3,3,3,3,4,4,4,4
After  5 days:    1,2,2,0,1,1,1,2,2,2,2,3,3,3,3
After  6 days:    0,1,1,3,0,0,0,1,1,1,1,2,2,2,2,4,4
After  7 days:    3,0,0,2,3,3,3,0,0,0,0,1,1,1,1,3,3,4,4,4,4,4,4,4,4
After  8 days:    2,3,3,1,2,2,2,3,3,3,3,0,0,0,0,2,2,3,3,3,3,3,3,3,3,4,4,4,4,4,4,4,4,4,4,4,4
```

Also, on day 8, we have a total of 37 bacterias, and after 60 days we would have a total of 7301991 bacterias

Notes:

- The initial number of adult bacteria is provided as the argument bacterias.
- The number of days is provided as the argument days.
- Feel free to choose the technology stack with which you feel most comfortable


## Challenge

- Build a function to calculate the final number of bacteria produced from an initial set of bacteria after n days (the value of n is passed as an argument).
- Build an API to provide this tool to all biologists worldwide through the internet for many different initial sets of bacteria.
- This API should provide a method to configure a new bacterial strain with different maturation periods (days needed to reach adulthood), life expectancy, and reproduction rate (how many new bacteria are produced in each cell subdivision).
- The function must be efficient enough to simulate scenarios of up to 1000 days.
- Provide instructions to run and test your solution

> There is no need to deploy the API on a real server.

> Please send the public repository link with the solution to this challenge to joel@kwema.co or grant access to your GitHub repository to the GitHub user "joelibaceta".


### Bonus
- Adhere to REST recommendations.
- Provide documentation and comments for code and API specification.
- Implement testing, such as unit testing.
- Implement proper error handling for user input mistakes.
- Consider the algorithm's complexity order.

