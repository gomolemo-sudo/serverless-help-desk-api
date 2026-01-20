# Serverless Help Desk API

This repository contains a Serverless Help Desk API built using AWS services. The project demonstrates how a simple, real-world ticketing system can be designed using a fully serverless architecture. It focuses on clean system design, practical AWS usage, and clear documentation.

The API allows users to create support tickets and retrieve existing tickets through HTTP endpoints exposed via Amazon API Gateway.

## Architecture

The system follows a serverless request flow where the client interacts with API Gateway, which triggers AWS Lambda functions. These functions handle business logic and store ticket data in DynamoDB. Amazon CloudWatch is used for logging and monitoring.

Request Flow:

User → API Gateway → AWS Lambda → DynamoDB → CloudWatch

An architecture diagram is included in this repository to visually represent the system design.

## AWS Services Used

This project uses the following AWS services:

Amazon API Gateway for exposing REST API endpoints  
AWS Lambda for serverless compute and business logic  
Amazon DynamoDB for storing help desk tickets  
AWS Identity and Access Management (IAM) for secure permissions  
Amazon CloudWatch for logs and monitoring  

## Functionality

The Serverless Help Desk API provides the following features:

Users can create a new help desk ticket by sending a POST request with a title and description.  
Users can retrieve an existing ticket using a unique ticket ID.  
The backend is fully serverless and runs on a pay-per-use model.  
All interactions use JSON-based requests and responses.

## API Endpoints

To create a new ticket, a POST request is sent to the `/tickets` endpoint. The request body must include a title and description.

Example request body:

```json
{
  "title": "Cannot access email",
  "description": "Outlook fails to open on startup"
}

[Serverless_Help_Desk_Architecture.pdf](https://github.com/user-attachments/files/24733711/Serverless_Help_Desk_Architecture.pdf)
