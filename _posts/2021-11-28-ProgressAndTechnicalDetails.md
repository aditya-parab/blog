---
layout: article
title: Progress and Technical Details
author: alex
tags: Progress Technical Details Employer Employee Experience Accept Reject Angular Blockchain Ethereum
aside:
    toc: true

---

This is an installment of the ECS 265 Project Blog on **LinkedChain**. LinkedChain makes the employee experience storage and verification more secure and efficient, and provides a new mechanism of hiring new candidates. We are a team of four MS CS graduate students (Naveen Kanuri, Aditya Parab, Abhishek Gokhale, and Maanas Vohra) attending the ECS 265 Distributed Database Systems and we will present LinkedChain as our project.
{:.info}

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

