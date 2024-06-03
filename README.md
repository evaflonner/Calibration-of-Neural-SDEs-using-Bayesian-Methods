Consider a Neural SDE model parameterised by neural networks $\theta$ consisting of equations
![grafik](https://github.com/evaflonner/Calibration-of-Neural-SDEs-using-Bayesian-Methods/assets/147062673/f9a88052-0d90-4a14-9a7a-6b7b1454a736)

In this work we propose a Bayesian method to calibrate this model. The key-advantage of this approach is, that robust bounds on the implied volatility are obtained in a natural way by 
utilising the posterior distribution on neural network weights.
This repository, which builds upon work done by [Patryk Gierjatowicz, Marc Sabate-Vidales and co-authors](https://github.com/msabvid/robust_nsde/blob/master/nsde_LSV.py), considers empirical S\&P 500 implied volatility data with 10 strikes and 4 maturities to determine the prices of the corresponding European call options.
The spot price of the underlying at time 0 is $S_0 = 590$, $\delta=4.5$, $\sigma_{prior}=4$, the interest rate is $r = 0.060$ and dividend rate $d = 0.026$. The prices are 

![grafik](https://github.com/evaflonner/Calibration-of-Neural-SDEs-using-Bayesian-Methods/assets/147062673/8ff12c8c-5fb9-4114-bd0c-606dee40247b)


The reason why we take this data set as an example is that even tough the data are from 1990s, they allow for a direct comparison with the results given in the [Gupta and Reisinger](https://people.maths.ox.ac.uk/reisinge/Publications/RobustnessPaper.pdf) paper, as we choose exactly the same data and hyperparameters. 
The plots 
![grafik](https://github.com/evaflonner/Calibration-of-Neural-SDEs-using-Bayesian-Methods/assets/147062673/c7c152fe-231d-49ec-aab7-08ddec250f87)

reveal that in contrast to the bounds on the implied volatility surface presented in Gupta and Reisinger, we obtain much tighter bounds given by the minimum and maximum implied volatility for each strike and maturity that are obtained after algorithmic convergence.
