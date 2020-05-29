# AccompanyMe
The application is designed for the university students where their user credentials are verified using the student database system (For the purposes of this application, a simulation of a university student database system is considered since we do not have access to the actual student database).The user information is displayed after a match has been found on a person who selected the same category, subcategory and generated the request from a location lesser than 10 miles from the other person who chose the same selection(category and subcategory) on the application. The information pertaining to the user such as name, contact details are shared so that they have the opportunity to connect. This application is a simulation of user connect in a university setting with a custom-built database and can also be deployed on to a cloud.

Index Terms— University connect, Match interest, User info sharing.

**Full Project Description **

Abstract— Individuals who have interest participating in activities such as sports, gaming, gyms, etc. often end up dropping their plans if their friends do not turn up when called upon to engage in the same activity of their interest. With the AccompanyME web application he/she can connect with the other person without having to look around for groups or clubs where they can find a companion.

I.	INTRODUCTION

With the technology space growing rapidly there’s also a growing sense of disconnect among the people. Meetings, hanging out with others have now become very uncommon and people often find themselves deserted and alone due to the lack of connectivity. Even those who want to network and socialize face several challenges as there are no channels which give a one stop solution to the problem of bringing like minds together. One such challenge in particular is to connect people who share similar passions and hobbies and are in need of a companion to share their ideas with, meet up and discuss about opportunities that are related to their field, a person who is interested in engaging in the same activity as they are and might be interested in working on the same kind of stuff that the other person is . Say for example a person wants to play baseball but none of his friends accompany him leaving him stranded and more often than not cancelling the plan. This application tries to bridge the gap between the users and helps them pursue their interest.

This application could especially help someone who is new to a place or city. The app allows you to explore and find other people on the internet and unlike other applications which gives a suggestion or a place to go the AccompanyME app actually, provides the user details and an opportunity to connect with them. The additional security measure to allow only verified users to use the system(a university setting in this case where it is assumed that only the person having a valid varsity email ID is allowed to register into the system) and prevents the misuse of information that is being shared in the application. It ultimately gives user the ability to take a final call on the information provided by the system. This makes AccompanyME a trustworthy and steadfast app. It is tested with all the possible cases to make sure that it is robust and well-built along with being a secure application.

The scope of this application is only restricted by the number of categories and subcategories that are being added in the system but it can be updated regularly and our effort is to add as many as we can to start with and update based on the user’s request after the system is deployed. This feature provides great opportunity for the programmer to understand the user requirements and keep making updates using a feedback system. It is easy to deploy and redeploy the application on cloud using EC2 (a future work proposed in section IV) making maintenance manageable and simple.

II.	RELATED PROJECT WORKS

A.	Hobbiespot 

Applications available in the market such as Hobbiespot come close to the AccompanyME app but the functionalities of the app are considerably different. Hobbiespot is mainly focused on finding hobbies/people/places near you based on your interest, it does not provide the details of the users who have selected the same hobby. It allows you to view events that people have attended and share it with others using social media platforms such as twitter, Facebook etc. It is an android application with about 200 downloads which makes it different from a web application. However, AccompanyME lacks features such as social media sharing of events that are happening nearby. Also, the AccompanyME app operates with the users in a particular organization such as a university to protect the identity of the users. This feature greatly reduces the risk of data being misused by individuals using the application [1].

B.	Google’s Neighbourly app 

   The other application which operates on similar lines is the Google’s Neighbourly app. This allows the users to help learn about the neighborhood by asking questions to other residents residing in the vicinity. It lets you find facilities and services in your area which might come in handy. All the places which you might need to visit in the near future are listed on the application based on user location. No personal information from the other users is shared though, it lets you see the profile picture and the first name. The scope of this application is limited to a particular city and it was launched as a pilot project by google in May 2018. The only city included to this was Mumbai and there have not been any updates to it since its first launch. Again, given the nature of functionalities included in this application, it is considerably different from AccompanyME [2].
   
C.	Tinder
Another popular app ‘Tinder’ is in comparable terms with the AccompanyME app if functionality is strictly taken into consideration but again Tinder is classified as a dating app with features such as chat, swipe select and depends on the user to select or unselect based on the profile picture/interests and both the users need to select each other for the next step to kick in. This is an app with more than a million downloads and one of the best rated on play store. AccompanyME chooses interest category and subcategory to filter the results unlike this app and although the AccompanyME may seem like a dating app it defers in many ways from other dating apps.

D.	Meetup
   Meetup is one application which comes close to AccompanyME in terms of matching user interests but all the app does is lists the events that are occurring near-by using the user location and this is based on subscription of your interested category during the registration stage and keeps updating regularly when the invites are sent out. The application does not give the opportunity to connect with anyone but lists the attendees and the users who plan to attend the event. User needs to attend the event in order to get in touch with the people and the app does not provide any inherit features to do so. 
            None of the products available in the market replicate the same functionalities of this application and it is unique in terms of development too since it is a web application.
            
