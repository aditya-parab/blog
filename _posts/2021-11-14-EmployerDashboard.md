---
layout: article
title: Employer Dashboard
author: alex
tags: Employer Dashboard LinkedChain Experience Verification Approve Reject Pending
aside:
    toc: true

---

This is an installment of the ECS 265 Project Blog on **LinkedChain**. LinkedChain makes the employee experience storage and verification more secure and efficient, and provides a new mechanism of hiring new candidates. We are a team of four MS CS graduate students (Naveen Kanuri, Aditya Parab, Abhishek Gokhale, and Maanas Vohra) attending the ECS 265 Distributed Database Systems and we will present LinkedChain as our project.
{:.info}

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

