### Extensions

By using an **extension**, you can continue writing the definition of a struct, class or enum anywhere in your codebase.

![Alt text](../Images/Properties_And_Access_Control/extension1.png "extension Example 1")

### Note:
* Code that is written in an extension will behave exactly the same as if it was defined in the original struct.
* You can exten structs, classes, and enums.

![Alt text](../Images/Properties_And_Access_Control/extension2.png "extension Example 2")

WHAT YOU CAN'T DO:
* In extension you cannot create stored properties:

![Alt text](../Images/Properties_And_Access_Control/extension3.png "extension Example 3")

* This restriction ensures that adding an extension to your code will never cause your code to not compile by adding new requirments.

  * Instead add computed properties:
  ![Alt text](../Images/Properties_And_Access_Control/extension4.png "extension Example ")