III.	SOLUTION

The first step towards building a solution is to maintain discretion on the data. The application is able to achieve this using feature such as OTP for verification and validation from the university student database. Only if the OTP matches the user is allowed to register. Secondly, finding the location from the webpage is done using GoogleAPI and it is only after the user is notified from a pop-up seeking his permission to do so, the location is captured. This value is relative to the user’s location and he can use the system from anywhere irrespective of the fact that he has used the system before. The user can change his selection at any point of the time unlike other applications which restrict the user to subscribe to a particular set of hobbies or activities he is interested in and are notified if events are being organized related to them.

    The goal of the application is achieved using a web application which reads three values from the user i.e. Category, subcategory and the user’s location. Once these are fed into the system a search operation is carried on the database using advanced queries which take the distance as an additional criterion (which is pre-determined to be 10 miles taking into consideration an average radius of a university campus area). Once the query is fired the results are displayed on the webpage with all the information.

A.	Technologies/Languages Used
   Node JS – It is a platform which runs on Chrome’s JavaScript and allows us to build fast network applications. It is an event-driven, non-blocking Input/output model which is perfectly suited for data-intensive and real time applications that run on multiple devices and across a network [3].

   Express JS – It is a web framework coupled with NodeJS and used for easy creation of web applications. It makes development simpler also making it secure, following a modular approach making it faster at the same time [4].

   MySQL Server – It is a free open source software provided by oracle for relational database management system and is based on Structured query language (SQL). It can be used in a wide range of applications; MySQL is often associated with most of the web applications. It is the used as a storage unit for all the information that is passed through-out the system.

   HTML, CSS and Bootstrap – Hypertext Markup Language (HTML) is a standard mark-up language for displaying documents on the web browser. It is commonly coupled with CSS (Cascading style Sheets) and scripting languages. Bootstrap gives the application a better look and feel giving a wide range of styling classes to add to the HTML format when designing a webpage. These are primarily used in designing the part of the application viewed by the user. The application is developed using node JS, ExpressJS, MySQL Server, HTML, CSS, bootstrap. Node JS is mainly used to build the application validation for the derived values from the front end. Using a storage database instead of using session data increases the reliability on the data and protects the data in case of a crash. Front end elements are designed using HTML (Hypertext markup language), CSS (Cascading stylesheets) and bootstrap. ExpressJs acts as a medium.

   The system validates the information and provides the search result based on the user input. If the user values match, then the system displays the matched user information. This gives the user the choice to discard the search results if he is not comfortable with the system. The application can be accessed from any location since it uses a google API which is a free open source API provided by google for web applications.

B.	Issues/Challenges

   Selecting the platform for development of the project was one of the most challenging tasks. Web development was new to us and we had to learn new languages to achieve the end results. After researching and noticing the future scope for our application it was found that Node JS can be used for server-side scripting. We choose NodeJS because, for moving the backend on cloud such as AWS will be easier as for the basic services which we will require like AWS Lambda, API Gateway or AWS Instances it will be easier. To develop the authentication part for verifying new user through using OTP was again a challenge to develop. In the later part of implementation, we figured that for passing the parameters from the UI to server dynamically we need to have AJAX also implemented on the client side. Hence, we had revise all our EJS (Embedded Java Systems) templates residing in view folder by adding the ajax part wherever necessary. Apart from all this, learning these concepts from various different sources like LinkedIn learning, YouTube and many more different URL's on google was a big challenge.
   Another critical challenge we faced was to write a query which will display all those users who were in the range of 10 miles from the user with interest. Having only the latitude and longitude of the user calculating the distance was bit complicated. This was achieved using a complex query which calculates the sin and cos values to locate the user.
IV.	SUMMARY AND FUTURE SCOPE

   The Project was implemented as a web application and is restricted to the members in the university. However, the next versions of the application can be used a target a wider audience.

The following features have been considered on the future scope of this application.

1.	Deploying the application on AWS EC2 to make it available as a website and allow users across the university to use this app.

2.	Including an Enterprise version of the database and including our own API’s to access the database from a remote location. The database used currently allows the access of the application in the local machine. 

3.	Adding new categories and subcategories as the newer versions of the application are released for the user to choose from since the application is now restricted only to the one’s provided by the system.

4.	Allowing the user to choose the distance for the search (Since the current version of the application is restricted to a university, the search distance has been limited to 10 miles).

5.	Adding a feature which allows users to chat within the application once they are matched. They will then be able to connect directly without sharing their information such as phone number or email.

