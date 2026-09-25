# Car Rental Request Automation in ServiceNow

## Project Overview

The **Car Rental Request Automation** project is a ServiceNow-based application designed to automate the process of submitting, approving, and processing car rental requests.

The solution uses a ServiceNow Catalog Item to collect car rental information and Flow Designer to automate the approval and fulfillment process.

## Problem Statement

Manual processing of car rental requests can involve multiple steps such as collecting request details, obtaining approval, assigning tasks, and notifying users.

This project automates these activities using ServiceNow so that requests can move through a predefined workflow with less manual intervention.

## Objectives

- Create a structured Car Rental Request form.
- Collect all required rental information from the requester.
- Automate the approval process.
- Create a fulfillment task after approval.
- Send an email notification after the required workflow step.
- Maintain the request process inside ServiceNow.

## Technologies Used

- ServiceNow
- Service Catalog
- Catalog Items
- Catalog Variables
- Workflow Studio
- Flow Designer
- Approval Management
- Catalog Tasks
- Email Notifications
- Update Sets

## Car Rental Request Form

The Catalog Item created for the project is:

**Car Rental Request**

The form contains the following variables:

| Variable | Type |
|---|---|
| Requested Date | Date |
| Pickup Location | Single Line Text |
| Drop Location | Single Line Text |
| Duration | Numeric Scale |
| Car Type | Select Box |
| Reason | Multi Line Text |

## Automation Flow

The project uses a Flow named:

**Car Rental Req**

The automation follows this process:

```text
User submits Car Rental Request
              ↓
     Service Catalog Trigger
              ↓
      Ask For Approval
              ↓
       Approval Decision
              ↓
        If Approved
              ↓
     Create Catalog Task
              ↓
         Send Email
