# The MVVM Architecture

For building SwiftUI apps, the most popular one is MVVM or the Model-View-ViewModel architecture.

## MVVM Components
There are three critical pieces to this structure: the Model (data), the View (UI), and the View-Model (interface). Each is responsible for a different function in our program.

### Model
The *Model* is the core data and logic of our software. This is where we define how our data is structured, manipulated, and stored.

### View
The View is the user interface of the application; this is what you will see on your screen. It handles the presentation of data and user input such as tapping on a button.

### ViewModel
The ViewModel is our in-between structure. It is designed to expose only the data points and hold the presentation logic that a specific View needs. The ViewModel exposes information from the Model to the View and then updates the Model in response to user interaction. The beauty of the ViewModel is that the Models and Views never interact with each other directly. This allows us to not have to build a different Model based on what the View needs and vice-versa. The Model doesn’t care about the View, and the View isn’t aware of the Model. Most times, the View will not need all the data that is stored in a Model, so the ViewModel only gives the UI access to information that it needs to present to the user. The ViewModel can pull data from one Model, or in our case, combine two or more Models under the same ViewModel.

### MVVM as a Whole
**The job of the ViewModel is to monitor data in both the Views and Models, then reload the Views when something changes. This ensures that the user has the most recent information.** 

To bring things altogether, it can be helpful to view the MVVM architecture as a typical restaurant experience. You, the user of the application, sit down at a table of the restaurant. The menu sitting there on the table represents the View. It displays the information that the user needs to interact with the restaurant. We can view the kitchen as the model. It contains all the recipes, ingredients, personnel, and equipment needed to create a meal. The user and the menu do not really need to know how the meals are prepared, how onions get chopped, or what temperature a potato gets baked at. All they need to see are the complete meals. Our waiter will act as the ViewModel, getting information from the kitchen and updating the menu as needed, as well as taking the user’s orders to the kitchen. If the user selects the special off the menu, a 14oz Ribeye with Asparagus and Garlic Mashed Potatoes, the waiter takes that information, as well as special parameters such as how well to cook the steak, back to the kitchen. The waiter then returns with the steak when it is complete and presents it to the user. This system keeps all of the data and views organized and operational.

Let’s remove this MVVM-style architecture from the restaurant. Imagine if we tried to talk directly to the kitchen ourselves. Think of the chaos that would bring! We don’t know our way around the restaurant, we don’t know who needs what information, and we don’t know how to give the kitchen staff our order.

While this restaurant still might be functional, it would be pretty disorganized. Think about coding a project the same way. If you have views and models scattered around your project chaotically, it would be very easy for errors and bugs to pop up. Building applications with a preplanned and well-executed structure helps eliminate these issues. It also demonstrates to other programmers and potential employers that you understand how to structure your logic, data, and presentations in a usable manner.

### Overview
MVVM architecture separates an application into three different areas:
  * ***Views*** that display information and handle user interaction.
  * ***Models*** that define how our data is structured and manipulated.
  * ***ViewModels*** that update Models as the user interacts with Views and update Views when the Model changes.