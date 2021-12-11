---
layout: article
title: LinkedChain Application
author: alex
tags: Problem Statement Introduction LinkedChain Employer Employee Dashboard LinkedChain Experience Verification Approve Reject Pending Progress Technical Details Accept Angular Blockchain Ethereum Future Work
aside:
    toc: true

---

This is an installment of the ECS 265 Project Blog on **LinkedChain**. LinkedChain makes the employee experience storage and verification more secure and efficient, and provides a new mechanism of hiring new candidates. We are a team of four MS CS graduate students (Naveen Kanuri, Aditya Parab, Abhishek Gokhale, and Maanas Vohra) attending the ECS 265 Distributed Database Systems and we will present LinkedChain as our project.
{:.info}

## Problem Statement
Currently, the standard employee recruiting process involves working with large amount of PII data, which usually resides in the cloud. Companies such as <a href="https://www.workday.com/">*Workday*</a> and <a href="https://www.smartrecruiters.com/">*SmartRecruiters*</a> face huge challenges in securely storing this data. In the recent years, the surge in data breaches have led to increased research in finding secure data storage methods. 

Moreover, potential employees can submit fraudulent data, leading to increased verification costs and wastage of time. For instance, the way of verifying a candidate’s employment history is to check the relieving/experience letter, which can be easily forged. 

Furthermore, this background verification can become complicated when an employee’s records get lost (which often happens in the case of interns) over time. It becomes more difficult if an employer (say, a startup) shuts down and there is no way of verifying records in such a case. In addition, there is no formalization of this verification process, which leads to discrepancies between companies when an employee changes the company.

## The Solution: LinkedChain
To overcome such concerns, we have come up with **LinkedChain**, a secure employee experience management system, as a solution. LinkedChain uses a blockchain to store critical employee/employer information which is confirmed by both parties and then formalized on a blockchain. Blockchain is used since it becomes very difficult to commit external hacks of sensitive records Therefore, it drastically reduces the chances of attacks and data breaches. Moreover, access to the blockchain is limited and controlled and even those with access can’t arbitrarily make changes to the record. This way, the verification costs and time are optimized. Furthermore, the data persists on the blockchain, and thus, its existence doesn't depend on the current status of the company. This doesn't lead to data invalidation when the company ceases to exist. Finally, the main goal of LinkedChain is to be a standard method of employment verification. This kind of technology can be groundbreaking in the HR departments of different companies as they will have a communication standard and work experience can be legitimized.


This portal will be used for employer registration, approving or rejecting the employees' experience verification requests, and maintaining a history of approved, pending, and rejected requests. 

The dashboard will also show all approved experiences of all the employees, thus maintaining a global database of potential employees. The employers can, therefore, use the search functionality to verify the work experience of a potential or new employee. Moreover, this can be used by recruiters to see which potential employees have worked with the required characteristics: for now, the search functionality allows the search for previous employers', experience duration, and designation. 

The frontend is built using Angular. We are using the Ethereum blockchain and Polygon framework for the backend implementation.

## Employer Registration
Potential employers can use this portal to register and put up their details on the blockchain, therefore providing substantial protection against attacks and data breaches.

The fields to be submitted are:

1. **Employer Public Key**: Public key of employer
2. **Employer Name**: Name of the employer
3. **Employer Address**: Address of the main headquarters of the employer
4. **Employer Phone Number**: Phone number of employer
5. **Employer URL**: URL link to Employer webpage
   
When we click on submit, the prompt asks us to verify the submitted details. This prevents unnecessary and accidental Matic expenditure used to add records to the Ethereum blockchain.

The following GIF elucidates the registration procedure.

![Employer Registration Process]({{ site.baseurl }}/assets/videos/employer_registration.gif)

## Employer Dashboard
Upon successful registration of employer profile, the user reaches the employer dashboard. This displays the employer details along with the current status of the employee experience verification requests pertaining to that employer. The dashboard displays the approved, rejected and pending work history requests from various employees for that particular employer (The employer can also choose to filter the Approved, Removed & Pending experiences by a given string).

The process of successful registration is shown in the below GIF. 

![Employer Successful Registration Process]({{ site.baseurl }}/assets/videos/employer_registration_successful.gif)

The employer can choose to approve or reject from the pending requests, upon which the record will be added under the Approved or Rejected table, and the status will be updated on the employees side as well.

