---
layout: post
title: Travelling-SalesMan Problem in Home Delivery Management System
date: 2019-08-17 09:56:00-0400
description: 
tags: project
categories: class-project
giscus_comments: false
related_posts: false
featured: false
---
# Travelling-SalesMan Problem in Home Delivery Management System

## Overview:

This project tries to solve the Travelling Salesman Problem, optimizing the route for a delivery boy to cover a list of provided addresses efficiently. The program calculates the shortest route using the Nearest Neighbour algorithm and displays information such as distance, cost, and estimated time.

## Files:

1. **ShortestPath.cs:**
   - Main form class containing the logic for the Travelling Salesman Problem application.
   - Handles user input for delivery addresses and integrates with the Nearest Neighbour algorithm.
   - Displays route details, including distance, cost, and estimated time.
   - Manages the delivery boy queue and updates the route dynamically.

2. **InsertBoy.cs:**
   - Form class for inserting new delivery boys into the system.
   - Allows users to add details of a new delivery boy, such as ID, name, and email.

3. **Email.cs:**
   - Class responsible for sending email notifications.
   - Utilizes the `SendEmail` method to send route details to the selected delivery boy.

4. **Settings.cs:**
   - Form class providing settings options for the application.
   - Users can configure parameters such as delivery speed and cost per kilometer.

## Functionality:

- **Insert Addresses:**
  - Users can input house and area details to add addresses for delivery.
  - The application displays the entered addresses for reference.

- **Find Route:**
  - When the user clicks the "Find Route" button, the application calculates the shortest route using the Nearest Neighbour algorithm.
  - Information about the route, including distance, cost, and estimated time, is displayed.

- **Insert Delivery Boy:**
  - Users can add new delivery boys by clicking the "Insert Delivery Boy" button.
  - The `InsertBoy` form allows users to provide details such as ID, name, and email for the new delivery boy.

- **Send Email:**
  - Clicking the "Send Email" button sends an email with the route details to the selected delivery boy.

- **Settings:**
  - Users can access application settings by clicking the "Settings" button.
  - The `Settings` form allows users to configure parameters such as delivery speed and cost per kilometer.

- **Start/Stop Timer:**
  - Users can start and stop the timer to measure the interval between route calculations.

## Usage:

1. **Insert Addresses:**
   - Enter house and area details and click the "Add Address" button.

2. **Find Route:**
   - Click the "Find Route" button to calculate the shortest route.

3. **Insert Delivery Boy:**
   - Click the "Insert Delivery Boy" button to add a new delivery boy.

4. **Send Email:**
   - Click the "Send Email" button to send route details to the selected delivery boy.

5. **Settings:**
   - Click the "Settings" button to configure application parameters.

6. **Start/Stop Timer:**
   - Use the "Start Timer" and "Stop Timer" buttons to control the timer interval.

## Notes:

- The application uses a dynamic queue (`DynamicQueue`) to manage delivery boys.
- The Nearest Neighbour algorithm is employed to find the shortest route.
- The program allows users to adjust settings such as delivery speed and cost per kilometer.

## Dependencies:

- The application relies on external classes such as `City`, `Route`, `NearestNeighbour`, `DeliveryBoy`, and `Email` for various functionalities.

## Additional Information:

- The application includes features such as sending email notifications, dynamic route calculation, and user-configurable settings.