# npEM
# DESCRIPTION

One of the classical problems in time series analysis consists in identifying a dynamical model from noisy data. Ignoring the noise in the inference procedure may lead biased estimates for the dynamics, and this becomes more and more problematic when the signal-to-noise ratio increases.
State-space models (SSMs) provide a natural framework to study time series with measurement noise  in  environment, economy, computer sciences, etc. A SSM is generally defined by a system of two models: a dynamical model which describes the evolution of the latent state and an observation model which represents the transformation between the state and the measurements.

In practice, the dynamical model is typically unknown or numerically intractable. A simple way is to consider an alternative parametric model based on basic functions with relevant parameters. However, it is typically difficult to find an approriate model. 
We now propose an original non-parametric method to reconstruct the dynamics as well as estimate the model parameters given only a sequence of the observation process.
This novel method is the combination of a non-parametric estimate of the dynamical model using local linear regression (LLR), a conditional particle smoother and an Expectation-Maximization (EM)-like algorithm. Further details of its construction and implementation are introduced in the article **An efficient particle-based method for maximum likelihood parameter estimates in nonlinear state-space models** of authors "T.T.T. Chau, P. Ailliot, V. Monbet".

This **npEM** source code was built to export numerical results in the paper. To verify the efficiency of the npEM algorithm, its performance is compared to the one of EM-like algorithms where the true model is given.

# STRUCTURE

We organize the library into two main testing files. The first one "*test_npEM_sinus.ipynb*" is to execute experiments on an univariate sinus model and the second "*test_npEM_L63.ipynb*" is to provide the results on a 3-dimensional Lorenz model. Supplementary codes are contained in the files named "*methods*", "*additives*" and "*models*". 


# CONTACT:
Thi Tuyet Trang Chau (thi-tuyet-trang.chau@univ-rennes1.fr)
