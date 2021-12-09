---
layout: article
title: Employee Dashboard
author: alex
tags: Employee Dashboard LinkedChain Experience Verification Approve Reject Pending
aside:
    toc: true

---

This is an installment of the ECS 265 Project Blog on **LinkedChain**. LinkedChain makes the employee experience storage and verification more secure and efficient, and provides a new mechanism of hiring new candidates. We are a team of four MS CS graduate students (Naveen Kanuri, Aditya Parab, Abhishek Gokhale, and Maanas Vohra) attending the ECS 265 Distributed Database Systems and we will present LinkedChain as our project.
{:.info}

This portal will be used for employee registration, submission of employee experience verification requests to the required employer, and maintaining a history of submitted requests. The dashboard will also show if the request has been approved, rejected, or if it's yet to be processed (pending). 

The frontend is built using Angular. We are using the Ethereum blockchain and Polygon framework for the backend implementation.

## Employee Registration
Potential Employees can use this portal to register and put up their details on the blockchain, therefore providing substantial protection against attacks and data breaches.

The fields to be submitted are:

1. **Employee Public Key**: Public Key of Employee
2. **Employee SSN**: Social Security Number required for unique identification
3. **Employer Name**: Name of the Employer
4. **Employer Address**: Address of the Employee
5. **Employee Phone Number**: Phone number of Employee

When we click on submit, the prompt asks us to verify the submitted details. This prevents unnecessary and accidental Matic expenditure used to add records to the Ethereum blockchain.

The following GIF elucidates the registration procedure.

![Employee Registration Process]({{ site.baseurl }}/assets/videos/employee_registration.gif)

## Employee Dashboard
Upon successful registration of Employee profile, the user reaches the Employee Dashboard. This displays the Employee details along with the current status of the submitted employee experience verification requests. The requests are sent via the form to those employers that the user has worked with. 

The process of successful registration is shown in the below GIF. 

![Employee Successful Registration Process]({{ site.baseurl }}/assets/videos/employee_successful_registration.gif)

Once the employer accepts the user's request and thereby acknowledges that their employment history with that organization is valid, the status becomes approved. 

The process of an approved experience is shown in the following [video](https://drive.google.com/file/d/1nqQfDFeQc6mQNrkgRMkp7FGxo0Kj0RL4/view?usp=sharing)

The process of a rejected experience is shown in the following [video](https://drive.google.com/file/d/1nlR23OeLz08E2V6fRsR4tWTfjPSOO0i_/view?usp=sharing)

