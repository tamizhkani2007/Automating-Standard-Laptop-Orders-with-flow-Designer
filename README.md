# Streamlining IT Procurement: Automating Standard Laptop Orders with Flow Designer

## Project Overview

This project automates the standard laptop procurement process using ServiceNow Flow Designer.

The main purpose of this project is to streamline the process of ordering standard laptops and automatically create a Catalog Task after the service request is approved. The task is assigned to the Hardware group for laptop configuration.

## Problem Statement

The current IT procurement process involves manual work and may cause delays while handling standard laptop orders.

Standard laptop requests require configuration, but this step can be overlooked or delayed. This can increase user waiting time and result in inefficient resource allocation within the IT department.

## User Story

As a member of the IT procurement team, I want a streamlined process for ordering standard laptops so that tasks are automatically generated and assigned to the Hardware team for configuration.

This ensures that laptops can be configured promptly after arrival, reducing user waiting time and manual intervention.

## Project Objective

The objective of this project is to implement an automated workflow using ServiceNow Flow Designer to facilitate the procurement and configuration of standard laptops.

### Objectives

- Create a seamless experience for users requesting standard laptops.
- Ensure timely laptop configuration.
- Reduce manual intervention.
- Reduce potential errors in the procurement process.
- Improve resource utilization within the IT department.
- Optimize task allocation.
- Improve overall efficiency and productivity.

## Technology Used

- ServiceNow
- Flow Designer
- Service Catalog
- Catalog Task
- Hardware Assignment Group

# Project Workflow

The overall workflow is:

Service Catalog
↓
Standard Laptop
↓
Order Now
↓
Service Request
↓
Approval
↓
Flow Designer
↓
Create Catalog Task
↓
Hardware Assignment
↓
Laptop Configuration

# Milestone 1: Create Flow

## Step 1: Open Flow Designer

1. Open ServiceNow.
2. Click on All.
3. Search for `Flow Designer`.
4. Click on Flow Designer under Process Automation.
5. Click on New.
6. Select Flow.

## Step 2: Configure Flow Properties

Enter the following details:

**Flow Name:**
`Standard laptop task`

**Application:**
`Global`

**Run User:**
`System user`

Click **Submit**.

## Step 3: Add Trigger

1. Click on **Add a trigger**.
2. Search for `Service Catalog`.
3. Select **Service Catalog**.
4. Click **Done**.

## Step 4: Add Action

1. Under Actions, click **Add an action**.
2. Search for `Create Catalog Task`.
3. Select **Create Catalog Task**.
4. Set the Requested Item Record in the Request item field.
5. The Table will be automatically populated as **Catalog Task**.

## Step 5: Configure Catalog Task

Set the following values:

**Short Description:**
`Laptop need to Configured`

**Description:**
`Laptop need to Configured`

**Assignment Group:**
`Hardware`

**Approval:**
`Approved`

Leave the remaining fields as default.

Click **Done**.

## Step 6: Save and Activate

1. Click **Save**.
2. Click **Activate**.
3. Click **Activate** again when prompted.

The Flow is now configured for the standard laptop request process.

# Milestone 2: Flow Assignment

## Assign Flow to Standard Laptop Service Catalog

1. Open ServiceNow.
2. Click on **All**.
3. Search for `Maintain Items`.
4. Select **Maintain Items**.
5. In the Name field, search for `Standard Laptop`.
6. Select the **Standard Laptop** record.
7. Open the **Process engine** section.
8. Remove the remaining automations.
9. Add the Flow.
10. Select the created Flow named:
   `Standard Laptop Task`
11. Save the record.

# Milestone 3: Service Catalog

## Place a Standard Laptop Order

1. Click on **All**.
2. Search for `Service Catalog`.
3. Open **Service Catalog**.
4. Click on **Hardware**.
5. Find **Standard Laptop**.
6. Click on **Standard Laptop**.
7. Click **Order Now** to place the request.

## Check Order Status

1. Open the Order Status.
2. Click on the **Request Number**.
3. The Requested Item record will open.
4. Scroll down to the **Approvers** section.
5. Approve the request.

## Verify Requested Item

1. Open the **Requested Item** section.
2. Open the Requested Item record.
3. Scroll down to the **Catalog Tasks** section.
4. Open the Catalog Task record.
5. Verify the updated status.
6. Verify the Short Description.
7. Verify the Assigned Group.

# Expected Result

After the service request is approved, the Flow Designer automation creates a Catalog Task.

The Catalog Task contains:

- Short Description: Laptop need to Configured
- Assignment Group: Hardware
- Approval: Approved

This allows the Hardware team to handle the laptop configuration task.

# Conclusion

By automating the standard laptop procurement process with ServiceNow Flow Designer, the project reduces manual overhead and improves the efficiency of IT procurement.

The automated workflow helps ensure timely laptop configuration, reduces user waiting time, optimizes resource allocation, and improves the overall user experience.

# Project Status

**Project:** Completed

**Platform:** ServiceNow

**Automation Tool:** Flow Designer

**Service Catalog Item:** Standard Laptop

**Assignment Group:** Hardware
