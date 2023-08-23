# PaymentMethod Demonstration

## Applying Strategy Pattern in a Java Project
Project developed to practice the application of the Strategy Pattern in Java as proposed by the refactoring.guru website. 

### Description
This demo project is a simple example of a payment system that demonstrates the use of the Strategy design pattern in Java. 
The main goal is to illustrate how different payment strategies can be easily switched, depending on the user needs.

### Main Features
* Supports two different payment strategies: PayPal and CreditCard.
* Allows the user to choose between these strategies during the checkout process.
* Collects payment details (credit card information or Paypal credentials).
* Performs a simulated payment, displaying a confirmation message upon completion.

### Project Structure
The project is composed by three main classes:
1. `PayStrategy`:
   * An interface that defines the contract for all payment strategies.
   * Includes methods for payment and to collect payment details.
2. `PayByPayPal`:
   * An implementation of the `PayStrategy`interface that enables payment using a PayPal account.
   * Requests the user's email and password for authentication.
   * Simulates a successful payment if the user is authenticated.
3. `PayByCreditCard`:
   * Another implementation of the `PayStrategy`interface that allows payment with a credit card.
   * Receives the credit card number, its expiration date and cvv code.
   * Simulates a successful payment and updates the credit card balance.
  
The project also has some additional auxiliary classes:
1. `CreditCard`:
   * Represents a credit card with an initial balance.
   * Maintains information such as the card number, expiration date and cvv code.
2. `Order`:
   * Represents a order with zero initial cost.
   * Maintains information about its total cost and status (open or closed).
3. `Demo`:
   * This is the main demo class that allows the user to select some products, the payment method 
and process the order.

### How to use
To execute the demo, follow these steps:
1. Run the Demo main method;
2. Select the products and their count;
3. Select Y or N to continue selecting products;
4. Choose the payment method (PayPal or Credit Card):
   * If you choose the PayPal method, type the user's email and password;
   * If you select the Credit Card option, type the card number and its expiration date and cvv code;
5. Select P or C to pay or continue shopping;
6. The payment will be processed and a message will be displayed indicating if the payment was successful.

### Disclaimer
This demo project aims to illustrate use of the Strategy Design Pattern to implement flexible payment strategies.
It's an simplified example and can be extended and improved for more complex scenarios.



