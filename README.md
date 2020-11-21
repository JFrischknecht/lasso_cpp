# lasso_cpp
A minimal working implementation of the LASSO estimator for linear models with C++

## About



## How to use the program 

This program requires two inputs. First it requires a CSV-file containing the continuous/binary outcome variable. Second it requires a CSV-file containing the continuous/binary predictor(s). The first row of each file (where column-names are usually placed) is not read. Both files must consist of only numeric columns without missing values. The user is responsible to clean and prepare the data first (e.g. deal with any missing values, one-hot-encode categorical predictors, etc.). Note that an intercept should not be included in the set of predictors.

By default the name of the first file is assumed to be *outcome.csv* and the name of the second file is assumed to be *predictors.csv*.

To run the program:
1. Download *lasso.exe* and save it together with *outcome.csv* and *predictors.csv* in a folder.
2. Start up a command-line (e.g. *cmd* on Windows) in this folder and execute *lasso.exe* in the command line. E.g.
```shell
D:\lasso_cpp-main>lasso.exe
```

You can deviate from the default file names by supplying two optional command-line arguments. In this case you always need to supply the name of both files. E.g.
```shell
D:\lasso_cpp-main>lasso.exe outcome_large.csv predictors_large.csv
```

The program will produce two files: *lasso_fitted.csv* and *lasso_coefficients.csv* in the folder where the program was executed.
The first file contains the fitted values of the optimal model and the second contains the estimated coefficients of the optimal model, with the intercept being the first coefficient.

## References

Friedman, J., Hastie, T., & Tibshirani, R. (2010). Regularization Paths for Generalized Linear Models via Coordinate Descent. Journal of Statistical Software, 33(1), 1 - 22. http://dx.doi.org/10.18637/jss.v033.i01

Hastie, T., Tibshirani, R., & Wainwright, M. (2015). Statistical Learning with Sparsity: The Lasso and Generalizations. Chapman & Hall/CRC.
