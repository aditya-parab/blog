---
layout: article
title: Problem Statement and Introduction to LinkedChain
author: alex
tags: Problem Statement Introduction LinkedChain
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

