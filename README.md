# Stripe Payment Gateway Integration Application

This Spring Boot application demonstrates integration with the Stripe Payment Gateway to handle Payment Intents and Refunds.

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Configuration](#configuration)
  - [Running the Application](#running-the-application)
- [API Endpoints](#api-endpoints)
- [Reference](#reference)


## Introduction

This application integrates with the Stripe Payment Gateway API to perform various operations such as creating Payment Intents, confirming/capturing Payment Intents, creating refunds, and listing Payment Intents.

## Features

- Create a new Payment Intent with customizable parameters.
- Confirm a Payment Intent using a payment method and return URL.
- Capture a Payment Intent that requires manual capture.
- Create refunds for Payment Intents.
- Retrieve a list of Payment Intents.

## Technologies Used

- Java
- Spring Boot
- Stripe API
- Maven


## Getting Started

Follow these instructions to get the project up and running on your local machine.

### Prerequisites

- Java Development Kit (JDK) 17
- Maven
- Stripe API key (test mode) 

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/Kapil7982/PortOne.git
   cd Stripe
   ```

## Configuration
Set your Stripe API key in StripeConfig.java.

## Running the Application
The application will start on port 8080 by default.

## API Endpoints

### Create Payment Intent

- **POST** `/api/v1/create_intent`
- **Headers** `Content-Type : application/json`

  Creates a new Payment Intent with default parameters.
  
![createIntent](https://github.com/Kapil7982/PortOne/assets/103938868/60092a04-90ba-479b-b9a6-e438c53ea8df)
-

### Confirm Payment Intent

- **POST** `/api/v1/confirm_intent/{id}`
- **Headers** `Content-Type : application/json`

  Confirms a Payment Intent by ID.
  
![confirmIntent](https://github.com/Kapil7982/PortOne/assets/103938868/536ee640-43e9-4539-b825-a3266859d135)
-
### Capture Payment Intent

- **POST** `/api/v1/capture_intent/{id}`
- **Headers** `Content-Type : application/json`

  Captures a Payment Intent that requires manual capture.

![captureIntent](https://github.com/Kapil7982/PortOne/assets/103938868/dc1f045b-56e2-47f9-bf8b-0351d4586de2)
-
### Create Refund

- **POST** `/api/v1/create_refund/{id}`
- **Headers** `Content-Type : application/json`

  Creates a refund for a Payment Intent by ID.

![createRefund](https://github.com/Kapil7982/PortOne/assets/103938868/d20c65c0-d968-434b-9507-af02aa99cd33)
-
 
### Get Payment Intents

- **GET** `/api/v1/get_intents`
- **Headers** `Content-Type : application/json`

  Retrieves a list of Payment Intents.

![getAllIntent](https://github.com/Kapil7982/PortOne/assets/103938868/99e558fc-59f4-4f12-a7e1-1427e116a567)
-
## Reference

- Stripe API docs - https://stripe.com/docs/api/payment_intents 
- Payment Intents - https://stripe.com/docs/payments/payment-intents
- Stripe go-SDK - https://github.com/stripe/stripe-go
- Stripe Other Language SDKs - https://github.com/stripe
- Setup simple backend in Golang - https://github.com/gorilla/mux

