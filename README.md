###First ***Gradient decsent***

*"Minimizing cost, step by step to negative gradient"*

Getting X,Y from the data, where X is features(Rm*n) and y is bias(Rm). 

After which we are findind sigmoid (the activator) it will give a probability of class being 1 "input->prob(0,1)"
which is


**1/1+exp(-z)**

Now we need prediction (X,w,b)


a= sigmoid(**Z=X*w+b**)=> y_pred


//i used epsilon to avoid log(0) but it should work without it too

binary cross-enropy loss function=

  ** -(ylog(y_pred)+(1-y)log(1-y_pred)) **


*log(y_pred)*-> positive class term    
*(1-y)log(1-y_pred)*-> negative class term     
then summing across all samples and finding avarage by /m 

used regularization term *L2 penalty*

 **J(w,b) = \text{loss} + \frac{\lambda}{2m} \sum_j w_j^2**

it gives more **balanced weights**, basically prevents overfitting, which is what we need for the better model;)
