# Azure to AWS Server Migration

Presentation Link
https://drive.google.com/drive/folders/1QY62HKwsK-bm_K4IJ5ICZOTCWpVLpBzg

This project demonstrates the successful migration of Virtual Machines (VMs) and associated resources from **Microsoft Azure** to **Amazon Web Services (AWS)** using the AWS Application Migration Service. The process ensures minimal downtime, secure data transfer, and data integrity, enabling workloads to benefit from AWS's scalable infrastructure.

## Table of Contents
1. [Introduction](#introduction)
2. [Project Objective](#project-objective)
3. [Tools and Technologies Used](#tools-and-technologies-used)
4. [Step-by-Step Process](#step-by-step-process)
5. [Validation and Testing](#validation-and-testing)
6. [Conclusion](#conclusion)
7. [Contact](#contact)


   ![AWS Application Migration Service](https://github.com/user-attachments/assets/67e93db6-46f9-4e24-aeeb-e0cbb39f8d53)


---

## Introduction
Server migration involves transferring workloads between cloud platforms to leverage better services, scalability, and cost-efficiency. This project utilizes **AWS Application Migration Service** to automate replication and migration, ensuring a seamless transition.

---

## Project Objective
- **Source Platform**: Azure - Virtual Machines, Resource Groups, and Networking.
- **Target Platform**: AWS - EC2 Instances with supporting networking components (VPC, Elastic IP).
- **Goal**: Achieve a smooth migration with minimal downtime while maintaining data integrity.

---

## Tools and Technologies Used
- **Microsoft Azure**: Virtual Machines, Networking Components.
- **AWS Services**:
  - **Application Migration Service**: For automated replication and migration.
  - **IAM**: To generate access and secret keys.
  - **Elastic IP**: For assigning static IP addresses to AWS instances.
- **Nginx**: For testing server functionality.
- **Windows PowerShell**: For executing AWS replication commands.

---

## Step-by-Step Process

### Pre-Migration
1. Set up Azure resources:
   - Create a Resource Group and Virtual Machine.
   - Install and configure **Nginx** for testing.
   - Add test data to an additional Azure disk.

2. Generate AWS access and secret keys in IAM.
3. Prepare AWS Application Migration Service templates:
   - **Replication Template**: Define replication settings.
   - **Launch Template**: Configure target EC2 instances.
   - **Post-Launch Template**: Set actions for post-migration.

---

### Migration Execution
1. Install AWS replication agent on the Azure VM.
2. Start replication in AWS Application Migration Service.
   - This process includes synchronizing services such as EC2, volumes, and snapshots.
3. Test the migrated instance:
   - Launch a test instance.
   - Verify data and application functionality.

4. Perform the final cutover:
   - Mark the instance as "ready for cutover."
   - Launch the final instance.
   - Assign Elastic IP and validate server access.

---

## Validation and Testing
- Confirm the availability of test data in AWS.
- Validate **Nginx** functionality on the migrated instance.
- Ensure a healthy state for the final instance with no downtime.

---

## Conclusion
This project successfully migrated Virtual Machines from Azure to AWS. The process was streamlined using automation, ensuring minimal downtime and robust data integrity. The new AWS environment offers scalability and cost efficiency for future needs.

---

## Contact
For any questions or further information, please contact:  
**Dhavanisha Jegannathan**  
**Email**: dhavanisha.jp@gmail.com
