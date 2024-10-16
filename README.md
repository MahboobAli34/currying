# Statelessness of  LinkedIn
Statelessness is a fundamental aspect of RESTful architecture, indicating that every request made by the client to the server must encompass all necessary information for understanding and processing the request, without depending on any previously stored context on the server.
# In the Context of LinkedIn:
* HTTP Requests:
When users engage with LinkedIn their browser or mobile application transmits separate HTTP requests to LinkedIn’s servers. Each request operates independently and includes essential information, such as session tokens or cookies, to authenticate the user’s session.
* Session Management: 
LinkedIn employs cookies or tokens  to manage user sessions the server does not retain information from  requests. Each request must carry the authentication token within the header or cookies enabling the server to verify the identity of the requester.
# Authentication  LinkedIN
* username and Password: 
The most prevalent method involves entering an email or phone number along with a password. Upon submission, LinkedIn verifies these credentials against its database to confirm the user's identity.
# Authorization on LinkedIn
* Profile Access: 
Although any individual can view a public LinkedIn profile, specific sections, such as contact information or activity feeds, are limited and may necessitate a connection.
Posting: 
* Upon successful authentication, users are permitted to share content; however, authorization determines their ability to post public updates or engage with particular groups.
* API Access:  
For external applications utilizing LinkedIn's API, the OAuth procedure guarantees that the application can only access data for which the user has provided explicit consent.

# Currying
* defination of curring
 taking a function that accepts multiple arguments and breaking it down so that at each step, one argument is given. Every time you provide an argument, it returns a new function that waits for the next argument. When all the arguments are provided, you get the final result.
 # Currying code explanation
 1. function calculatePrice(discount) { 
 2.  return function(tax) {
 3.  return function(price) {                   
 4. const discountedPrice = price - price * discount;         
 5. const totalPrice = discountedPrice + discountedPrice * tax;   
 6. return totalPrice;              
 7. };  
 8.  };          
 9. }    
   
10. const discount10 = calculatePrice(0.1);                 
11. const discount10AndTax20 = discount10(0.2);                  
12. console.log(discount10AndTax20(100));                           

 * This outermost function takes discount as an argument and returns another function (inner function).  
 * This inner function takes tax as an argument. After you provide the tax, it returns yet another function that will take the price   
* This innermost function takes the price and performs the calculation for the total price.  It first calculates the discounted price, applies tax to the discounted price, and returns the final result: