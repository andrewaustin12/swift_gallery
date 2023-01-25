# Overriding Methods

To override a method, you can redeclare it in the subclass and add the override keyword to let the compiler know that you aren’t accidentally creating a method with the same name as the one in the parent class.

![Alt text](../Images/Classes/overriding.png "overriding Example 1")

Working Example:

![Alt text](../Images/Classes/overriding2.png "overriding Example 2")

Suppose you want a new ***SavingsAccount*** class and you want to override the ***.withdraw()*** method from its superclass BankAccount:

![Alt text](../Images/Classes/overriding3.png "overriding Example 3")

Here, the new .withdraw() method not only subtracts amount from balance, but it also increments numWithdraw.