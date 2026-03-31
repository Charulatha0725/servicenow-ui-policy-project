# Enforcing Mandatory Fields Using UI Policies and Migrating Changes with Update Sets

## Project Overview

This project demonstrates how to enforce mandatory fields using UI Policies and migrate the changes using Update Sets in ServiceNow. The goal is to ensure that certain fields become mandatory when specific conditions are met and to safely transfer these configurations between ServiceNow instances.

## Platform Used

* ServiceNow

## Objective

To enforce the **Priority field** as mandatory when the **State of an Incident is changed to "In Progress"** using UI Policies and to capture these changes using Update Sets.

## Steps Performed

### 1. Create an Update Set

* Navigate to **System Update Sets → Local Update Sets**
* Create a new Update Set
* Make the Update Set **Current**

### 2. Create a UI Policy

* Navigate to **System UI → UI Policies**
* Create a new UI Policy for the **Incident table**
* Set the condition:

  * **State is In Progress**

### 3. Create UI Policy Action

* Add a UI Policy Action for the **Priority field**
* Set **Mandatory = True**

### 4. Test the UI Policy

* Navigate to **Incident → Create New**
* Change the **State to In Progress**
* The **Priority field becomes mandatory**

### 5. Capture Changes in Update Set

* Verify that the UI Policy and UI Policy Action are captured in the Update Set

### 6. Export and Import Update Set

* Export the Update Set as **XML**
* Import it into another ServiceNow instance using **Retrieved Update Sets**

## Result

When the Incident State is changed to **In Progress**, the **Priority field becomes mandatory**, ensuring that users provide necessary information before proceeding.

## Screenshots

Screenshots of the implementation are available in the repository
