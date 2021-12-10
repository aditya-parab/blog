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

## Employer Registration

Once we arrive on the employer URL, if we aren't registered as an employer or employee before, we can access the registration page. If we're registered as an employer, we can see the employer dashboard. If we've registered as an employee, the page redirects to the employee dashboard.

On the employer registration page, once the form is validated, the confirmation dialog opens. The new employer has the option to confirm the details before submitting, which helps to avoid unnecessary Matic expenditure used while writing records on the Blockchain. Once the details are submitted and the transaction confirmed from the Metamask wallet, the details are written on the blockchain, and finally the page redirects to show the employer dashboard. 

![Employer Registration Activity Diagram]({{ site.baseurl }}/assets/images/LinkedChain/EmployerRegistrationActivityDiagram.jpg)
> Activity Diagram for Employer Registration

## Employer Dashboard

On the employer dashboard, the employer can go through the approved and rejected experiences related to that employer only, and filter and sort them. The employer can also go through the pending experiences, filter and sort them, and approve or reject an experience (with comments if required). Once the experience is approved/rejected, it would show in the approved/rejected list for that employer. 

The employer can also go through all approved experiences of all approved experiences and filter and sort them. This functionality can be used by an employer to verify a new or potential employee's work experiences.

![Employer Dashboard Activity Diagram]({{ site.baseurl }}/assets/images/LinkedChain/EmployerDashboardActivityDiagram.jpg)
> Activity Diagram for Employer Dashboard

## Employee Registration

This is similar to the employer registration process. Once we arrive on the employee URL, if we aren't registered as an employer or employee before, we can access the registration page. If we're registered as an employee, we can see the employee dashboard. If we've registered as an employer, the page redirects to the employer dashboard.

On the employee registration page, once the form is validated, the confirmation dialog opens. The new employee has the option to confirm the details before submitting, which helps to avoid unnecessary Matic expenditure used while writing records on the Blockchain. Once the details are submitted and the transaction confirmed from the Metamask wallet, the details are written on the blockchain, and finally the page redirects to show the employee dashboard. 

![Employee Registration Activity Diagram]({{ site.baseurl }}/assets/images/LinkedChain/EmployeeRegistrationActivityDiagram.jpg)
> Activity Diagram for Employee Registration

## Employee Dashboard

On the employee dashboard, the employee can go through all the submitted experience verification requests which show the status of the request. The status of a request can be "Pending", "Approved", or "Rejected". The employee can also filter and sort them. 

The employee can also submit the request by entering the relevant experience details. Once the form is validated, the confirmation dialog opens. This helps to avoid unnecessary Matic expenditure used while writing records on the Blockchain. Once the details are submitted and the transaction confirmed from the Metamask wallet, the details are written on the blockchain, and finally the page redirects to show the employee dashboard with the new request having status as "Pending" added to the existing list. 

![Employee Dashboard Activity Diagram]({{ site.baseurl }}/assets/images/LinkedChain/EmployeeDashboardActivityDiagram.jpg)
> Activity Diagram for Employee Dashboard
