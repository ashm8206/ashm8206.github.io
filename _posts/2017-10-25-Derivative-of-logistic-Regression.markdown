---
layout: post
title:  Derivative of Logistic regression
feature-img: "assets/img/pexels/logistic-regression/cover.jpg"
thumbnail: "assets/img/pexels/logistic-regression/cover.jpg"
tags: [calculus]

---

When taking the andrew Ng's deep learning course , I realized that I  have gaps in my knowledge regarding the mathematics behind deep learning. So today I worked on calculating the derivative of  logistic regression, which is something that had puzzled me previously.
Over the last year, I have come to realize the**importance of linear algebra , probability and stats in the field of datascience.**Mathematics is of core importance for any  CS graduate. However, it is a field thats often overlooked by them.Part of the problem could be that theoretical concepts may seem rather boring in the absence of practical and fun applications to help explain them. Another part could be fear of mathematics. Both these issues can be **easily remedied by having an inquisitive mind.** Sounds rather trite? but allow me to explain.

When I first started taking English seriously(as a non-native speaker), I used to spend hours on the internet, looking up phrases and the right pronouciations of words that were previously unknown to me.I even looked up meanings right in the middle of conversations because I wanted to better my vocabulary. Why am I digressing into this? Well I believe that **to learn something new** you need to develop a love for looking it up in your free time, just for fun. **You need to constantly expose yourself to better articles and better words to get better at describing concepts to yourself and to others(for better understanding).**

**Solution**: Look up mathemmatical concepts for sheer pleasure of diving into something new. It can be anything,even something that has no relevance to you in the present moment. If something seems boring and if you haven't comprehended anything halfway through, drop it and pick up an easier explanation of the same.Eventually **you will come around to understanding and using those "big scary words" or in our case "wickedly involved concepts" with ease.**

Now you might say that there simply is not enough material that explains concepts to us beginners. **Well that's where this blog comes in**.This post is primarily written so that anyone starting off in the field of datascience, can quickly bridge their gaps in calculus and stats.**I also encourage other readers to write and contribute to learning, it does not matter if you are just starting out, just write,publish  get the word out tweet and cite other bloggers on your blog.**In the rare case you do get stuck, dig and dig some more like you would if it were your own pet project.
Without further ado, lets begin.

## Computational graph of logistic regression.
![computational graph]({{ site.baseurl }}/assets/img/pexels/logistic-regression/1.png)

In the above fig, **x** and **w** are vectors and **b** is a scalar. We are consider the case where there are only two input features, below is the compuational graph for that case
![computational graph]({{ site.baseurl }}/assets/img/pexels/logistic-regression/2.png)


## Desired partial derivatives
![computational graph]({{ site.baseurl }}/assets/img/pexels/logistic-regression/3.jpg)


## Strategy for Solving.
![computational graph]({{ site.baseurl }}/assets/img/pexels/logistic-regression/4.jpg)


We consider the chain rule which breaks down the calculation as following
![computational graph]({{ site.baseurl }}/assets/img/pexels/logistic-regression/5.jpg)



Lets look at each component one by one
## Component 1
Remember that the logs used in the loss function are natural logs, and not base 10 logs.
![computational graph]({{ site.baseurl }}/assets/img/pexels/logistic-regression/6.jpg)

## Component 2
Here we take the derivative of the activation function.
We have used the sigmoid function as the activation function

![computational graph]({{ site.baseurl }}/assets/img/pexels/logistic-regression/7c.jpg)

For detailed derivation look below

![computational graph]({{ site.baseurl }}/assets/img/pexels/logistic-regression/7b.jpg)



## Component 3
![computational graph]({{ site.baseurl }}/assets/img/pexels/logistic-regression/8.jpg)



## Component 4
![computational graph]({{ site.baseurl }}/assets/img/pexels/logistic-regression/9.jpg)



## Component 5
![computational graph]({{ site.baseurl }}/assets/img/pexels/logistic-regression/10.jpg)




## Putting it all together
![computational graph]({{ site.baseurl }}/assets/img/pexels/logistic-regression/11.jpg)



![computational graph]({{ site.baseurl }}/assets/img/pexels/logistic-regression/12.jpg)



## Finally

![computational graph]({{ site.baseurl }}/assets/img/pexels/logistic-regression/13.jpg)
We get our desired derivatives



#### Credits
[Ronny Restrepo](http://ronny.rest/blog/post_2017_08_10_sigmoid/)
