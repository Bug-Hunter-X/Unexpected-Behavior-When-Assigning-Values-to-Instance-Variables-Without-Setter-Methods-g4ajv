# Ruby Instance Variable Assignment Bug

This repository demonstrates a common, yet subtle, bug in Ruby related to assigning values to instance variables when you are using getter methods, and forget to create a setter.

## Problem

The `bug.rb` file shows that modifying the instance variable directly using `@value = 20` does not change the value returned by the `value` getter method. This is because the getter creates an isolated local variable named value, which can be confusing.  

## Solution

The `bugSolution.rb` file demonstrates a corrected version. Now the setter is explicitly defined, allowing direct modification of the instance variable via `my_object.value = 20`. This resolves the unexpected behavior.

## How to Reproduce

1. Clone the repository.
2. Run the file bug.rb.
3. Observe that modifying instance variable directly does not update the accessor method's value.
4. Run the file bugSolution.rb.
5. Observe that the instance variable value is updated correctly. 