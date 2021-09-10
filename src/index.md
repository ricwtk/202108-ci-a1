# Instructions 

## Assignment tasks

1. Solve the following problems with evolutionary algorithms in Python.

    !!! question "Problem 1: Seating plan arrangement"        
        You need to seat five people on a row of five chairs, sitting side by side. Each of them has their preferencess of the person to sit beside. This is defined by their happiness level defined in the following table:
    
        
        |                | Sitting next to A | Sitting next to B | Sitting next to C | Sitting next to D | Sitting next to E |
        |:--------------:|:-----------------:|:-----------------:|:-----------------:|:-----------------:|:-----------------:|
        | Happiness of A | -                 | 20                | 20                | 30                | 25                | generally friendly
        | Happiness of B | 20                | -                 | 50                | 20                | 5                 | pickish
        | Happiness of C | 10                | 10                | -                 | 100               | 10                | pickish
        | Happiness of D | 50                | 5                 | 10                | -                 | -5                | pickish
        | Happiness of E | -50               | -30               | -100              | -10               | -                 | extremely introverted

        The calculation of happiness for each person is shown with the following example. If there are only three chairs, A sits on one side, B sits in the middle, and C sits in the other side, i.e. A - B - C, the happiness of each person is calculated as follows:

        - Happiness of A = Happiness of A sitting next to B = 20
        - Happiness of B = Happiness of B sitting next to A + Happiness of B sitting next to C = 20 + 50 = 70
        - Happiness of C = Happiness of C sitting next to B = 10

    !!! question "Problem 2: Time to move"
        You are asked to vacate your current accommodation next week anytime between Monday 0000 to Sunday 2359. For any part of a day you stay in the current accommodation, you will need to pay the rental rate of RM 30 per day. That means if you leave on Monday 2200, you will need to pay RM 30 in total; if you leave on Tuesday 0100, you will need to pay RM 60 in total for the rental. 

        The rental rate of the new place is cheaper than the current accommodation. For each day staying in the new accommodation, you need to pay RM 25. However, the renovation of the new place is still ongoing. The renovation can be quantified as a value between 0 and 1, with 0 being completed unrenovated and 1 being fully renovated. You can move in to the place at any renovation level, however, the higher the renovation level, the more comfortable the place is. On Monday 0000, it's estimated that the renovation will be at the level of 0.5. The renovation level at every minute of the week can be estimated with the following function:

        $$\text{renovation level, } \rho = \frac{T^2}{126} + \frac{T}{63} + 0.5$$

        where

        - current time, 
            
            $$T = ( d-1 ) + \frac{60 h + m}{ 24 \times 60}$$

        - day of week, $d$ from 1 as Monday to 7 as Sunday
        - hour of day, $h$ from 0 to 23
        - minute of the hour, $m$ from 0 to 59

        On the other hand, the price for the moving service fluctuates throughout the day. The price of the moving service of a day is calculated with the following function:

        $$\text{price of moving service, } \phi = 50\cos\left(\frac{12\pi t}{24}\right)+50\cos\left(\frac{8\pi t}{24}\right)+150$$

        where

        - current time of day, 
        
            $$t = h + \frac{m}{60}$$

        - hour of day, $h$ from 0 to 23
        - minute of the hour, $m$ from 0 to 59
        - $\cos$ can be implemented with Python's `math.cos(...)` function
        - $\pi$ can be implemented with Python's `math.pi` constant
        
        Determine the optimal time for you to move from the current accommodation to the new place.

    !!! note
        Design your own fitness function

2. Prepare a report that contains
    - problem description,
    - problem formulation,
    - result, 
    - analysis, and
    - discussions.
    
## Logistics

1. This assignment contributes 15% of this course.

2. You will fulfill this assignment in groups of 4 to 5 members.

3. Your submission will be a zipped file (`.zip`) consisting of a report (`report.pdf`) and a folder (`script`) containing your scripts.

4. You are required to submit on MS Teams by **7 October 2021 21:59**. Penalties apply for late submission.

    | Submission by   | Penalties |
    |:---------------:|:---------:|
    | 7 October 21:59 | No penalty |
    | 7 October 23:59 | Obtained marks (out of 15) - 2 |
    | 8 October 11:59 | Obtained marks (out of 15) - 4 |
    | 8 October 16:59 | Obtained marks (out of 15) - 6 |
    
    Submission after 8 October 2021 17:00 will not be marked.
