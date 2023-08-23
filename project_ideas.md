
 
# M.Phil Part 3 project ideas 

Soumya Banerjee 

Senior Research Fellow

University of Cambridge, Cambridge, United Kingdom 

∗ E-mail: sb2333@cam.ac.uk neel.soumya@gmail.com

Office: FC01 (first floor) in the computer science department


I work in explainable AI (xAI) and unconventional approaches to AI. I work at the intersection of complex systems and xAI: I take inspiration from complex systems to suggest new approaches to AI, and use AI to analyze complex systems.


## Projects 

### Project idea 1 (Explainable AI)

* Contemporary approaches towards explainable AI are model-centric. We will use data-centric approaches to explain the complex interplay between data and models. This will build on and extend published work [1]. This project will be ideal for a student with interest in machine learning and who has coding experience. 
 
 There are many ways in which the work presented in [1] can be extended (either new methods or new application areas). Please get in touch to discuss. 
 
 
### Project idea 1B: explainable AI applied to biology/computational biology

 Another project idea is to apply explainable AI approaches to genomic data. This will be a machine learning, computational biology and bioinformatics project.
 
 The student will develop explainable AI approaches for interpreting clusters in single-cell gene expression data or other biological data. There is an opportunity to also look at other computational biology projects. No background is biology is necessary.

  This work is part of the Accelerate Programme for Scientific Discovery which aims to democratize access to AI tools and apply AI to problems from diverse disciplines. The student will be part of a growing community of inter-disciplinary AI researchers at the University of Cambridge. 


<!---### Project idea 1C: explainable AI applied to biology/computational biology

Cells express receptors on their surface. These receptors are expressed based on genes.
These receptors bind to rceptors on other cells.

This project will use publicly available genomic data to predict what receptors will be expressed on the surface of a cell.
-->



### Project idea 2

* For high stakes decisions we need simple and explainable/interpretable models. This need is acute in the case of healthcare and social sciences like recidivism prediction [2]. In this project, we will build simple interpretable models that are surrogates for deep learning models. 

  The student will look at publicly available data and synthetic data to generate surrogate models that are transparent and interpretable. The process of creating these surrogate interpretable models will be automated. This can also be partially based on published work [1]. 

 The surrogate models can be decision trees (like CART) trained on the input and output of a deep learning model [1].   This can use R packages like party, rpart, partykit or other packages. 
 This will lead to tools that automated the creation of surrogate interpretable models based on deep learning models in healthcare. 

  This project will be ideal for a student with interest in machine learning and who has coding experience.
  

   This work is part of the Accelerate Programme for Scientific Discovery which aims to democratize access to AI tools  and apply AI to problems from diverse disciplines. The student will be part of a growing community of inter-disciplinary AI researchers. 


### Project idea 3: Personalized explainable AI

Tailor machine learning model explanations based on audience (e.g. patients, clinicians, farmers, etc.). Generate natural language explanations from machine learning model and tailor these natural language expplnanations based on unique background of listener.

<!--(joint supervision with Peter Ochieng). 
-->

### Project 4: Tradeoffs between explainabilty and privacy

Develop explainable machine learning models that explain themselves but do so without leaking personal data. For example, class-contrastive reasoning techniques [1] can be used to generate explanations. But they can inadvertently leak personal data. This project will explore the tradeoff between explainability and privacy (and potentially bias). This will lead to models that balance explainability, privacy and bias.


### Project idea 4B: Explainable privacy preserving machine learning

Develop explainable machine learning models that are also privacy preserving. 

Model explanations will be extracted from machine learning models. However this can lead to leakage of private data. Hence one approach is to add noise to model weights (using differential privacy techniques). This will lead to explainable models that are also privacy preserving.

This can also be done in a federated fashion that will help preserve privacy. 

This project is a collaboration with Dr. Abhirup Ghosh.

<!---### Project idea 5: Explainable AI models applied to time series data

This project will involve developing explainable AI models for time series data. The time series data will come from ECG data and data from activity sensors.

This project is a collaboration with Dr. Abhirup Ghosh.
-->


### Project idea 5: Generative AI applied to complex systems


This project will involve modelling complex systems (like an epidemic spread) with generative agents. For example, generative agents can be coupled to agent based models. This can be used to simulate epidemics.

https://arxiv.org/abs/2307.04986

https://github.com/bear96/GABM-Epidemic

