Test_Automation_Using_AI_Copilots
Overview
This repository demonstrates two approaches for developing automation scripts using Cucumber, Page Object Model (POM) with Page Factory, and Maven:

Part 1: Manual Development
Part 2: AI Copilot-Assisted Development

Both approaches automate the same scenario:
Login with valid credentials and extend to a complete purchase flow using Selenium and TestNG.

Framework Structure
src/test/java
├── Pages          # Page Object classes
├── stepdef        # Step Definitions
├── Runner         # TestNG Cucumber Runner
└── Utilities      # Base class for browser setup, screenshots
src/test/resources
└── Features       # Cucumber Feature files


Components
Pages


home_page.java

getDisplayedUsername() → Returns welcome message text.
Methods to click first, second, third, and fourth product.



product_page.java

getProductTitle() → Returns product name.
clickAddToCart(), clickHomeButton(), clickCartButton().



cart_page.java

getCartPageTitle(), getProductName(), getProductPrice().
deleteFourthProduct(), isProductPresent(), getTotalPrice(), clickPlaceOrder().



placeorder_page.java

getPlaceOrderTitle(), getConfirmationPopupText().
Methods to enter Name, Country, City, Credit Card, Month, Year.
clickPurchase(), clickConfirmationOk(), read confirmation details.




Utilities

base.java

Launch Chrome & Edge browsers using if-else logic.
Screenshot method.
Alert handling method (handleAlertIfPresent()).
Explicit wait methods.




Step Definitions


home_steps.java

Verify welcome message with assertion.
Click first, second, third, and fourth product.



product_steps.java

Add product to cart, accept alert, click home/cart, verify 4th product name.



cart_steps.java

Verify cart page title, product details, total price, delete 4th product, verify deletion, click place order.



placeorder_steps.java

Verify modal title, enter details, click purchase, verify confirmation popup, verify alert text.




Feature Files

Must use Given, When, Then steps.
Every Then step → Assertion in StepDef.
Example:
Then the user should see the welcome message "Welcome <username>"




Assignment Deliverables

ZIP of Manual Development Project
ZIP of AI Copilot Development Project
Screenshots of timestamps:

Start and end time for manual development.
Start and end time for AI Copilot development.


AI Prompts Used

Example:

“Write a Cucumber feature file for login with valid credentials using Given-When-Then steps.”
“Generate step definitions for login scenario using Selenium and TestNG assertions.”




Assignment Description


Time Taken

Manual Development:
1 hour 2 minutes (5:04 PM – 6:06 PM)
AI Copilot Development:
15 minutes (6:15 PM – 6:30 PM)

