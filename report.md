# lab6-microservices!

This is the report for **lab6-microservices**.

## The two microservices `accounts (2222)` and `web` are running and registered (two terminals, logs screenshots)

- Accounts microservice is registered in port 2222
![Account 2222](report_images/AccountLog.PNG)
- Web microservice is registered in port 3333
![Web 3333](report_images/WebLog.PNG)
## The service registration service has these two microservices registered (a third terminal, dashboard screenshots)
- Registration service shows the first two microservices registered
	 - Registration log (port 1111)
![Registration 1111](report_images/RegistrationLog.PNG)
	- Dashboard (localhost:1111)
![Dashborad 1](report_images/Dashboard.PNG)

## A second  `accounts`  microservice instance is started and will use the port 4444. This second  `accounts (4444)`  is also registered (a fourth terminal, log screenshots).

- Accounts microservice is registered in port 4444
![Account 4444](report_images/NewAccount4444.PNG)

> to do so you have to change the proper `applications.yml` with the specified port and run it in another terminal as `gradle :accounts:bootRun`

-  Registration service dashboard shows the first  two microservices registered and this new one
![Dashboard 2](report_images/Dashboard_two_accounts.PNG)

##  What happens when you kill the microservice  `accounts (2222)`  and do requests to  `web`?  
   

Since the `accounts (4444)` microservice is still running and registered in Eureka , the web service can provide information about accounts. 
- ![Account 2222 down](report_images/Account_2222_takedown.PNG)
- Still working after 2222 was taken down
![Account 2222 down web browser](report_images/StillWorkingAfter2222down.PNG)
