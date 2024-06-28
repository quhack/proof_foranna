https://bookdown.org/annabrown/psychometricsR/

insertions are indicated using `backticks`
deletions are indicated using ~~double tilda~~
some general comments or suggestions are provided as paragraph(s) surrounded by `backticks`

### Preface

#### What is this book for?; para 2
This book can be used for self-study by anybody who want`s` to acquire practical skills in conducting psychometric analyses.

#### How this book is organised; Part III
This part contains 2 exercises, teaching how to fit~~ting~~ a single-factor model to polytomous item scores and to dichotomous item scores.

### Getting Started with R and RStudio
(No comments)

### INTRODUCTION TO PSYCHOMETRIC SCALING METHODS

#### Exercise 1; 1.2 Study of a community sample using the Strength and Difficulties Questionnaire (SDQ)
The Strengths and Difficulties Questionnaire (SDQ) is a brief behavioural screening questionnaire about children and adolescents of 3-16 year`s` of age.

#### Exercise 1; step 1:
You should see a new object SDQ appear on the Environment tab (top right RStudio panel). This tab will show any objects currently in the workspace, and the data frame SDQ was ~~stoerd~~ `stored` in file SDQ.

There is `a` Gender variable (0=male; 1=female), followed by responses to 25 SDQ items named consid, restles, somatic etc.

Item variables reflect `the` key meaning of the actual SDQ questions, which are also attached to the data frame as labels.

#### Exercise 1; step 3:
Normally, we could use `the` base R function rowSums(), which computes...

This is because the default option for dealing with missing data in `the` rowSums() function is to..

We will use `the` rowMeans() function to compute the mean of those item responses that are present...

#### Exercise 1, section 1.3, step 4:
`The histogram has a large first column becuase it contains both 0 and 1 values combined into one column without adjusting the width. R defaults to the Sturges method for defining columns in histograms, you could potentially use an alternative method, or just point it out given it graphically illustrates your point about the floor effect.`

#### Exercise 1, section 1.3, step 5:
A few non-integer scores must not worry you. They occurred due to computing the scale score from the item means for some pupils with missing responses. For all cases without missing responses, the resulting scale score`s` will be integer`s`.

#### 1.4 Worked Example 2; step 2

To reverse–code this item, we will use a dedicated function of `the` psych package...

#### 1.4 Worked Example 2; step 3

Because there are missing responses (particularly for Time 2), we will use `the` rowMeans() function...

#### Exercise 1, section 1.5
Repeat the steps in the Worked Example 1 for the Pro-social facet. NOTE that just like the Emotional Symptoms scale, the Pro-social scale does not have any counter-indicative items. For computing scale scores for other SDQ facets, you will need to reverse code such items, which we ~~will learn~~ `learned` in the second Worked Example. ~~Then, you will be able~~ `Use the techniques learned in the second Worked Example` to practice this exercise with the remaining SDQ scales.

#### 1.6 Solutions

If you call SDQ$S_conduct2, you will see that there are many cases with `a` missing score, labelled NaN.

#### 3.2 Worked Example; Step 1

Files in foreign to R formats are not “loaded” but ~~“red”~~ `“read” instead.

#### 3.2 Worked Example; Step 3

`When I've followed the steps the x-axis of each plot has the category labels (agree/ disagree) rather than an index along the x-axis`

#### 4.3 Worked Example; Step 1

You can press on `the` JobFeatures object. This will make `the` View(JobFeatures) command run...

#### 4.3 Worked Example; Step 2

`Technically the function is defined with *parameters* and the user passes *arguments* so suggested draft as follows`

Each component in the parentheses is ~~called~~`a placeholder for an` “argument”, and so `the` thurstone() function ~~has~~ `accepts` three arguments.

#### 4.3 Worked Example; Step 3

You can check what is stored inside any of these constituent parts by ~~referring to them by full name - starting with scaling followed by the $ sign~~`prefixing the part name with "scaling$"`...

Let’s examine the “choice” matrix more carefully. Look for the entry in row [8] and column [6]. This value, 0.8526413, represents the proportion of participants who preferred `the` 8th feature, Competition, to `the` 6th feature, Development, and it is the largest value in the “choice” matrix

QUESTION 2. How does the above result for choices for `the` 8th feature, Competition, ~~oevr~~`over the` 6th feature, Development, correspond to the estimated utility means?

#### 4.4 Solutions

This means that `a` Competitive environment was least wanted...

Other features were scaled somewhere between these two, with Safety having `a` low mean (0.23) - barely higher than 0 for ~~Competition~~`**Competition**`, whereas Support, Challenge, Career and Ethics ~~having~~`have` similarly high means (around 0.9).

(`the` 6th feature, Development, must have a much higher mean utility than `the` 8th feature, Competition)

This result is indeed in line with the results for the utility means, where `the` Development mean was the highest at 1.04 and Competition was the lowest at 0.

### CLASSICAL TEST THEORY AND RELIABILITY THEORY

#### 5.3 Worked example; Step 3 para 4

This will ensure that statistics in the output are given for the sum score (“cumulative” of item scores) rather than for the average score ~~(deafult)~~**(default)**.

#### 5.3 Worked example; Step 3 Question 2

“the proportion of variance in the observed score due to **the** true score”

6.2; para 2

On **the** contrary, the EPQ scales are measured...

6.3 Worked example; Step 1; para 2

*This suggestion is stylistic rather than the typos/ omissions I've generally listed - just to make it clear we're not passing the arguments at all if we're happy with the defaults*

Other arguments all have defaults, so you ~~change~~specify them only if necessary.

6.3 Worked example; Step 2; para 1

Analyses in this ~~Exercise~~exercise will require...

6.3 Worked example; Step 4

Now let’s estimate the “internal consistency reliability” (Cronbach’s alpha) of the total score. We apply function alpha() from **the** psych package to all 23 items of the SDQ data frame. Like in Exercise 5, I suggest ~~to obtain~~obtaining output for the sum score (which we computed) rather than average score (deafult in alpha()).

6.3 Worked example; Step 4; para under Question 4

Yes, you can get these statistics without computing the test score ~~but~~ by just running function alpha().

6.3 Worked example; Step 4; para above Question 5

In the “Item statistics” section of the output, an interesting statistic...

6.3 Worked example; Step 5; para 3

Note that because you pass ~~to the function~~ the correlations **to the function** rather than the raw scores, no statistics for the “test score” can be computed and you cannot specify the type of score using **the** cumulative option.

Part III. Test homogeneity and Single-Factor Model

7.2 Worked example; step 2

There is **a** Gender variable (0=male; 1=female), followed by...

7.2 Worked example; step 2

Kaiser (1975) table for interpreting MSA - first two twos need aligning.

-- STEP 7 --

"We are hoping to retain this hypothesis, therefore hoping for a **large** p-value, definitely p > 0.05, and hopefully larger."

Is "large" the right word here? 
