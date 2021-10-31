# ADM Homework 2
Repository for ADM homework 2

# File description

__`ADM-HW2.ipynb`__: Notebook that contains our answers for both The Research and Theoretical questions

As some markdown text is not displayed correctly, here is a link for an external Jupyter viewer:
https://nbviewer.org/github/onurergun316/ADM-HW2/blob/main/ADM-HW2.ipynb


### In this project we used three different csv files which can be found from the following links:
      https://www.kaggle.com/najzeko/steam-reviews-2021
      https://sapienza2021adm.s3.eu-south-1.amazonaws.com/steam_reviews_bonus_1.zip.
      https://sapienza2021adm.s3.eu-south-1.amazonaws.com/steam_reviews_bonus_2.zip.

### Contributors:
      - Francesco Pinto
      - Onur Ergun
      - Christian Buda

## This homework consists of : 
### 8 Research Questions

1. RQ Exploratory Data Analysis
      
2. RQ Let's explore the dataset by finding simple insights into the reviews.
           
                  - Plot the number of reviews for each application in descending order.
                  - Plot the number of reviews for each application in descending order.
                  - What applications have the best Weighted Vote Score?
                  - Which applications have the most and the least recommendations?
                  - How many of these applications were purchased, and how many were given for free?

3. RQ Now it's important to understand the preferred time to do reviews. 
                  
                  - What is the most common time that authors review an application? For example, authors usually write a review at 17:44.
                  - Create a function that receives as a parameter a list of time intervals and returns the plot the number of reviews for each of the intervals.
                  - Use the function that you created in the previous literal to plot the number of reviews between the following time intervals:
             
Initial Time  |  Final Time
------------- | -------------
  06:00:00    |	10:59:59
  11:00:00    |	13:59:59
  14:00:00    |	16:59:59
  17:00:00    |	19:59:59
  20:00:00    |	23:59:59
  00:00:00    |	02:59:59
  03:00:00    |	05:59:59
            
4. RQ As Steam is a worldwide platform, the reviews can be done in many languages. Let's extract some information about it.
                    
                  - What are the top 3 languages used to review applications?
                  - Create a function that receives as parameters both the name of a data set and a list of languages’ names and returns a data frame filtered only                     with the reviews written in the provided languages.
                  - Use the function created in the previous literal to find what percentage of these reviews (associated with the top 3 languages) were voted as                       funny?
                  - Use the function created in the literal “a” to find what percentage of these reviews (associated with the top 3 languages) were voted as                             helpful?
          
5. RQ The reviews' authors are users from the game that provide their opinion on it. Now you can check how often they make reviews.
                        
                  - Plot the top 10 most popular reviewers and the number of reviews.
                  - What applications did the most popular author review?
                  - How many applications did he purchase, and how many did he get as free? Provide the number (count) and the percentage.
                  - How many of the applications he purchased reviewed positively, and how many negatively? How about the applications he received for free?
 
 6. RQ It's time to get information from the updates that a user does to his reviews.

                  - What is the average time (days and minutes) a user lets pass before he updates a review?
                  - Plot the top 3 authors that usually update their reviews.
                  
 7. RQ Of course, calculating probabilities is a job that any Data Scientist must know. Let's compute Some interesting figures.
                  
                  - What’s the probability that a review has a Weighted Vote Score equal to or bigger than 0.5?
                  - What’s the probability that a review has at least one vote as funny given that the Weighted Vote Score is bigger than 0.5?
                  - Is the probability that “a review has at least one vote as funny” independent of the “probability that a review has a Weighted Vote Score equal                   or bigger than 0.5”?
                  
8. RQ Every decision you take in a data-based environment should be reinforced with charts, statistical tests and analysis methods to check if a hypothesis is correct or not.
            
                  - Is there a significant difference in the Weighted Vote Score of reviews made in Chinese vs the ones made in Russian? Use an appropriate                             statistical test or technique and support your choice.
                  - Can you find any significant relationship between the time that a user lets pass before he updates the review and the Weighted Vote Score? Use                       an appropriate statistical test or technique and support your choice.
                  - Is there any change in the relationship of the variables mentioned in the previous literal if you include whether an application is recommended                     or not in the review? Use an appropriate statistical test or technique and support your choice.
                  - What are histograms, bar plots, scatterplots and pie charts used for?
                  - What insights can you extract from a Box Plot?
    
### 3 Theorotical Questions
1. TQ 1 
                                    
                   Input: 
                   A: array of length n
                   k: integers between 1 and n

                  function alg(A, k):
                    s <-- a random element of A
                    set L = [all the elements of A with value <= s]
                    set R = [all the elements of A with value > s]
                    r = len(L)
                    if k == r:
                      return s
                    else if k < r:  
                      return alg(L, k)
                    else:
                      return alg(R, k - r)
      1- What does the algorithm compute?
      2- What is asymptotically (i.e., we are asking for big-O complexity) the running time of the algorithm in the worst case, as a function of n?
      3- What is asymptotically the running time of the algorithm in the best case?


2. TQ 2

You are given the recursive function splitSwap, which accepts an array a, an index i, and a length n.

               function splitSwap(a, l, n):
              if n <= 1:
                return
              splitSwap(a, l, n/2)
              splitSwap(a, l+ n /2, n/2)
              swapList(a, l, n)
              
      The subroutine swapList is described here:
      function swapList(a, l, n):
  
              for i = 0 to n/2:
                tmp = a[l + i]
                a[l + i] = a[l + n/2 + i]
                a[l + n/2 + i] = tmp


How much running time does it take to execute splitSwap(a, 0, n)? (We want a Big O analysis.)
What does this algorithm do? Is it optimal? Describe the mechanism of the algorithm in details, we do not want to know only its final result.

4. TQ 3

In the knapsack problem we are given n objects and each object i has a weight w_i and a value v_i. We are also given a weight budget W. The problem is to select a set of objects with total weight bounded by W that maximized the sum of their values. The following are three natural heuristics:

      Order them in increasing order of weight and then visit them sequentially, adding them to the solution as long as the budget is not exceeded
      Order them in decreasing order of values, and then visit them sequentially, adding them to the solution if the budget is not exceeded
      Order them in decreasing relative value (v_i / w_i), and then visit them sequentially, adding them to the solution if the budget is not exceeded
      For each of the heuristics, provide a counterexample, that is, an example of a problem instance in which the heuristic fails to provide the optimal solution.


