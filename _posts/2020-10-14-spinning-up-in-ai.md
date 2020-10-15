---
layout: post
title: Spinning Up in Active Inference and the Free Energy Principle
description: A Syllabus for the Curious
toc: True
comments: true
hide: True
---

A few months back I posted the first part of [an introduction to the Free Energy Priniple](https://jaredtumiel.github.io/blog/2020/08/08/free-energy1.html). I did this because it's fascinating and important, and yet sometimes comically difficult to learn about. A big part of the problem is probably [Research Debt](https://distill.pub/2017/research-debt/) - a dearth of digestible translations of the current cutting edge research into accessible language. This is the problem I'm trying to solve with my Intro posts. Another problem is that there is no well-defined syllabus of material that you could aim to complete such that, at the end, you have the necessary theoretical background to grok the theory in its full glory, and can feel confident that you have a reasonably complete map of the territory. A syllabus should gradually shorten the [inferential distance](https://www.lesswrong.com/posts/HLqWn5LASfhhArZ7w/expecting-short-inferential-distances), taking you from a complete beginner, and gradually increasing the detail and technicality.

This syllabus includes short descriptions of each entry, so that it also functions as a high-level overview of how the various parts of the theory fit together. The syllabus ends with a list of the biggest unsolved challenges and open problems in the FEP/Active Inference scene. If you have suggestions, let me know on [Twitter](https://twitter.com/jnearestn)!

## How to use this syllabus

Generally, you should [Dive In](http://mindingourway.com/dive-in/). Don't wait to finish all the prerequisites before you try getting your head around the theory. Jeremy Howard from Fast.ai has this great line about playing around with a system *before* you fully understand it, and once you have a feel for it, only then do you go learn the technical details. So even though this list starts with "prerequisites", treat that as a placeholder, go until you get stuck, and then come back and see if you can find the answer to the stuck-feeling in one of the prerequisites. 

I've also tried to have a hierarchy of materials within each category, starting with short, intuitive primers and ending with longer, more difficult technical material that only becomes relevant as your interests deepen. There isn't a strict order to the materials, which is why it's probably better to go iteratively deeper across categories as needed.

## Prerequisites

### Neuroscience

The FEP came out of Karl Friston's neuroimaging work, so it shouldn't be surprising that neuroscience is a key competency.

#### Predictive Coding/Predictive Processing

Predictive coding is a theory of how the brain works that inverts the traditional "bottom-up" feature detection view and replaces it with the brain generating top-down predictions instead. When a prediction does not match with what is actually observed, an error signal is passed up through the brain and changes take place to minimise the prediction error in the future. 

Predictive processing is closely associated with the FEP, and naturally "emerges" from the equations governing the FEP. In this sense, understanding PP is helpful to have an intuitive view of what the FEP achieves in the brain.

- [It's Bayes All The Way Up](https://slatestarcodex.com/2016/09/12/its-bayes-all-the-way-up/) by Scott Alexander [blog]
  - Scott has a great series of posts on Bayesian brain hypotheses. A nice way to get some intuitions!
- [Bit of a Tangent](https://open.spotify.com/episode/61WphINy1mdxCIwUDnEG2M) [podcast]
  - This is cheating, but we did a series of three podcasts on PP, so check those out if you prefer audio
- [Surfing Uncertainty](https://www.amazon.com/Surfing-Uncertainty-Prediction-Action-Embodied/dp/0190217014) by Andy Clark [book]
  - This technical book gives a deep introduction to much of the theory behind PP, but still manages to be accessible to non-neuroscientists (I'm not one). It's really good for getting an overview of the PP literature and the flavour of this view of the brain!
  - Scott Alexander also has a great review of the book [here](https://slatestarcodex.com/2017/09/05/book-review-surfing-uncertainty/)

#### Computational Neuro and modelling techniques

Part of the appeal of the FEP is that it might lead to improved models of the brain and biological intelligence. Learning to set up experiments, design simulations, and implement models of neural systems in code is a big part of turning the theoretical results of the FEP into a powerful set of new tools and applications!

- [Neuromatch Academy](http://www.neuromatchacademy.org/syllabus/) 
  - This is a fully-online Summer School with all the materials freely available. It includes all of the content you need to get started in computational neuroscience and includes deep learning and reinforcement learning content too! The content has been created and curated by a great team of researchers and their explicit goal is to train people from diverse backgrounds in computational neuroscience!
- [The Imbizo](http://imbizo.africa/) [Summer School/Course]
  - If/when international travel ever becomes possble again, I cannot more strongly recommend attending the annual Computational Neuroscience 'Imbizo' in Muizenburg, South Africa. It's basically a three week crash course in computational neuroscience with a bunch of awesome speakers and students. It's easily the most fun I had in 2020, and I learnt a tonne!
- [Computational Psychiatry course](http://www.translationalneuromodeling.org/cpcourse/)
  - One of the promises of the FEP is a new understanding of the computational basis of psychiatric disorders such as depression, schizophrenia, ADHD, bipolar-mood disorder and others. This course is an introduction to understanding these conditions computationally and mathematically. The course materials are all online, and Karl Friston himself has given some of the lectures in previous years!

### Physics

The Free Energy Principle wants to explain how we, as biological organisms obeying the laws of physics, can self-organise into complicated creatures that maintain our complexity despite ([or because of](https://kaiu.me/2019/10/09/life-and-the-second-law/)) dissipative forces. The FEP rests solidly on the ideas of modern physics, so the more you know here the better!

#### Statistical Mechanics

Entropy, Free Energy, non-equilibrium steady states - these ideas are front and centre in the FEP literature and all come from stat-mech. If you were going to spend your time learning about only one area of physics to really have a good basis in the FEP, this is probably the one you'd pick.

- [Statistical Mechanics in The Theoretical Minimum](http://theoreticalminimum.com/courses/statistical-mechanics/2013/spring) by Leonard Susskind [lecture course]
  - Leonard Susskind is a hero to me. I've heard more than one person say that they did multiple stat-mech courses and the derivation of the partition function was never as magically clear as Susskind's. If you've never done any stat-mech, this is a good place to start!
- [Statistical Mechanics: A Set of Lectures](https://www.amazon.com/Statistical-Mechanics-Lectures-Frontiers-Physics/dp/0201360764) by Richard Feynman [textbook]
  - The Feynman Lectures on Physics are rightly famous for their explanatory clarity, but less well-known are his lectures on statistical mechanics! Worth reading just because it's Feynman!

#### Non-equilibrium Statistical Mechanics

Of course, the FEP deals with living systems, and living means being far from thermodynamic equilibrium, so we'll want to understand how to describe these systems mathematically. The big ideas that come up often are non-equilibrium steady states, as well as the Langevin and Fokker-Planck equations.

- [Non-equilibrium Statistical Mechanics](https://www.youtube.com/watch?v=SjTfNFso4mE&list=PLbMVogVj5nJQqNx0ElSk3Ip04Ofg7B22W) by the Indian Institute of Technology Madras [lecture videos]
  - Professor Balakrishnan is legendary on YouTube for the clarity of his explanations. The course is genuinely great and includes lots of detailed explanations of the Langevin and Fokker-Planck perspectives on dynamical systems!
- [A Worked Example of Fokker-Planck based Active Inference](https://slideslive.com/38933123/a-worked-example-of-fokkerplanck-based-active-inference) by Magnus Koudahl & Bert De Vries [video]
  - This is a great direct introduction to using the Fokker-Planck equation in the FEP! It's especially useful if you've read a few papers and can't make sense of the notation - this is the clearest description I've found!
- [Nonequilibrium Statistical Physics: A Modern Perspective](https://www.amazon.com/Nonequilibrium-Statistical-Physics-Modern-Perspective/dp/1107049547) by Livi & Politi [textbook]
  - Both this book and the one below contain detailed derivations of the techniques used for non-equilibrium stat mech. They're both similar, but Attard's book has more focus on entropy and the second law of thermodynamics, whereas Livi spends more time on critical phenomena. 
- [Non-equilibrium Thermodynamics and Statistical Mechanics: Foundations and Applications](https://www.amazon.com/Non-equilibrium-Thermodynamics-Statistical-Mechanics-Applications/dp/0199662762) by Attard [textbook]


#### Classical Mechanics, Hamiltonian Mechanics, and the Principle of Least Action

Friston sometimes frames the FEP in terms of a principle of least action, where action is an integral over a nice object called a Lagrangian. Lagrangians and Least Action principles give us a really powerful way to describe the equations of motion, symmetries, and conservation laws of our system, so knowing about this approach is really worthwhile. That being said, this approach doesn't feature prominently in the basic formulation of the FEP, so don't get stuck here!

- [Classical Mechanics](https://theoreticalminimum.com/courses/classical-mechanics/2011/fall) by Leonard Susskind
  - Like his Stat-Mech course, Susskind does a good job of getting the main ideas across with just enough maths to allow you to understand more formal treatments later.


#### Gauge theory

Gauge theory is a way of describing how certain symmetries in our system can lead to new properties/forces. It's not a big part of the core theory, but I include it here because it's a personal favourite, and Friston and collaborators have dabbled in applying some gauge-theoretic ideas to the FEP.

- [Gauge Theory - The Biggest Ideas in The Universe](https://www.youtube.com/watch?v=AuqKsBQnE2A&list=PLrxfgDEc2NxZJcWcrxH3jyjUUrJlnoyzX&index=30) by Sean Carroll
- [Physics From Finance: A Gentle Introduction to Gauge Theories](https://www.amazon.com/Physics-Finance-introduction-fundamental-interactions/dp/1795882417) by Jakob Schwichtenberg [textbook]
  - This is about as an intuitive introduction to the idea as you could ever get. Schwichtenberg actually starts off with an easy financial model and then uses that analogy to build up to the use of gauge theories in particle physics. 

### Maths

I kind of want to say that I'm taking it for granted that you know at least a bit of [multivariable calculus](https://ocw.mit.edu/courses/mathematics/18-02sc-multivariable-calculus-fall-2010/), some [linear algebra](https://ocw.mit.edu/courses/mathematics/18-06-linear-algebra-spring-2010/), and some [probability theory](https://ocw.mit.edu/resources/res-6-012-introduction-to-probability-spring-2018/) (the FEP people definitely assume this, and more), but also *I* didn't know any of those things when I started (not so long ago!) and felt really helpless when they were just assumed, so the above links go to the MIT OpenCourseware courses I used to get going!

#### Bayesian inference

The FEP fundamentally deals with agents trying to infer the state of their environment, given their current sensory data. Whenever you have a sentence like that, Bayes' Theorem can't be far behind! Understanding, on a gut level, the mechanics of how Bayes works, and being able to fluidly work with the different forms of the formula (knowing some basic identities in terms of joint distributions and marginal distributions) generally makes a lot of things in the FEP clearer!

- [An Intuitive Explanation of Bayes' Theorem](https://yudkowsky.net/rational/bayes/) by Eliezer Yudkowsky [blog]
  - I link to this article all over the place because it's just so good. It won't teach you to use Bayesian techniques in your machine learning model, but it will teach you why you'd want to!
- [Probability Theory: The Logic of Science](https://www.amazon.com/Probability-Theory-Science-T-Jaynes/dp/0521592712) by E.T. Jaynes [textbook]
  - Rederiving probabilitiy theory from scratch might be overkill, but this book sort of reads like the Feynman Lectures, but for probability theory. Be sure to grab the [unofficial errata](http://ksvanhorn.com/bayes/jaynes/index.html)
- [Machine Learning: A Probabilistic Perspective](https://www.amazon.com/Machine-Learning-Probabilistic-Perspective-Computation/dp/0262018020) by Kevin Murphy [textbook]
  - This is pretty lengthy but for the first 3 chapters (reintroducing key ideas in machine learning, probability theory, and generative models) are a quick way to get up to speed with a lot of the jargon, if you've already done a bit of probability theory beforehand! Chapter 5 on Bayesian statistics and chapter 21 on variational inference (see below) are especially relevant to the FEP!


#### Information theory

Entropy, confusingly, moonlights as a term in information theory. Not only that, but since much of the FEP is about a system inferring the state of a hidden (latent) variable through its noisy sensory signals, the techniques of information theory (invented by Claude Shannon for almost exactly that kind of problem) are key. Information theory also teaches us about the Kullback-Liebler divergence, which is worth knowing just on its own!

- [Shannon Entropy and Information Gain](https://www.youtube.com/watch?v=9r7FIXEAGvs&t=7s) by Louis Serrano [video]
  - This is a good intro video covering a lot of what you need to know when you're just getting started
- [A Short Introduction to Entropy, Cross-Entropy, and KL-Divergence](https://www.youtube.com/watch?v=ErfnhcEV1O8) by Aurélien Géron [video]
  - I've watched this video at least 5 times. It's a brilliant introduction to some genuinely challenging concepts in a way that leaves you feeling like everything finally makes sense!
- [Information Theory, Inference, and Learning Algorithms](https://www.inference.org.uk/itprnn/book.pdf) by David MacKay [textbook]
  - This freely available textbook contains a lot more detail than the two intro videos. It's a good place to look if you have nitty-gritty information theory questions.

#### Information geometry

Depending on your feelings about math, information geometry is either a sort of sublime union of differential geometry and statistics, or a Frankenstein's Monster of two other monsters. Information geometry lets us do statistics on manifolds, which seems arbitrary (especially if you don't know what a manifold is), but might be useful, and is at least very cool to say to your friends. Friston occasionally mentions the term, so this is here as a reference you can return to for when he does.

- [Information Geometry](https://math.ucr.edu/home/baez/information/) by John Baez [notes]
  - These notes are packed with insights about geometry, entropy, dissipative forces, and more! Most importantly, they feature a neat derivation of the Fischer Information Metric, which is a big part of the field. I really enjoy the way that John C. Baez explains maths - he manages to make me feel like I really could have *done that* when he derives something. A bonus of these notes is Baez riffing on how this information geometry applies to evolutionary systems, and the relative entropy (aka the KL-divergence!), so you can see a lot of the bread and butter of the FEP infused into this field!

### Computer science and machine learning

The FEP will remain an intriguing bit of mathematical theory if good programmers don't start to find ways to apply the ideas to problems in artificial intelligence and machine learning. On the other side, ideas from AI/ML are key to understanding where the FEP and Active Inference can fit in and what the current state-of-the-art is.

#### Deep Learning

Deep learning has been so damn successful that it's worth knowing about just for that. Neural networks are great function-approximators, which can be useful in the FEP *Kaui article*. Also, the standard deep learning libraries (PyTorch/Tensorflow etc.) are worth learning because they make it really easy to build flexible models using current best-practices, and they make things like autodifferentiation and optimisation easy!

- [fast.ai](https://course.fast.ai/) by Jeremy Howard and Rachel Thomas [course]
  - An excellent, practical introduction to state of the art techniques in modern deep learning. Emphasis on deploying models. Worth it just for the Jeremy's wisdom.
- [Advanced Deep Learning and Reinforcement Learning](https://www.youtube.com/watch?v=iOh7QUZGyiU&list=PLqYmG7hTraZDNJre23vqCGIVpfZ_K2RZs) by DeepMind
  - A more detailed course which picks up a lot of the detail that Fast.ai leaves out. It's by Deepmind so the content is good quality!
- [Deep Learning Book](https://www.deeplearningbook.org/) by Ian Goodfellow, Yoshua Bengio, and Aaron Courville
  - Not so relevant to the FEP, but so so good and freely available that you might as well browse it! If you ever want to know more about deep learning, it also has a great set of introductory chapters on calculus, linear algebra, and probability theory, which just give enough to get started in the general area, rather than doing entire university courses!

#### Reinforcement Learning

RL is the current established field for creating autonomous, intelligent agents that can interact with their environments. Knowing the basics of how RL has approached intelligence, what kinds of techniques are available, and their limitations, helps us put the FEP in context. RL also deals heavily with Markov chains, the Markov property, and has established techniques for programming these kinds of agents, all of which can be transferred into the design of FEP-style agents.

A nice side-effect is that RL has a bunch of established benchmarks and environments for testing how intelligent an agent is, and I think it's key to the future of the FEP/Active Inference that their techniques can be shown to compete with and eventually outperform the pure-RL models.

- [Introduction to Reinforcement Learning](https://www.youtube.com/watch?v=2pWv7GOvuf0&list=PLqYmG7hTraZDM-OYHWgPebj2MfCFzFObQ) by David Silver [lecture videos]
  - The classic intro course!
- [CS285: Deep Reinforcement Learning](https://www.youtube.com/watch?v=SinprXg2hUA&list=PLkFD6_40KJIwhWJpGazJ9VSj9CFMkb79A) by Sergey Levine [lecture videos]
  - Where the DeepMind course with David Silver introduces the ideas of traditional RL, this course goes into the details of modern deep RL
- [OpenAI Spinning Up in Deep RL](https://spinningup.openai.com/en/latest/)

#### Variational inference

At the start of your journey into the FEP, you'll keep hearing about 'surprisal', 'the ELBO' (evidence lower bound), 'variational Bayes', and 'model evidence'. For whatever reason, I took too long to just go and find out that all of these ideas are well established and well explained in the field of variational inference

- [Variational Inference and Deep Learning: An Intuitive Introduction](https://www.youtube.com/watch?v=h0UE8FzdE8U) by Alex Lamb [video]
- [Variational Inference: Foundations and Innovations](https://www.youtube.com/watch?v=Dv86zdWjJKQ) by David Blei [video]
- [Machine Learning: Variational Inference](https://www.youtube.com/watch?v=2pEkWk-LHmU) by John Boyd-Graeber [video]
- [Variational Algorithms for Approximate Bayesian Inference]((https://cse.buffalo.edu/faculty/mbeal/papers/beal03.pdf)) by Matthew Beal [Thesis]
  - The PhD thesis Friston cites frequently - the source of many of the key equations used in the FEP
- [Derivation of the Variational Bayes Equations](https://arxiv.org/abs/1906.08804) by Alianna Maren [paper]
  - A friendlier explanation of Beal's thesis, specifically for the FEP!

#### Generative models

Close your eyes and imagine a red bus! If you can do it, maybe that counts as evidence to you that your brain has some sort of generative model (i.e. can imagine/synthesise data points). More generally, generative modelling tries to explain the data we're observing as being generated by some smaller set of variables. The FEP deals heavily with the language and ideas of generative models, so reading up on directy is helpful!

- [Modern Latent Variable Models](https://www.youtube.com/watch?v=7Pcvdo4EJeo) by DeepMind & UCL [video]
- [Probabilistic Graphical Models](https://www.youtube.com/watch?v=oqvdH_8lmCA&list=PLoZgVqqHOumTqxIhcdcpOAJOOimrRCGZn) by Eric Xing (also see course website [here](http://www.cs.cmu.edu/~epxing/Class/10708-20/lectures.html) [video lectures]
  - I enjoy this course for taking a different perspective on ML/DL. There's a lot of variety, but the course has videos on variational inference and generative models. There are also slides and course notes [here](http://www.cs.cmu.edu/~epxing/Class/10708-20/lectures.html)
  
## The Free Energy Principle and Active Inference

The main event!

### General introductions

- [God Help Us, Let's Try To Understand Friston on Free Energy](https://slatestarcodex.com/2018/03/04/god-help-us-lets-try-to-understand-friston-on-free-energy/) by Scott Alexander [blog]
- [Karl Friston on Brains, Predictions, and Free Energy](https://www.youtube.com/watch?v=TcFLQvz5uEg) by Sean Carroll on The Mindscape Podcast [podcast]
  - Sean's interview with Karl Friston is my favourite of his 'popular' appearances. Sean Carroll really got some great detail and explanations from Friston
- [Karl Friston: Neuroscience and the Free Energy Principle](https://www.youtube.com/watch?v=NwzuibY5kUs) by Lex Fridman [podcast]

### Technical introductions

- [Active Inference Podcast](https://www.youtube.com/watch?v=C94WDXAe4EE&list=PLNm0u2n1Iwdoe-4Be7frRpvBQ0q7yhnBV) by [@InferenceActive](https://twitter.com/InferenceActive)
  - This is a weekly podcast/journal club on the FEP/Active Inference. They're detailed and the participants are active researchers in the field, so it's a great way to hear their thoughts on some of the field's key papers 
- [Tutorial on Active Inference](https://medium.com/@solopchuk/tutorial-on-active-inference-30edcf50f5dc) by Oleg Solopchuk [blog]
- [How To Read Karl Friston in The Original Greek](https://www.aliannajmaren.com/2017/07/27/how-to-read-karl-friston-in-the-original-greek/) by Alianna Maren [blog]
- [The Free Energy Principle and Active Inference](https://kaiu.me/2017/06/23/deep-active-inference-for-artificial-general-intelligence/) by Kai Ueltzhöffer [blog]
  - This post and the two below it are my favourite blog posts on the FEP. They come with enough math to understand it on a deep level, the explanations are intuitively satisfying, and  I really enjoy the 
- [Introducing The Deep Active Inference Agent](https://kaiu.me/2017/07/11/introducing-the-deep-active-inference-agent/) by Kai Ueltzhöffer [blog]
  - A great technical discussion of using deep learning to improve active inference! Notably, there is working code you can play around with and a [paper on arXiv](https://arxiv.org/abs/1709.02341) going into more detail
- [Life and The Second Law](https://kaiu.me/2019/10/09/life-and-the-second-law/) by Kai Ueltzhöffer [blog]
- [Active Inference and Artificial Curiosity](https://www.youtube.com/watch?v=Y1egnoCWgUg) by Karl Friston [video]
- [Predictive Coding Workshop](https://www.youtube.com/watch?v=b1hEc6vay) by Karl Friston [video]
- [A Tutorial on Active Inference](https://www.youtube.com/watch?v=WzFQzFZiwzk) by Maxwell Ramstead [video]
  - This is a really well explained intro to both the FEP and active inference. Big bonus is that it includes a great explanation of Markov Blankets, which you'll definitely want to know about!
- [International Workshop on Active Inference](https://iwaiworkshop.github.io/#programme) [videos]
  - ECML-PKDD 2020 hosted the first ever International Workshop on Active Inference! This a big deal for the field as a whole, both because active inference got an entire workshop devoted to it at a mainstream machine learning conference, and because created a great  space to find more people working in the field! The video tutorials are all available to watch, and come paired with the slideshows. There were too many good talks to list them all, so go check the programme page above! Some talks I particularly enjoyed were:
    - [Active Learning and Active Inference in Exploration](https://slideslive.com/38933135/active-learning-and-active-inference-in-exploration) by Philipp Schwartenbeck
    - [Putting An End to End-to-End: Gradient-Isolated Learning of Representations](https://slideslive.com/38933137/putting-an-end-to-endtoend-gradientisolated-learning-of-representations) by Sindy Löwe
    - [On the relationship between active inference and control as inference](https://slideslive.com/38933114/on-the-relationship-of-active-inference-and-control-as-inference) by Beren Millidge, Alexander Tschantz, Anil Seth and Christopher L. Buckley, and the closely related [Active Inference or Control as Inference? A Unifying View](https://slideslive.com/38933122/active-inference-or-control-as-inference-a-unifying-view) by Abraham Imohiosen, Joe Watson and Jan Peters
    - [A Worked Example of Fokker-Planck based Active Inference](https://slideslive.com/38933123/a-worked-example-of-fokkerplanck-based-active-inference) by Magnus T. Koudahl and Bert de Vries

### Key papers

This list is as much a list of some of the most fascinating directions of research in the field as it is a general overview. The hope is that the ideas in some of these papers sound so cool that you can't help but want to take the ideas further (that was my experience, and that's why I'm still here!).
Rereading this list, I can see it's skewed by my own research interests, so let me know what other sections/papers should be added!

- **General**
  - [The Free Energy Principle for Action and Perception: A Mathematical Review](https://arxiv.org/abs/1705.09156) by Christopher L. Buckley, Chang Sub Kim, Simon McGregor, Anil K. Seth (2017)
    - If you're already mathematically trained and just want a good, deep, technical intro to the FEP this is a great paper to start with. It lays almost all of the terminology and main constructs out in one place (notably, it doesn't introduce Markov Blankets or information geometry) and you'll be able to read almost every other paper in the FEP literature after reading this!
  - [Deep Active Inference](https://arxiv.org/abs/1709.02341) by Kai Ueltzhöffer (2017)
  - [A Free Energy Principle for a Particular Physics](https://arxiv.org/abs/1906.10184) by Karl Friston (2019)
    - This monograph lays out a sort of grand-unified vision of the FEP as seen from Karl Friston's point of view. It's one of the most encompassing of all the FEP papers and I implicitly designed this syllabus so that, if you knew most of the stuff in the prerequisites list, you'd be able to read and understand this
- **Reinforcement Learning and Active Inference**
  - [Reinforcement Learning or Active Inference?](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0006421) by Karl J. Friston, Jean Daunizeau, Stefan J. Kiebel (2009)
  - [Active Inference: Demystified and Compared](https://arxiv.org/abs/1909.10863) by Noor Sajid, Philip Ball, Karl J. Friston (2019)
  - [Reinforcement Learning Through Active Inference](https://arxiv.org/abs/2002.12636) by Alexander Tschantz, Beren Millidge, Anil K. Seth, Christopher L. Buckley (2020)
  - [Action and Perception as Divergence Minimisation](https://arxiv.org/abs/2009.01791) by Danijar Hafner, Pedro A. Ortega, Jimmy Ba, Thomas Parr, Karl Friston, Nicolas Heess (2020)
  - [Active Inference on Discrete State Spaces: A Synthesis](https://arxiv.org/abs/2001.07203) by Lancelot Da Costa, Thomas Parr, Noor Sajid, Sebastijan Veselic, Victorita Neacsu, Karl Friston (2020)
- **Physics/Theory**
  - [The Thermodynamics of Prediction](https://arxiv.org/abs/1203.3271) by Susanne Still, David A. Sivak, Anthony J. Bell, Gavin E. Crooks (2012)
  - [Towards A Neuronal Gauge Theory](https://journals.plos.org/plosbiology/article?id=10.1371/journal.pbio.1002400) by Biswa Sengupta, Arturo Tozzi, Gerald K. Cooray, Pamela K. Douglas, Karl J. Friston (2016)
  - [Approximate Bayesian inference as a gauge theory](https://arxiv.org/abs/1705.06614) by Biswa Sengupta, Karl Friston (2017)
  - [Markov Blankets, Information Geometry, and Stochastic Thermodynamics](https://royalsocietypublishing.org/doi/full/10.1098/rsta.2019.0159) by Thomas Parr, Lancelot Da Costa, and Karl Friston (2019)
  - [On the statistical mechanics of life: Schrödinger revisited](https://arxiv.org/abs/1908.08374) by Kate Jeffery, Robert Pollack, Carlo Rovelli (2019)
  - [Conservation Laws by Virtue of Scale Symmetries in Neural Systems](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1007865) by Erik D. Fagerholm, W. M. C. Foulkes, Yasir Gallero-Salas, Fritjof Helmchen, Karl J. Friston, Rosalyn J. Moran, Robert Leech (2020)
- **Computational Psychiatry**
  - [What Is Mood: A Computational Perspective](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6340107/) by James Clark, Stuart Watson, and Karl Friston (2018)
  - [Deeply Felt Affect](https://psyarxiv.com/62pfd/) by Casper Hesp, Ryan Smith, Thomas Parr, Micah Allen, Karl Friston, Maxwell Ramstead (2019)
- **Origins of Life/Self-Organisation**
  - [Answering Schrodinger's question: a free-energy formuation](https://www.sciencedirect.com/science/article/pii/S1571064517301409) by Maxwell Ramstead, Paul Badcock, Karl Friston (2018)
  - [The Markov Blankets of Life: Autonomy, Active Inference, and the Free Energy Principle](https://royalsocietypublishing.org/doi/10.1098/rsif.2017.0792) by Michael Kirchhoff, Thomas Parr, Ensor Palacios, Karl Friston and Julian Kiverstein (2018)
  - [On Markov Blankets and hierarchical self-organisation](https://www.sciencedirect.com/science/article/pii/S0022519319304588) by Ensor Palacios, Adeel Razi, Thomas Parr, Michael Kirchhoff, Karl Friston (2020)

## Open Problems

What are the current open problems in the FEP/Active Inference framework? What research directions are there? Suggestions encouraged!

## Conclusion

I hope this encourages more people to get stuck-in to the FEP/Active Inference research-space. It's so interdisciplinary that it welcomes people from all kinds of backgrounds, and there's important work that needs doing in math, neurobiology, philosophy, ecology, physics, software engineering, machine learning, and more! There are so many friendly people who are willing to think out loud, explain, answer questions, and offer support -seriously, just try tweet some of the people mentioned in this post!

Good luck with your studies!