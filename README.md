# ML_SupReg_TimeSeries_EnergyConsumption
Use Time Series forcast to predict Energy consumption

XGBoost based on GBoost and Regularization
GBoost based on AdaBoost
AdaBoost based on DecisionTree and RandomForest (RF)


## AdaBoost
1. Trees are made of stump (1 root node and 2 leaves , 1 feature is used /Tree) --> weak learner

2. unlike RF where all Trees are equally weighted , in Ada Trees have weight

3. unlike RF where Trees are created independetly , in Ada errors of 1st Tree is propagated to 2nd Tree


## GradientBoost
1. 1st Tree (1leave) predict = init_predict 
    "init_predict = base_score default = 0.5"
2. 2nd Tree predict = 1st predict + learning_rate *(residual from 1st predict)  
    "learning_rate default = 0.03 - 0.3"
n. nth Tree predict = ....
    "n_estimator default = 1000"


## XGradientBoost
1. lambda (Regularization parameter ): reduce the prediction sesnitivity for individual observation (prevent overfiting)
    "lambda default = 1"

2. max_depth default 3-6
3. gamma : gain value used to prunn the tree
    branch gain > gamma --> keep it
    branch gain < gamma --> prunn it
    hint : even gamma =0 won't totally prevent prunning