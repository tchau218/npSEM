# DESCRIPTION

One of the classical problems in time series analysis consists in identifying a dynamical model from noisy data. Ignoring the noise in the inference procedure may lead biased estimates for the dynamics, and this becomes more and more problematic when the signal-to-noise ratio increases.

State-space models (SSMs)} provide a natural framework to study time series with measurement noise  in  environment, economy, computer sciences, etc.  They are generally defined as follows
\begin{align} 
X_{t} = m \left(X_{t-1} \right) + \eta_{t},  \quad  \eta_{t} \sim \mathcal N (0,Q_t) \\
Y_t = H(X_t)  + \epsilon_t, \quad \epsilon_t \sim \mathcal N (0,R_t).
\end{align} 
where $(X_t, Y_t) \in (\mathcal{X},\mathcal{Y}),  \forall t = 1:T$. The models $(m,H)$ with respect to independent white noises $ (\eta_t, \epsilon_t)_{t=1:T}$, describe the evolution of the latent state $(X_t)$ and the transformation between the state $(X_t)$ and the measurements $(Y_t)$. 

In practice, the dynamical model $m$ is typically unknown or numerically intractable. A simple way is to consider a parametric model of $m$ based on basic functions with relevant parameters. However, it is typically difficult to find an approriate model. 
We now propose an original non-parametric method to reconstruct the dynamics as well as estimate the model parameters given only a sequence $y_{1:T} = (y_1,y_2,\cdots,y_T)$ of the observation process $(Y_t)_t$.

Our approach, named as npSEM, is the combination of a non-parametric estimate of $m$ using local linear regression (LLR), a conditional particle smoother and a stochastic Expectation-Maximization (SEM) algorithm. Further details of its construction and implementation are introduced in the manuscript *An algorithm for non-parametric estimation in state-space models* of authors "T.T.T. Chau, P. Ailliot, V. Monbet".

This *npSEM* source code was built to export numerical results in the manuscript. To verify the efficiency of the npSEM algorithm, its performance is compared to the one of SEM algorithms where the true model $m$ is given.

# CONTENTS


We organize the library into two *.ipynb files for executing experiments and performing results of the SEM and npSEM algorithms on two toy models. The first one "test_npSEM_sinus.ipynb" is  on a univariate sinus model, and the second "test_npSEM_L63.ipynb" performs the results on a 3-dimensional Lorenz model. The codes associated to the two testing files are contained in the files named "methods.zip" and "models.zip". 


# AUTHORS:
Thi Tuyet Trang Chau (trang.chau@lsce.ipsl.fr,tuyettrang218@gmail.com)
Valerie Monbet (valerie.monbet@univ-rennes1.fr)
Pierre Ailliot (pierre.ailliot@univ-brest.fr)
