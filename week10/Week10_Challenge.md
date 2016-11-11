### Week 10 of Data Hackerspace Challenge.

The weekly challenge must be submitted thru Slack to Tyler.

The assignment should be all written in RMarkdown (.rmd) and attach the file on slack.

It's ironic cause this isn't even a RMarkdown file - I'm just lazy :)

Please also include the output of your code somehow in the RMarkdown file for full credit!

- First Deadline:   Sunday 11:59pm
- Second Deadline:  Wednesday 11:59pm  (for 80% of credit)

#### Challenge 1.

The next section contains many “errors” that appear in R code.
Your job is to solve them and explain how you fixed the problem.

```
#1
f = function(x){
  n = a+x
}

f(1)
```
```
#2
p = function(x){
  log(p/(1-p))
}

vals = seq(0, 1, by = 0.1)

p(vals)
```

```
#3
d = c(1, 3, NA, 5, 6, 9)

mean(d) == 1/length(d)*sum(d)
```

```
#4
set.seed(145)

d = sample(1:10, 5)
b = sample(1:10, 5)

if(d > b){
  d+5
}
else {
  b*2
}
```
```
#5
set.seed(1234)

f = function() {
    if (runif(1) > .8) stop("oops")
    TRUE
}

g = function() {
  tryCatch(f(),
           error = function(err) { warning(conditionMessage(err)) }
           )
}

a = replicate(10, g())
if(is.logical(a) && sum(a) > 0){
  cat("We had a few successes!\n")
}
```


#### Challenge 2.

RMarkDown is important.

You can literally do Web-Dev in RMarkdown and RMarkdown only!

##### Round 1
- Download the html for http://xkcd.com/
- Extract the URL for the daily comic.
- Download the comic image to disk.
  - Include the Comic picture inside the R Markdown file.
  - If I appreciate the comic, I might grade easily?

##### Round 2  (optional & for extra credit /s)
- Establish an ```html_session``` with ```rvest``` pointed at https://slashdot.org/.
  - You are only allowed to hardcode https://slashdot.org/
- Navigate to the Science news section of slashdot given at


https://science.slashdot.org/ by having ```rvest``` click the appropriate link. - Scrap all of the titles of the articles on the first and second pages. - Provide the selector information that you used. - Scrap all the URLs given within each of the story descriptions. - Provide the selector information that you used. - List the URLs next to the Titles. - You can embed a ```list``` with the titles inside a data.frame!

#### Challenge 3.

Let's refer back to Week4's challenge. We are going to - whoops, I meant - you guys will be doing the Week 4 Challenges in R!


Here are the links to the Week 4 Challenge + the raw date source
https://github.com/CS196Illinois/Data_Hackerspace/blob/master/week4/NumpyAndPandas.ipynb
https://raw.githubusercontent.com/mwaskom/seaborn-data/master/titanic.csv


###### 1. Calculate the survival rates of passengers by class (First, Second, Third)


##### 2. Calculate the average fare paid by those who survived compared to the fare paid by those who didn't


##### 3. Plot the ages of the female survivors that embarked at Cherbourg