The process of an approved experience is shown in the following [video](https://drive.google.com/file/d/1nqQfDFeQc6mQNrkgRMkp7FGxo0Kj0RL4/view?usp=sharing)

The process of a rejected experience is shown in the following [video](https://drive.google.com/file/d/1nlR23OeLz08E2V6fRsR4tWTfjPSOO0i_/view?usp=sharing)

The employer can also search through the approved experiences of the different employees working for all available employers.


This portal will be used for employee registration, submission of employee experience verification requests to the required employer, and maintaining a history of submitted requests. The dashboard will also show if the request has been approved, rejected, or if it's yet to be processed (pending). 

The frontend is built using Angular. We are using the Ethereum blockchain and Polygon framework for the backend implementation.

## Employee Registration
Potential Employees can use this portal to register and put up their details on the blockchain, therefore providing substantial protection against attacks and data breaches.

The fields to be submitted are:

1. **Employee Public Key**: Public key of employee
2. **Employee SSN**: Social Security Number required for unique identification
3. **Employee Name**: Name of the employee
4. **Employee Address**: Address of the employee
5. **Employee Phone Number**: Phone number of employee

When we click on submit, the prompt asks us to verify the submitted details. This prevents unnecessary and accidental Matic expenditure used to add records to the Ethereum blockchain.

The following GIF elucidates the registration procedure.

![Employee Registration Process]({{ site.baseurl }}/assets/videos/employee_registration.gif)

## Employee Dashboard
Upon successful registration of employee profile, the user reaches the employee dashboard. This displays the employee details along with the current status of the submitted employee experience verification requests. The requests are sent via the form to those employers that the user has worked with. 

The process of successful registration is shown in the below GIF. 

![Employee Successful Registration Process]({{ site.baseurl }}/assets/videos/employee_successful_registration.gif)

Once the employer accepts the user's request and thereby acknowledges that their employment history with that organization is valid, the status becomes approved. 

The process of an approved experience is shown in the following [video](https://drive.google.com/file/d/1nqQfDFeQc6mQNrkgRMkp7FGxo0Kj0RL4/view?usp=sharing)

The process of a rejected experience is shown in the following [video](https://drive.google.com/file/d/1nlR23OeLz08E2V6fRsR4tWTfjPSOO0i_/view?usp=sharing)


LinkedChain is a web application with the frontend built using Angular. We are using the Ethereum blockchain and Polygon framework for the backend implementation. The following explains the technical details with the help of a Gantt chart and relevant UML diagrams. 

## Progress

We divided the tasks over the course of nine weeks among ourselves and finished each task per week timely.

![Gantt Chart ECS 265]({{ site.baseurl }}/assets/images/LinkedChain/GanttChart.png)
> Gantt Chart for ECS 265

## Employer

### Employer Registration

Once we arrive on the employer URL(`domainName/employer`), if we aren't registered as an employer or employee before, we can access the registration page. If we're registered as an employer, we can see the employer dashboard. If we've registered as an employee, the page redirects to the employee dashboard.

On the employer registration page, once the form is validated, the confirmation dialog opens. The new employer has the option to confirm the details before submitting, which helps to avoid unnecessary Matic expenditure used while writing records on the Blockchain. Once the details are submitted and the transaction confirmed from the Metamask wallet, the details are written on the blockchain, and finally the page redirects to show the employer dashboard. 

![Employer Registration Activity Diagram]({{ site.baseurl }}/assets/images/LinkedChain/EmployerRegistrationActivityDiagram.jpg)
> Activity Diagram for Employer Registration

### Employer Dashboard

On the employer dashboard, the employer can go through the approved and rejected experiences related to that employer only, and filter and sort them. The employer can also go through the pending experiences, filter and sort them, and approve or reject an experience (with comments if required). Once the experience is approved/rejected, it would show in the approved/rejected list for that employer. 

The employer can also go through all approved experiences of all approved experiences and filter and sort them. This functionality can be used by an employer to verify a new or potential employee's work experiences.

![Employer Dashboard Activity Diagram]({{ site.baseurl }}/assets/images/LinkedChain/EmployerDashboardActivityDiagram.jpg)
> Activity Diagram for Employer Dashboard

## Employee

### Employee Registration

This is similar to the employer registration process. Once we arrive on the employee URL (`domainName/employee`), if we aren't registered as an employer or employee before, we can access the registration page. If we're registered as an employee, we can see the employee dashboard. If we've registered as an employer, the page redirects to the employer dashboard.

On the employee registration page, once the form is validated, the confirmation dialog opens. The new employee has the option to confirm the details before submitting, which helps to avoid unnecessary Matic expenditure used while writing records on the Blockchain. Once the details are submitted and the transaction confirmed from the Metamask wallet, the details are written on the blockchain, and finally the page redirects to show the employee dashboard. 

![Employee Registration Activity Diagram]({{ site.baseurl }}/assets/images/LinkedChain/EmployeeRegistrationActivityDiagram.jpg)
> Activity Diagram for Employee Registration

### Employee Dashboard

On the employee dashboard, the employee can go through all the submitted experience verification requests which show the status of the request. The status of a request can be "Pending", "Approved", or "Rejected". The employee can also filter and sort them. 

The employee can also submit the request by entering the relevant experience details. Once the form is validated, the confirmation dialog opens. This helps to avoid unnecessary Matic expenditure used while writing records on the Blockchain. Once the details are submitted and the transaction confirmed from the Metamask wallet, the details are written on the blockchain, and finally the page redirects to show the employee dashboard with the new request having status as "Pending" added to the existing list. 

![Employee Dashboard Activity Diagram]({{ site.baseurl }}/assets/images/LinkedChain/EmployeeDashboardActivityDiagram.jpg)
> Activity Diagram for Employee Dashboard

## File Structure

The file structure of LinkedChain when using `tree WorkExValidator/ -I node_modules -L 4` gives:

```rust
maanas@LAPTOP-DLRDBUGV:/mnt/d/Users/maana/Desktop/UC Davis/Projects/WorkExValidator-ADP$ tree WorkExValidator/ -I node_modules -L 4
WorkExValidator/
├── README.md
├── angular.json
├── blockchain
│   ├── artifacts
│   │   ├── blockchain
│   │   │   └── contracts
│   │   └── build-info
│   │       └── d61cfb86b0401b540a5b339376cbe521.json
│   ├── cache
│   │   └── solidity-files-cache.json
│   ├── contracts
│   │   └── WorkEx.sol
│   ├── scripts
│   │   └── deploy.js
│   └── test
│       └── test.js
├── environment
│   ├── contract-address.json
│   └── secrets.json
├── environment_bak
│   ├── contract-address.json
│   └── secrets.json
├── hardhat.config.js
├── karma.conf.js
├── package-lock.json
├── package.json
├── personal details
├── src
│   ├── app
│   │   ├── app-routing.module.ts
│   │   ├── app.component.css
│   │   ├── app.component.html
│   │   ├── app.component.spec.ts
│   │   ├── app.component.ts
│   │   ├── app.module.ts
│   │   ├── dialogs
│   │   │   └── confirm
│   │   ├── employee
│   │   │   ├── employee.component.css
│   │   │   ├── employee.component.html
│   │   │   └── employee.component.ts
│   │   ├── employer
│   │   │   ├── employer.component.css
│   │   │   ├── employer.component.html
│   │   │   └── employer.component.ts
│   │   └── services
│   │       ├── dialog.service.spec.ts
│   │       └── dialog.service.ts
│   ├── assets
│   │   └── Mumbai.png
│   ├── custom-theme.scss
│   ├── environments
│   │   ├── environment.prod.ts
│   │   └── environment.ts
│   ├── favicon.ico
│   ├── index.html
│   ├── main.ts
│   ├── polyfills.ts
│   ├── styles.css
│   └── test.ts
├── tsconfig.app.json
├── tsconfig.json
└── tsconfig.spec.json

20 directories, 43 files
```

### File Overview

Following is an overview of the important files of the project.

| File/Directory | Description | 
| -------------- | ----------- | 
| :scroll: `blockchain/contracts/WorkEx.sol` | Contains the Solidity contract used to write records on the Ethereum blockchain. This has the required methods for employee registration, employer registration, and experience management. | 
| :scroll: `blockchain/scripts/deploy.js` | Script used to deploy the contract. The command `npx hardhat run blockchain/scripts/deploy.js --network mumbai` is used. |
| :scroll: `blockchain/test/test.js` | Tests written for the contract. The command `npx hardhat test` is used. | 
| -------------- | ----------- |
| :floppy_disk: `environment/secrets.json` | Contains the Mumbai network's blockchain endpoint and secret key of contract creator account. |
| :file_folder: `src/app/dialogs/confirm` | Contains the details for the confirm component. This component generates the confirmation dialog after submitting details during employee registration, employer registration, and employee experience submission. | 
| :file_folder: `src/app/employee` | Contains the details for the employee component. This component contains the employee registration page and employee dashboard details. |
| :file_folder:  `src/app/employer` | Contains the details for the employer component. This component contains the employer registration page and employer dashboard details. |
| :file_folder: `src/app/services` | Contains the `DialogService` service which carries the message from the employee and employer components to generate the relevant confirmation dialog box. |


## Future Work
We aim to improve the current product by implementing more features in the future, such as:

 - Send status updates by email or push notification to subscribed users
 - Automatically import data from LinkedIn and send work history requests to Employers
 - Add more UI elements (e.g. loading screen, add more user interaction etc.)

## Demo

This is the demo for the LinkedChain project: [demo link](https://drive.google.com/file/d/1wnAw6QJL25qaYlb_K75zMOUw3DY-a0kv/view?usp=sharing)