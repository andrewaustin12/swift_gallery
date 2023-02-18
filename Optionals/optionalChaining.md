##### OPTIONALS
# Optional Chaining

It’s common in Swift to chain properties and method calls on a variable:

![Optional Chaining Example 1](../Images/Optionals/chaining1.png "Optional Chaining Example 1")

But what if the variable is an optional? We can use the *!* operator to force unwrap the optional:

![Optional Chaining Example 2](../Images/Optionals/chaining2.png "Optional Chaining Example 2")

But this will crash if the optional is nil:

![Optional Chaining Example 3](../Images/Optionals/chaining3.png "Optional Chaining Example 3")

Fortunately Swift gives us a way to safely chain different calls on an optional using *optional chaining*. By replacing the ***!*** operator with the ***?*** operator, our code can no longer crash. If the optional is ***nil***, then the entire expression will evaluate to ***nil***.

![Optional Chaining Example 4](../Images/Optionals/chaining4.png "Optional Chaining Example 4")

If the optional is not ***nil***, then it will be unwrapped and have the subsequent properties and methods called on it. Note that because the entire expression can be nil, it now evaluates to an optional as well:

![Optional Chaining Example 5](../Images/Optionals/chaining5.png "Optional Chaining Example 5")