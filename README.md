# DESCRIPTION

One of the classical problems in time series analysis consists in identifying a dynamical model from noisy data. Ignoring the noise in the inference procedure may lead biased estimates for the dynamics, and this becomes more and more problematic when the signal-to-noise ratio increases.

State-space models (SSMs) including a dynamical model and an observation model provide a natural framework to study time series with measurement noise  in  environment, economy, computer sciences, etc.  

In practice, the dynamical model is typically unknown or numerically intractable. A simple way is to consider a parametric model of the dynamic based on basic functions with relevant parameters. However, it is typically difficult to find an approriate model. 
We now propose an original non-parametric method to reconstruct the dynamics as well as estimate the model parameters given only a sequence of the observation process.

Our approach, named as npSEM, is the combination of a non-parametric estimate of the dynamic using local linear regression (LLR), a conditional particle smoother and a stochastic Expectation-Maximization (SEM) algorithm. Further details of its construction and implementation are introduced in the manuscript *An algorithm for non-parametric estimation in state-space models* of authors "T.T.T. Chau, P. Ailliot, V. Monbet".

This *npSEM* source code was built to export numerical results in the manuscript. To verify the efficiency of the npSEM algorithm, its performance is compared to the one of SEM algorithms where the true dynamic is given.

# CONTENTS


We organize the library into two *.ipynb files for executing experiments and performing results of the SEM and npSEM algorithms on two toy models. The first one "test_npSEM_sinus.ipynb" is  on a univariate sinus model, and the second "test_npSEM_L63.ipynb" performs the results on a 3-dimensional Lorenz model. The codes associated to the two testing files are contained in the files named "methods.zip" and "models.zip". 


# AUTHORS:
Thi Tuyet Trang Chau (trang.chau@lsce.ipsl.fr, tuyettrang218@gmail.com); 
Valerie Monbet (valerie.monbet@univ-rennes1.fr); 
Pierre Ailliot (pierre.ailliot@univ-brest.fr)
