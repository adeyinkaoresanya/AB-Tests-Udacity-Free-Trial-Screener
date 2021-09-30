# A/B Test: Udacity Free Trial Screener


## Introduction


### **Experiment Overview**


Udacity tested a change on their website where if a potential student clicked the "Start Free Trial" button on the Course Overview page, they were asked how much time they had available to devote to the course. If the student indicated 5 or more hours per week, they would be taken through the checkout process as usual. If they selected fewer than 5 hours per week, a message would appear informing them that Udacity courses usually require a greater time commitment for successful completion and suggesting that the student might like to access the course materials for free. At this point, the student would have the option either to continue enrolling in the free trial, or access the course materials for free instead. It is assumed that the Free trial screener will reduce the number of students who leave the free trial because of lack of time and increase the likelihood of students who continue past the free trial to eventually make payments and complete the course.The overall business objective for this new feature is to increase the likelihood that students who continue past the free trial will make payments and complete their courses.


### **Aim**

The aim of this project is to conduct statistical analysis on the data gathered from the A/B experiment to determine whether there was a significant change caused by the Free Trial Screener and to provide recommendation whether or not to launch this feature.


### **Hypothesis**

H0: There is no significant difference between students who went through the Free Trial Screener and those who did not.

Ha: There is a significant difference between students who went through the Free Trial Screener and those who did not.


## Approach

Confidence interval, z-tests and t-tests were conducted on four metrics to determine if there is a significant difference between those who saw the Free Trial Screener and those who did not.

### **Selected Metrics**



*   **Click-through rate:** This is the number of clicks divided by the number of pageviews. For this experiment, this metric will not move because it can not distinguish the outcomes of the Free Trial Screener between the experiment and control groups, as clicks happened before the Screener popped up. Thus, it will be useful as an invariant metric for checking that the experiment is robust for A/B testing.


*   **Retention:** This is the number of users to remain enrolled past the 14-day boundary (and thus make at least one payment) divided by the number of enrolled students. This metric is expected to increase for the experiment group given that the number of students who go ahead with the free trial reduces without reducing the number of students who are enrolled past 14 days.


*   **Gross conversion:** This is the number of enrolled users divided by the number of clicks. It is assumed that this metric will decrease for the experiment group because the number of enrollments is expected to decrease after answering the Screener question, given  that those who indicated 'Fewer than 5 hours per week' will not be encouraged to enroll.


*   **Net conversion:** This is the number of users to remain enrolled past the 14-day boundary (and thus make at least one payment) divided by number of clicks. This metric is also expected to increase for the experiment group 


### **Datasets**

The datasets used are available [here](https://docs.google.com/spreadsheets/d/1Mu5u9GrybDdska-ljPXyBjTpdZIUev_6i7t4LRDfXM8/edit#gid=0)


### Tools/Libraries required

* [Python 3.9](https://python.org)
* Numpy
* Pandas
* Scipy
* Statsmodel
* Sklearn


## **Significance of metrics under different confidence levels (using t-test results)**

![alt text](https://github.com/adeyinkaoresanya/AB-Tests-Udacity-Free-Trial-Screener/blob/main/src/Results.PNG "t-test results under different confidence intervals")
![alt text](https://github.com/adeyinkaoresanya/AB-Tests-Udacity-Free-Trial-Screener/blob/main/src/Results2.PNG "t-test results under different confidence intervals")


Conclusions about the significance of net conversion do not differ under the different confidence levels because the p-value, 0.593, is very large compared to the different levels of significance. This implies that there is a 59.3% probability of any difference observed being completely random and not due to the change in the experiment.

Whereas, at 60% confidence level, retention rate and gross conversion are statistically significant. However, it is important to note that setting the alpha level at 40% means there is large chance that we might incorrectly reject the null hypothesis, meaning that we conclude there is a change in these metrics when there is really not one, which is a waste of resources for Udacity!


## **Conclusion**

Based on the findings, there is no sufficient evidence to conclude that the Free Trial Screener will increase the likelihood of students to continue past the free trial and eventually make payments or complete the course.


## **Recommendation**

Do not launch the change on the website.


## Contribution

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License

The MIT License - Copyright (c) 2021 - Adeyinka J. Oresanya

[MIT](https://choosealicense.com/licenses/mit/)

