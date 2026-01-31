# Python Functions: Medical Insurance Project
## Data Scientist: Analytics - Codecademy

You are curious about how certain factors such as age, sex, BMI, number of children, and smoking status contribute to medical insurance costs.

Note: while insurance companies do use BMI in their calculations, and that is reflected in this project, BMI is not necessarily an accurate predictor of health. As data scientists, we should always be skeptical of quantitative measures like BMI that reduce complex phenomena to a single number.

You will apply your new knowledge of Python functions to write a useful function that calculates medical insurance costs.

### Tasks

#### Creating a function

1. First, take a look at the code in **script.py**.

In this code, we estimate the medical insurance costs for two individuals, Maria and Omar, based on five variables:

* <code>age</code>: age of the individual in years
* <code>sex</code>: 0 for female, 1 for male
* <code>bmi</code>: individual’s body mass index
* <code>num_of_children</code>: number of children the individual has
* <code>smoker</code>: 0 for a non-smoker, 1 for a smoker

These variables are used in the following formula to estimate an individual’s insurance cost (in USD):

*insurance_cost* = 250 ∗ *age* − 128 ∗ *sex* + 370 ∗ *bmi* + 425 ∗ *num_of_children* + 24000 ∗ *smoker* − 12500
​

Click “Save” to see the estimated insurance costs for Maria and Omar.

2. The code used to estimate insurance costs for Maria and Omar looks quite similar – in both cases we calculate the insurance cost using the same formula and then print the output.

This code is a great candidate for a function because it involves repeating almost identical commands in multiple places.

Let’s start by defining a function called <code>calculate_insurance_cost()</code> on line 2. For now, your function should not have any parameters or output.

3. Let’s outline the behavior we want our function to have. Inside of <code>calculate_insurance_cost()</code>, do the following:

* Create a variable called <code>estimated_cost</code>. For now, set this variable equal to a value of <code>1000</code>. You’ll add the full formula in the next step.
* Add a print statement that prints <code>estimated_cost</code>. You should output a message similar to: <code>"The estimated insurance cost for this person is xxx dollars."</code>
* Return <code>estimated_cost</code>

#### Adding parameters to a function

4. Nice job – you’ve created a simple Python function that we’ll use to estimate medical insurance costs.
 
However, the function currently returns a value of 1000. We want it to return our insurance cost formula instead.

Modify the function definition so that it contains five parameters:

* <code>age</code>
* <code>sex</code>
* <code>bmi</code>
* <code>num_of_children</code>
* <code>smoker</code>

Take a look at the hint if you need a reminder on how to add parameters to a function definition.

5. Now that we have set up the function to take inputs for each of the values needed in the insurance formula, we can make use of them inside of our function.

In <code>calculate_insurance_cost()</code>, change the value of <code>estimated_cost</code> from <code>1000</code> to our formula for insurance cost.

Remember that the formula for insurance cost is:

```
250 * age - 128 * sex + 370 * bmi + 425 * num_of_children + 24000 * smoker - 12500
```

#### Calling a function

6. The function is now properly set up to calculate an individual’s medical insurance costs based on the five variables passed into it. Let’s test this out!

Go to the section of code that estimates Maria’s insurance cost.

Rename <code>insurance_cost</code> as <code>maria_insurance_cost</code> and set it equal to <code>calculate_insurance_cost()</code> with the appropriate values for Maria as arguments.

7. Now, remove the print statement for Maria since our function will take care of printing the estimated cost for us.

Additionally, remove the five lines of code defining the initial variables for Maria, as we are now passing in these values directly in the function call.

8. Repeat steps 6-7 for Omar:

* Rename <code>insurance_cost</code> as <code>omar_insurance_cost</code> and set it equal to the <code>calculate_insurance_cost()</code> function, passing in the appropriate values as arguments.
* Remove the initial variables and print statement for Omar.

Notice how much cleaner our code is now! By utilizing a Python function, we were able to condense many lines of code into just a few.

#### Adding new parameters

9. Click “Save” to see the estimated insurance costs for Maria and Omar as calculated by your function.

In the output terminal, notice that it says <code>"The estimated insurance cost for this person is..."</code> but it does not specify the actual name of the person.

To fix this, begin by adding an additional parameter called <code>name</code> to the function definition.

10. Next, modify the print statement in the function so that it includes the new <code>name</code> parameter, replacing <code>"this person"</code> with the actual name of the person.

11. We must also update our function calls, passing in the name variable as an argument.

Update the function call for <code>maria_insurance_cost</code>, passing in <code>name = "Maria"</code> as an argument.

Do the same for Omar, passing in <code>name = "Omar"</code>.

Now if you click “Save”, you’ll see that our function is able to write a more personalized message specifying the name of the individual it is estimating insurance costs for. Pretty neat, right?

#### Estimating your own insurance cost

12. In this example, we calculated the insurance costs for two individuals, but with our new code we can easily extend this to thousands or even millions of individuals.

To illustrate, estimate your own insurance cost.

At the bottom of your code, create a new insurance_cost variable for yourself, similar to how we did it for Maria and Omar.

Set the variable equal to a function call to <code>calculate_insurance_cost()</code>, passing in your own name, age, sex, bmi, number of children, and smoker status.

Click “Save” to see the result.

#### Extra

13. Congratulations! In this project, you created a useful function that calculates medical insurance costs based on the values passed into the function. Great job!

As a data scientist, you should always strive to make your code more clean and modular. Using functions to avoid repetitive code is a great way to do just that.

Now it’s your turn! If you’d like extra practice with Python functions, here are some suggestions to get you started:

* Modify the <code>calculate_insurance_cost()</code> function so that it returns two values – the output message and the estimated cost.
* Create a second function to calculate the difference between the insurance costs (given as inputs) of any two individuals and print a statement saying: <code>"The difference in insurance cost is xxx dollars."</code>

Happy coding!