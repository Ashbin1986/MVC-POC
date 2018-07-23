# MVC-POC
Develped with (DI+MVC+EntityFrmework) AND(WebAPI+EntityFramework)

MVC WebAPP:

Step1 : There is HealthCareDBScript.sql inside the Evolent.HealthCare.rar folder - run that script in SQL server.
Step2: Cross check the connection string in MVC Project & WebAPI project : data source=(local)(This should be installed SQL server name)
<connectionStrings>
    <add name="HealthCareEntities" connectionString="metadata=res://*/DataAccess.HelathCare.csdl|res://*/DataAccess.HelathCare.ssdl|res://*/DataAccess.HelathCare.msl;provider=System.Data.SqlClient;provider connection string=&quot;data source=(local);initial catalog=HealthCare;integrated security=True;MultipleActiveResultSets=True;App=EntityFramework&quot;" providerName="System.Data.EntityClient" />
  </connectionStrings>
Step3 : Set as StartUpPoject to  Evolent.HealthCare and press f5 to view the application and perform Crud operations.

WebAPI Project 

Step1 : There is HealthCareDBScript.sql inside the Evolent.HealthCare.rar folder - run that script in SQL server.if already ran then ignore it. 
Step2 :  Set as startup project to Evolent.HealthCare.WEBAPI
Step3 : Press f5 to run the app.

Actions: Add Contact
Step4 : Open the Post man -Paste the url http://localhost:58585/api/contact/addContact
           Request : {

          "Email" : "ashbin.kumar@gmail.com",
          "FirstName":"Ashvin",
          "LastName":"Kumar",
          "PhoneNumber":"16238127"

                     }
Actions: Update Contact:http://localhost:58585/api/contact/UpdateContact
Request : {
	"ContactID" : "3c1b8100-a8e5-471c-b10a-9321272526b8"
	"Email" : "ashbin.kumar@gmail.com",
	"FirstName":"Ashvin",
	"LastName":"TestUser",
	"PhoneNumber":"16238127"
	
}

Action : DeleteContact  http://localhost:58585/api/contact/DeleteContact
Request :
{
	"ContactID" : "3c1b8100-a8e5-471c-b10a-9321272526b8"
	
}

                     
                     