We will further develop this this framework and apply it to other complex systems (like supply chains, modelling of disinformation, people who are against taking vaccines, conflicts in societies, etc.) 


 
 ### Project idea 6
 
 * Build a computational model of analogy making and apply it to biomedical and genomic data.
 
 For other project ideas related to explainable AI see the following page:
 
 https://github.com/neelsoumya/special_topics_unconventional_AI/
 
 Broadly this will use concepts like analogies and stories to create new explainable AI methods.
 
 See for example 
 
 https://github.com/Tijl/ANASIME
 
 https://github.com/crazydonkey200/SMEPy

 https://github.com/fargonauts/copycat
 
 
 ### Project idea 7
 
 Build a machine learning algorithm or domain specific language to solve the Abstraction and Reasoning Corpus Challenge
 
   https://github.com/fchollet/ARC

 Abstraction and Reasoning Corpus Challenge

   https://blog.jovian.ai/finishing-2nd-in-kaggles-abstraction-and-reasoning-challenge-24e59c07b50a

   https://github.com/alejandrodemiquel/ARC_Kaggle

 Domain specific languages may be required (as suggested by Chollet) like genetic algorithms and cellular automata.
 
 <!--
 This will also involve extensions of the DreamCoder paper.
 
 DreamCoder: Growing generalizable, interpretable knowledge with wake-sleep Bayesian program learning
 
   https://arxiv.org/abs/2006.08381
 --> 


 <!--Please note this is a very challenging project.-->
 
 

### Project idea 8 (Automated Scientific Discovery)
  
This is a project on automatically discovering scientific laws (like Kepler's Law) and invariants (like Boyle's Law) from data.  

This may involve building a model or Bayesian model and/or probabilistic programming model of infection dynamics (like a SIR model) or an intra-cellular regulatory network [5]. This would apply a probabilistic programming model to infection data from different sources.  

Other models include phsyics simulators like pymunk:

http://www.pymunk.org/en/latest/examples.html#planet-py

You would simulate physics based simulations (like pymunk) or other models (like the SIR model above) and develop a machine learning approach to automatically generate insights from this model.

This would be an explainable AI model for a complex model of a physical system.

The project would involve building a model that would generate insights from these complex systems (an artificial model of human creativity).



### Project idea 8B
  
This is a project on automatically discovering scientific laws (like Kepler's Law) and invariants (like Boyle's Law) from data.  This will enable us to automatically discover conservation laws from data.

One can build a model or Bayesian model and/or probabilistic programming model of a complex systems model like infection dynamics (SIR model) or an intra-cellular regulatory network [5]. 

This would involve building a qualitative process model for a physical system.   

This would be an explainable AI model for a complex model of a physical system.

The project would involve building a model that would generate insights from these complex systems (an artificial model of human creativity).


### Project idea 8C

This is a project on automatically discovering scientific laws or mathematical equations from data.    

This would involve extending the Ramanujan machine by applying it to other data or other dynamical systems or using another machine learning approach.

https://github.com/RamanujanMachine/RamanujanMachine

Other ideas including extending AI Feynman 2.0 

https://github.com/SJ001/AI-Feynman

or BACON.3

https://github.com/jantzen/BACON

One can also apply symbolic regression approaches like PySR (python) or gramEvol (R).

<!-- one can also apply Bayesian symbolic regression. This can be applied to discover trigonometric identities. This would be a joint project with Challenger Mishra -->

<!-- data can be used from the AI feynman database on Max tegmark's website -->

Other approaches include Bayesian symbolic regression 

https://arxiv.org/abs/1910.08892

https://github.com/ying531/MCMC-SymReg


or seq2seq approaches to symbolic regression

https://openreview.net/pdf?id=W7jCKuyPn1

https://github.com/SymposiumOrganization/NeuralSymbolicRegressionThatScales

This would be an artificial model of human creativity.

Other ideas include discovering ordinary differential equations from data

https://arxiv.org/abs/2211.02830#


### Project idea 9 (Collective intelligence in AI)

Dynamics of collective learning in artificial neural networks, Hopfield networks, self organizing maps and neural gas.
 
 
### Project idea 9B
 
The role of noise in collective artifical intelligence in building behaviour (altruism, co-operation, competition) and structures (structures to capture prey). This will use the multi-agent platform MAgent

https://github.com/geek-ai/MAgent

We can also use the EvoJax framework

https://github.com/google/evojax/blob/main/examples/notebooks/EncirclingAgents.ipynb

We can also extend MAgent using dream mechanisms in World Models

https://worldmodels.github.io/

https://smartlabai.medium.com/world-models-a-reinforcement-learning-story-cdcc86093c5


### Project idea 9C (Modelling complex systems with generative agents)

This project will involve modelling complex systems (like an epidemic spread) with generative agents. For example, generative agents can be coupled to agent based models. This can be used to simulate epidemics.

https://arxiv.org/abs/2307.04986

https://github.com/bear96/GABM-Epidemic

This can also be combined with neural automata (see projects below)


### Project idea 10 (Explainable neural cellular automata)

Extending the neural cellular automata

https://distill.pub/2020/growing-ca/#experiment-2

