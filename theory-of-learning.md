
## Links to theories and ideas about deep learning

### the student becomes the teacher

This is a little more out there for now, but may be interesting to play with. 
A lot of the effort so far in teaching a deep neural network (DNN) 
relies on clever humans generating the models. 

But think about how a child learns as it grows: 
it does not listen (much) to a parent giving specific instructions about the 'right way'
it just tries and tries until it find a way that works more or less right. 

![Sketch overview of Valpola's model](https://thecuriousaicompany.com/wp-content/uploads/2017/12/mean_teacher_L2.png)
`image credit cai.fi the Curious AI Company`

Harri Valpola is a Finn who has dreamt of machines learning in the same way. 
Instead of very clever engineers determining a series of programmatic procedures to develop the best model, 
he decided to let the AI do some of the teaching of the model instead. 
This is the type of abstraction that works in our brains, 
so why should it not work in 'brains' based on the way ours work. 

For a soft introduction, check out 
[the Wired Article from Sep 2017](http://www.wired.co.uk/article/harri-valpola-curious-ai-artificial-intelligence-third-wave). 
If you like what you read move on to 
[his company blog article describing the process](https://thecuriousaicompany.com/mean-teacher/). 
If you want to try it out, see their [Github repo 'mean-teacher'](https://github.com/CuriousAI/mean-teacher), 
but be warned, it needs a large data set to be more efficient at learing than other 'clever' models. 

Toddlers are happy to spend a good few months trying stuff out to get things right, 
but to you have the patience and the stimuli to put in front of a semi-self-teaching 
network to make it work?

