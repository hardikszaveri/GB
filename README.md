# GB
A Pet Weather solution build using two separate applications and make them work together to help answer the question: Does my pet need an umbrella?

Solution Brief:
A solution named SlnGasBuddy has been built for Pet Weather assignment which contains following projects 
-	PetDBStore
A database project which contains database objects creation scripts and sample data creation scripts.
-	PetWeatherApp
It is web application where homepage displays all Pets from the Pet Shelter API, Clicking on a Pet take you to the Pet details page which shows details for that particular Pet along with Google Map. Along with that, it also provides Pet creation functionality.
-	PetShelterAPI
It manages database of Pets and provide three RESTful JSON API endpoints :
1. An index of Pets
2. Pet lookup by ID
3. Pet creation with proper error checking for:
This application is built using ASP.Net Web API and uses Entity Framework to interact with database.	 

The technologies used for this project are .Net Framework 4.5, C#, ASP.Net MVC, ASP.Net Web API, Entity Framework, BootStrap, JQuery, SQL Express, Open Weather API, Google Map API etc.
The following are some of the features of application:
1)	Responsive design and Rich UI
2)	Latitude and longitude validation to make sure capture correct data
3)	Use of Jmelosegui.Mvc.GoogleMap NuGet paclage to use Google map for showing map on application
4)	Use of Open Weather API to determine weather condition
5)	Cashing of Configuration related settings
6)	Location determination based on longitude and latitude value
7)	PetShelterAPI is RESTful JSON so it can be targeted to various devices i.e. laptop, tablet, phone etc.

How to setup and run SlnGasBuddy
1)	Open SlnGasBuddy solution 
2)	Go to PetDBStore project and deploy Pet.SQL file followed by Pet.Data.SQL file to existing database or new database
3)	Go to PetShelterAPI project and make following changes in root web.config file
Search for PetsDataStoreEntities connectionstrings key and change its conectionstring value to database which holds PetDBStore objects which we deployed in step 1.
4)	Deploy PetShelterAPI project on IIS 
5)	Go to PetWeatherApp project and make following changes in root web.config file
Search for PetShelterAPIBaseURL key and set its value to path where PetShelterAPI deployed
Search for OpenWeatherAppId key and set its value to API key which you get by registering yourself at OpenWeatherAPI site https://openweathermap.org/appid.
This key is required to determine weather condition based on longitude and latitude value.
Search for GoogleMapKey key and set its value to API key which you get by registering yourself at https://developers.google.com/maps/documentation/javascript/get-api-key  site
6)	Deploy PetWeatherApp project on IIS 
7)	You can run PetWeatherApp project to test PetWeatherApp