and make it more interpretable and explainable.

For example, you can apply it to data from the Game of Life and infer the rules.

https://github.com/lantunes/netomaton/blob/master/demos/game_of_life/README.md

https://github.com/tomgrek/gameoflife

We can also apply it to biological data from cell biology.
<!-- morphology or wave propagation in the Rho GTPase system -->
<!--This would be similar to wave propagation in B-Z systems. We can also apply it to data from the B-Z system. -->

<!-- we can also apply it to data from computational fluid dynamics -->

Another idea is to apply this to simulations from computational fluid dynamics using the software below:

https://github.com/md861/HypFEM

This would be jointly with Mayank Drolia.


### Project idea 10B (Neural cellular automata for control of complex systems)


Use neural cellular automate for self-organized control of complex systems

https://arxiv.org/abs/2106.15240

We can use this framework to, for example, model and control epidemics. 

Also see projects above on generative agents.

https://arxiv.org/abs/2307.04986

https://github.com/bear96/GABM-Epidemic



### Project idea 11: Biologically inspired machine learning applied to cyber security

This project will involve developing biologically inspired machine learning techniques, like negative selection algorithms [7]. Negative selection algorithms are inspired by how the immune system is trained to detect pathogens. This project will involve developing a biologically inspired machine learning algorithm and applying it to cyber security. An example application would be detecting outliers in network traffic.


### Project idea 12: AI applied to cyber security

This project will develop AI tools applied to cyber security. 

Ideas include developing and improving on AI based methods for password guessing. See PassGAN: A Deep Learning Approach for Password Guessing

https://arxiv.org/pdf/1709.00440.pdf

<!-- talk on AI applied to cyber security

https://www.youtube.com/watch?v=oBdB61A8Yt8

-->

Other ideas include extending AI based approaches to generate better phishing URLs. For example, DeepPhish: Simulating Malicious AI

https://albahnsen.files.wordpress.com/2018/05/deepphish-simulating-malicious-ai_submitted.pdf

Other ideas include designing better outlier detection algorithms in network traffic data. For example, one can use ideas from rough sets to design better outlier detection strategies:

Outlier Detection Using Rough Sets

https://link.springer.com/chapter/10.1007/978-3-030-05127-3_7

We can also use autoencoders for detecting outliers in network traffic data.

Other ideas include using deep autoencoders for detecting malicious source code

https://doi.org/10.1016/j.patter.2023.100773


### Project idea 13

* Other project ideas are generating synthetic data from private datasets like data from electronic healthcare records data [3], other explanatory artificial intelligence (xAI) techniques, privacy preserving machine learning [4], documenting data and models, detecting concept drift [6], etc. 



### Other ideas

 Project ideas can be developed according to student interests. If you have other project ideas you would like to discuss, please come speak with me.
 
 
## Supervision 
 
 Students will be jointly supervised with Prof. Neil Lawrence and Prof. Pietro Lio.

## Contact

Project ideas can be developed according to student interests. 

Please contact Soumya Banerjee at sb2333@cam.ac.uk or neel.soumya@gmail.com to have an informal chat. Please also send a copy of your CV.

Office: FC01 (first floor) in the computer science department

You can learn more about my work here: 

https://sites.google.com/site/neelsoumya 

## Bigger Picture

The main objective is to develop a suite of techniques inspired by classical AI to inform explainable AI.
This project is part of a wider effort of unconventional approaches to AI. 

## References 

1. Banerjee S, Lio P, Jones PB, Cardinal RN (2021) A class-contrastive human-interpretable machine learning approach to predict mortality in severe mental illness. npj Schizophr 7: 1–13. 

2. Rudin C (2019) Stop explaining black box machine learning models for high stakes decisions and use interpretable models instead. Nat Mach Intell 1: 206–215. 

3. Banerjee S, tom rp Bishop (2022) dsSynthetic: Synthetic data generation for the DataSHIELD federated analysis system. BMC Res Notes 15: 230. 

4. Banerjee S, Sofack GN, Papakonstantinou T, Avraam D, Burton P, et al. (2022) dsSurvival: Privacy preserving survival models for federated individual patient meta-analysis in DataSHIELD. BMC Res Notes 15: 197.

5. Modelling the effects of phylogeny and body size on within-host pathogen replication and immune response, Soumya Banerjee, Alan Perelson, Melanie Moses, Journal of the Royal Society Interface 14(136), 20170479, 2017

6. https://web.archive.org/web/20230606205118/https://www.nannyml.com/blog/when-data-drift-does-not-affect-performance-machine-learning-models, URL accessed June 2023

7. Influence of correlated antigen presentation on T cell negative selection in the thymus, Soumya Banerjee, SJ Chapman, Journal of the Royal Society Interface, 15(148), 20180311, 2018



