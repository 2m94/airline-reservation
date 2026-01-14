✈️ Airline Reservation System
Overview

The Airline Reservation System is a full-stack application designed to simulate a real-world airline booking platform. The system enables customers to search for flights, make and manage reservations, while allowing airlines to manage flight inventory and airports to display real-time arrival and departure information.

The project was built collaboratively by a small development team, following modular design principles with a focus on data persistence, access control, and user experience.

Key Features

Secure customer accounts with reservation management

Airline-managed flight inventory and capacity enforcement

Centralized flight search and booking engine

Public airport arrival and departure information displays

Persistent storage across application restarts

Role-based access control for customers, airline admins, and system admins

System Architecture

The application is composed of the following core components:

Customer Portal

Airline Management Interface

Search Engine

Airport Information Displays

Persistent Data Layer

Each component is logically separated to reflect real-world airline reservation workflows.

Core Domain Entities
Customers

Register and authenticate with password-protected accounts

Search available flights and fares

Make and cancel reservations

View all personal reservations in a read-only dashboard

Customer data is isolated and inaccessible to other users

Airlines

Maintain an airline-specific management interface

Airline administrators can:

Create new flights

Set fares and maximum passenger capacity

Cancel existing flights

Customers can:

View airline flight listings

Book and cancel reservations

Airline administrators have read-only access to all reservations made on their flights

Capacity enforcement

Each flight enforces a maximum capacity

Once capacity is reached, further reservations are blocked

Flight cancellation handling

When a flight is canceled, all affected customer reservations are automatically updated

Airports

Airports provide public, real-time information displays with no authentication required.

Arrivals Screen

Displays all arriving flights for a given airport

Shows flight status:

On Time

Cancelled

Automatically refreshes at regular intervals

Departures Screen

Displays all departing flights for a given airport

Shows real-time flight status

Automatically refreshes to reflect airline updates

There is no airport administrator role; all airport data is read-only and public.

Search Engine

The search engine acts as a centralized discovery and booking interface.

Search flights using relevant criteria (e.g., airline, fare, destination)

Sort results by:

Fare

Airline name

Clearly indicates when flights are fully booked

Allows customers to make reservations directly from search results

Search Engine Administration

Admins can view all reservations made through the search engine only

Airline and customer reservations made outside the search engine are not visible

Access is read-only and restricted to system administrators

User Interface Requirements

Multi-screen graphical user interface (GUI)

Separate views tailored to:

Customers

Airline administrators

System administrators

Public airport displays

Clear role-based access enforcement across all views

Data Persistence

All application data persists across restarts

Data storage implemented using:

Database-backed persistence or

Structured file-based storage

The persistence strategy is abstracted from the UI layer

Technology Stack

Backend: Java (architecture-neutral, extensible design)

Frontend: GUI-based multi-screen interface

Persistence: Database or file-based storage

Security: Authentication and authorization enforced per role

Engineering Focus

This project emphasizes:

Clean separation of concerns

Role-based access control

Data consistency and integrity

Real-world business rules (capacity limits, cancellations)

Collaborative development practices

Future Enhancements

Payment processing integration

Notification system for flight changes

REST API exposure for mobile clients

Audit logging and reporting

Scalable microservices architecture

Why This README Works for Hiring Managers
