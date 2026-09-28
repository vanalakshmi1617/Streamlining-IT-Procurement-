# Streamlining-IT-Procurement
Automating Standard Laptop Orders With Flow Designer
# ServiceNow – Standard Laptop Task Automation

## Project Overview

This project demonstrates how to automate the laptop request process in ServiceNow using Flow Designer. A flow is created to automatically generate a catalog task when a user submits a Standard Laptop request.

The project includes creating a flow, configuring the catalog item, and testing the automation by placing a laptop request.

## Objectives

* To create a flow using Flow Designer in ServiceNow.
* To automate catalog task creation.
* To configure assignment groups and approval status.
* To integrate the flow with a catalog item.
* To test the automated laptop request process.

## Tools and Technologies

* **Platform:** ServiceNow
* **Module:** Flow Designer
* **Application:** Global
* **Feature:** Service Catalog
* **Automation:** Create Catalog Task

## Activities

### Activity 1: Create a Flow Using Flow Designer

1. Open ServiceNow and navigate to **All**.
2. Search for **Flow Designer** under Process Automation.
3. Click **New** and select **Flow**.
4. Enter the following flow properties:

   * **Flow Name:** Standard Laptop Task
   * **Application:** Global
   * **Run As:** System User
5. Click **Submit**.
6. Click **Add a Trigger** and select **Service Catalog**.
7. Click **Done**.
8. Under Actions, click **Add an Action**.
9. Search for and select **Create Catalog Task**.
10. Configure the action with the following details:

| Field             | Value                     |
| ----------------- | ------------------------- |
| Request Item      | Requested Item Record     |
| Table             | Catalog Task              |
| Short Description | Laptop need to Configured |
| Description       | Laptop need to Configured |
| Assignment Group  | Hardware                  |
| Approval          | Approved                  |

11. Leave the remaining fields as default.
12. Click **Done** and save the flow.
13. Click **Activate** to activate the flow.

**Result:** A flow named Standard Laptop Task is created and activated to automate catalog task creation.

### Activity 2: Configure the Flow in Maintain Items

1. Open ServiceNow and navigate to **All**.
2. Search for **Maintain Items**.
3. Open Maintain Items.
4. Search for **Standard Laptop** in the Name field.
5. Open the Standard Laptop catalog item.
6. Navigate to the **Process Engine** section.
7. Remove the existing automations, if any.
8. Select **Flow** and add the previously created flow, **Standard Laptop Task**.
9. Save the record using the form menu.

**Result:** The Standard Laptop catalog item is configured to use the newly created flow.

### Activity 3: Test the Flow

1. Navigate to **All** and search for **Service Catalog**.
2. Open Service Catalog and select **Hardware**.
3. Find and select **Standard Laptop**.
4. Click **Order Now** to submit the request.
5. Open the order status and click the Request Number.
6. Scroll down to the **Approvers** section.
7. Right-click the approval record and select **Approve**.
8. Open the **Requested Items** section.
9. Open the corresponding Requested Item record.
10. Scroll down to the **Catalog Tasks** section.
11. Open the catalog task to verify the task details.

**Result:** The catalog task is created through the flow. The short description and assignment group can be checked in the generated task record.

## Expected Output

When a user submits a Standard Laptop request:

* A requested item is created.
* The flow is triggered by the Service Catalog request.
* A catalog task is automatically created.
* The short description is set to "Laptop need to Configured".
* The assignment group is set to Hardware.
* The approval field is configured as Approved.
* The generated catalog task can be viewed under the Catalog Tasks section.

## Conclusion

This project demonstrates the automation of a laptop request process using ServiceNow Flow Designer. By creating and configuring a flow, the catalog task creation process can be automated, reducing manual work and making the request process easier to manage.


