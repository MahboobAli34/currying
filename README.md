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