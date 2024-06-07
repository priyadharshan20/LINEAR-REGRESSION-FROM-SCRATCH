# LINEAR-REGRESSION-FROM-SCRATCH

In this project I have implemented a simple linear regression model from scratch without using any libraries or frameworks to predict salaries based on years of experience using gradient descent optimization. It involves data preprocessing, visualization, cost calculation, and gradient descent for optimizing the linear regression parameters.

I have used the Experience-Salary.csv dataset in this model. The functions involved are

1. **predict(slope, y_intercept, experience)**

   - This function calculates the predicted salary based on the linear regression model given the slope, y-intercept, and experience.

   - The function uses the formula for a linear regression model:
   - **predicted_values = ( slope × experience ) + y_intercept**

   - It multiplies each value of experience by the slope, adds the y-intercept, and returns the predicted salary.


2. **cost_function(experience, salary, predicted_values)**

   - This function computes the cost function, which measures the error between the actual and predicted values.
   - The cost function is calculated using the mean squared error formula:

   - COST FUNCTION OR MSE = (1/2n) * Σ(y_i - y_hat_i)^2
   
   - Where:
    - 'n' represents the number of data points.
    - 'y_i' denotes the actual salary for the 'i-th' data point.
    - 'y_hat_i' denotes the predicted salary for the 'i-th' data point.

3. **gradient_descent(slope, y_intercept, experience, salary, learning_rate)**

    - This function performs gradient descent to optimize the linear regression parameters (slope and y-intercept).
    - Gradient descent is an optimization algorithm used to minimize the cost function.
    - It iteratively updates the parameters (slope and y-intercept) in the direction that reduces the cost function.
    - The function computes the gradients of the cost function with respect to the parameters and updates them using a learning rate.
    - It stops iterating when the cost function no longer decreases significantly or after a fixed number of iterations.
  
   **STEPS INVOLVED**

    - Predicted values are calculated using the formula:
     
      	- predicted_values = (slope * experience) + y_intercept
      
    - Calculate the derivatives of the cost function with respect to slope and y-intercept:
      
      	- For slope (𝑚):
      
      		- d(cost_function)/d(m) = - (1/n) * Σ(experience_i * (salary_i - predicted_values_i))
      
      	- For y-intercept (𝑏):
      
      		- d(cost_function)/d(b) = - (1/n) * Σ(salary_i - predicted_values_i)
      	   
    - Update slope and y-intercept:
      
      	- Update the slope (m):
      	  
      		- slope<sub> i+1</sub> = slope<sub> i</sub> - learning_rate *  d(cost_function)/d(m) 
      	
      	- Update the y_intercept (b):

          - intercept<sub> i+1</sub> = intercept<sub> i</sub> - learning_rate *  d(cost_function)/d(b) 


    - These formulas are used in the gradient_descent function to iteratively update the slope and y-intercept values to minimize the cost function, which measures the difference between the actual and predicted values.
