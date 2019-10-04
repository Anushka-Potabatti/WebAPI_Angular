# WebAPI_Angular
A project to store and retrieve Training Information.

Application Details :

1.
TrainingInfoAPI : WebAPI Application
- This is a WebAPI project with Entity Framework.
- It is used to get data from DB and handover to caller application.
- It is used to add data to DB once it receives a post request.
- As required, the error message text for start date and end date validation should be defined externally. I assumed externally here means server side.
- After saving the application responds with Success message and sends number of days between the two date inputs.

2.
TrainingInfoAPI : Angular Application
- This application provides a UI form with input fields as training name, start date, end date, and a Confirm button to submit the form.
- On Confirmation of saving, Web API is called to save details to DB. It responds with Success message. Along with message, application displays number of days between the two date inputs which is calculated at ServerSide.
- Bootstrap is used for making the application responsive.

---------------------------------------------------------------------------------------------------------------------------
Steps To Execute :

1.
DB :
- Export DB to SQL Server

2.
Web API (TrainingInfoAPI):
- Open the project.
- Change connection details in Web.config.
	Key : TrainingEntities
	Change values for : data source, user id, password
- Right click on TrainingInfoAPI->Properties->Web
- Note down the ProjectURL.
- Execute the project

3.
Angular (TrainingInfoApp):
- Change the port number in the baseURL in training.service.ts line at line 12.
- Save and Run ng serve. 
- Navigate to http://localhost:4200/.   
