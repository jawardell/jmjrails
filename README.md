# JMJ Travel-Tracker

An automated solution for requesting, approving, and reimbursing corporate travel.


## Project Description 
> Create detailed reports for your corporate travel expenses and get them approved by your bosses quickly!

JMJ Travel Tracker is a product which allows someone in a corporate setting to create reimbursement requests and expense reports in order to be reimbursed for job related travel expenses. The application assumes a hierarchical structure consisting departments which have budgets and payment managers which have a one large budget comprising many departments' budgets. The departmental budgets are approved by the budget approvers. A payment manager is in charge of many departments at once and is in charge of approving all line items from the departments which they manage. In order to get a trip approved, an employee needs the approval of the budget approvers and ultimately the payment manager. If the budget approvers sign off on the line items, but the payment manager does not approve, the report is sent back to the employee, with  revisions annotated by the disapproving parties. The budget approvers can also decline an employee's request, add revision notes, and send the request back to the employee for resubmission.


### Two Step Reimbursement Process 
There are two major parts of the reimbursment process, namely, approving estimated expenses and approving actual expenses.

1. Pre-Approval: Trip Estimates
	- The employee submits a report outlining the expenses they intend to encounter during the trip. If the expenses seem reasonable, the budget approvers and payment managers will sign off on the trip. Once the trip is approved, the report status is updated and the employee is cleared to go on the trip.

	
2. Reimbursment Approval: Expenses Encountered
	- The employee records expenses that they encounter during the trip and adds new line items to their trip report. The employee uploads photos of receipts, actual costs, descriptions, and dates to the post-trip report. The report is submitted to the budget approvers again so that they can analyze the claimed expenses. If the expenses seem reasonable, the budget approvers sign off on the report and send it to the payment manager. If the payment manager signs off on the actual expenses, the trip is marked as approved and the employee's expenses will be processed for refund. 

	
	
### User Roles
There are three user entities in this application. 

* Employee
	- An employee is an entity which creates trip reports containing estimated and actual expenses.
* Budget Approver
	- The budget approver entity belongs to a department which has a budget allocated to it. The budget approver decides whether or not their departmental budget can reimburse the employee's estimated and/or actual expenses and approves/declines line items associated with their department.
* Payment Manager
	- Payment managers control many departments and thus are in charge of approving groups of line items belonging to many departments. This entity has the final say as to whether or not the estimated or actual expenses are approved. 

	
# Using this Project

You can use this project by either cloning the repository and running it locally using the sqlite database OR you can visit a live demo of the project which uses a postgres database.

## Live Demo
Please use firefox for this project. This project was created last year so the SSL certificate is not compliant with many operating systems after requirements for trusted certificates in iOS 13 and macOS 10.15 were modified. You can bypass these errors in Firefox. 

<a href="https://cox-oldfield-wardell.herokuapp.com">Demo Link</a>

## Running Locally
Clone the repositiory onto you're computer. 

Open up your bash terminal and type the following command: 

`git clone https://github.com/jawardell/jmjrails`

Great! Now move into the directory you just cloned: 

`cd jmjrails`

Now execute the configuration script: 

`./config.sh`

This will set up all of the cool gems, set up the yarn tools we used, and get the local server running. If you have problems with executing this script, you migth need to make it runnable with this command: `chmod +x config.sh`

You'll be ready to view the project when you see this in your terminal output: 

```* Listening on tcp://localhost:3000```

Open your Chrome browser and type `localhost:3000` in the address bar. 

Now you're using JMJ Travel Tracker! 

Some accounts were already created when you ran the `config.sh` script, but feel free to make your own accounts and play with the application.


## Authors
<a href="https://github.com/montrez">@montrez</a>

<a href="https://github.com/jboldfield">@jboldfield</a>
