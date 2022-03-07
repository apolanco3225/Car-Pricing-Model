# Quesitons

1. Data Analysis Questions

Take each of the following 3 variables:

    • odometer 
    • condition 
    • vin
    
For each of them analyze the following points:

    1. Evaluate the completeness of the variable and highlight any findings you think relevant for a discussion.
    2. Evaluate how well the value discriminates your dependent variable and determine if you would use it in your model.
    3. If the previous answer was affirmative then how would you propose to include it in your model. That is, what transformations, techniques, or tools would you use to include it.

# ***Answers***

- Odometer
    - odometer: Device that measures how many miles the car has been driven. (Int, Numerical Feature). Critical piece of information for the model, 18% of values were missing.
- Condition
    - condition: Evaluation of the current state of the car (String, Categorical feature) (New, Like new, Excellent, Good,Fair, Salvage) Also, very critical information for the model, 43% of values were missing. 
- VIN
    - vin: Vehicle identification number, car's id. (String, Categorical Feature) Not very useful for model prediction because of the cardinality of the variable, it could be used in a different part of the system to validate correctness of  information using an additional source of information from the government.
    
2. Model Building Questions
- ***What model would you propose to solve the problem and why did you choose it?***
Start with a simple baseline model like Linear Regression, this  would make easy to interpret the predictions it makes in a very intuitive since you can easily check the weight on every hiper parameter for every feature, therefore build trust in non-technical people. After that, iterate on more complicated models keeping track on a metric of interest, possible suggestions are:
- Random Forest Regressors
- Support Vector Regression
- Feed Forward Neural Network (You need big data here)

- ***What performance metrics would you use and discuss whether they are valid and their results***
I decided to remove mean squared error since it outputs the squared of the error, it is great for spotting outliers but could be a little bit discouraging to for a stakeholder to see an error of 25,000 dollars. Both, root mean squared error and mea absolte error change linearly, therefore more intuitive. The output is showed in dollars and not squared dollars.
- Root Mean Squared Error
- Mean Absolute error

- ***Discuss how would you monitor your model in 3 months time to determine its validity.***
Deploy model to a small population, let's say in a state, where the data science team can closely follow the behavior and analize the performance of the model. Having tackle all the challenges in that small experiment, you can proceed to scale to a bigger population until you can cover all the demand.
