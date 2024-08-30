# Housing Price Predictor


## Author's context:
I've built out some basic web apps, but this would be my first AI/ML project.

## What I built:
- Using ML (supervised learning), I discovered the best way to predict an individual house's market value based on parameters such as size, location, and age (much like Zillow.com's Zestimate feature) At a high-level:

    ### Data Collection:
  - Leaned on existing, but imperfect, dataset from the public web

  ### Data Exploration and Preprocessing:
  - Addressed missing values and employed encoding

  ### Model Selection & Training:
    Per textbook, I sampled only 3 common methods and then measured stats like MSE, RMSE and R-Squared:
  - Linear Regression (eventual winner)
  - Decision Tree Regression
  - Random Forest Regression

  ### Model evaluation:
  - Scores represented as MSE, RMSE, R^2
  - Cross validation, which is kind of like a tournament of the 3 players (competing models) involved 

  ### Conclusion:
  - INTENTIONALLY LEFT BLANK

## New technical achievements:
>**JUPYTER**
Up until now, I have always used Pycharm to print out statements to test my code. The first benefit I noticed to this was the ability to display visuals

>**PANDAS**
Since I got my start on LeetCode, my original training forced me to use only the core Python functions for solving problems, and I never used libraries like NumPy or Pandas to do calculations. Now I see that Pandas is kind of like giving Python a path to SQL-like queries: "Group this data by X, then return Y description such as an average or a count"

>**MATPLOTLIB**
I had seen in a YouTube parody how Python can produce visuals, but I never knew how. This is the visualization tool.

>**SCIKIT-LEARN / SKLEARN**
I never heard of this tool, because I haven't touched anything related to data science or ML.

>**NumPy**
Heard of this many times during my LeetCode days, but never touched it because it would be cheating during an interview. Just used it to produce a stratified sampling (by median household income), followed by first histogram

>**SciPy**
Never heard of this before, but just used it convert string data in the ocean proximity dimension into multiple columns i.e. One-Hot Encoding


## Sample screenshots:


## Learnings:
- There's a complementary tool "Hugging Face" I could use in future projects to host data, if viewers need more evidence beyond screenshots.
- Don't be surprised if your requirements.txt only lists 6 libraries, but your installation produces 20 packages. This is the result of a "dependency chain"
- Jupyter can be powerful because it allows you to see visual outputs (see later comment about matplot)
- When I got the section about splitting data into 2 sets, I learned that a function can return multiple outputs, so long as they are in tuples (not something you'd ever see on LeetCode)
- I always knew that tuples were like an immutable version of a list, but there was never a need to use them on LeetCode because the memory savings wasn't worth the trouble. Now I see that tuples, because they are locked-in, could be used as a dictionary key, which might have impacted my strategy for solving the DSA question in my first technical interview!
- In the famous Django tutorial by the University of Michigan professor, he mentions "42" as a survey answer. This tutorial asks us to pick "42" as an arbitrary seed value or random version number, cluing me in to engineering's inside-joke from that book "Hitchhiker's Guide to the Galaxy" 
- There's 2 ways we can randomly pull 80% of data and set it aside for training:
  - Method 1 is using latitude+longitude to make an non-random index ID, making it random via hash values, sorting by hash values, then taking the bottom 80% for training
  - Method 2 is using SciKit to skip ahead to the final step: randomly put 80% of the rows into the training bucket.
  - The point is that you need 1 or 2, but not both at same time.
- During stratified sampling, we set up "bins" just like in our Tableau days to divide districts by household income (bottom group 1 being < $15,000). Out of 20K districts, we found that ~4% were in group 1 income range, so the stratified sampling will ensure 4% of the training data prioritizes pulling random rows that are in that income range.
- When switching machines, I had to re-install 6 packages and I didn't know realize until that moment how large some of the libaries were, and how the internet can be so slow it gives timeout errors. Might be smart to prep devices before entering a cruise ship or a flight
- You can get the same randomized outcomes based on the seed value across multiple devices - it doesn't mean there was no randomness!

## Potential improvements:
>**PLACEHOLDER:**<br>
placeholder text