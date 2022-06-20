---
title: "Code Review"
teaching: 0
exercises: 0
questions:
- "Why is code review important for reproducibility?"
- "What curation activities are associated with code review?"
objectives:
- "Basic understanding of what is involved in code review"
- "Providing examples of common code issues when attempting computational reproducibility"
keypoints:
- "Difficulties with executing code can prevent computational reproducibility." 
- "Researchers should write code with reproducibility in mind."
- "Curators reviewing the code can take steps to ensure that it is executable and documented to facilitate reproducibility."
---

**Data generating, cleaning, or transformation:**
~~~
//Labeling variables
label variable treatment "The manipulation group"
label define treatment1 1 "$4" 2 "$"
label variable treatment treatment1
label variable pieces "How many pieces of pizza did you eat today?"
label define ideolab -3 "V. Lib." -2 "Lib." -1 "S. Lib." 0 "Middle" 1 "S. Cons." 2 "Cons." 3 "V. Cons." 4 "" 5 "DK/Can't place"
 
//recoding variables
recode region (1/2=1 "Northeast") (3/4=2 "Midwest") (5/7=3 "South") (8/9=4 "West"), gen(region_4cat)
 
//generating variables
generate gp100m = 100/mpg
label var gp100m "Gallons per 100 miles"
~~~
{: .source}

{% include links.md %}