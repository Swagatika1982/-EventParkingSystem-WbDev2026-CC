# EventParkingSystem-WbDev2026-CC
ERD and SQL database design for a multi-zone event parking system with zones, levels, tickets, sessions, and payments.

 
https://app.eraser.io/workspace/KUCJo8e0p5x2XBhLqiG9?origin=share
 

# Multi-Zone Event Parking System ERD

This project contains the  Entity Relationship Diagram (ERD)  for a  Multi-Zone Event Parking System  designed for large convention venues such as  Comic-Con India.

The goal of this project is to design a clean and normalized database structure that can manage thousands of vehicles arriving across multiple event days.

This system supports:

- vehicle entry and exit tracking
- multiple parking zones and levels
- different vehicle types
- reserved parking categories
- parking tickets
- parking sessions
- payment records
- spot availability tracking

This project focuses on **database design and ER modeling only**.

# Real-Life Scenario

Imagine a large event venue hosting **Comic-Con India**.

Thousands of visitors arrive for:

- anime screenings
- cosplay competitions
- creator meetups
- gaming showcases
- merchandise shopping
- panel discussions

Visitors may arrive using:

- bikes
- cars
- SUVs
- cabs
- EV vehicles

Some parking areas are specially reserved for:

- cosplayers with props
- exhibitors
- creators
- VIP guests
- staff members
- EV charging vehicles

Whenever a vehicle enters:

- the system creates a **parking session**
- generates a **parking ticket**
- assigns a suitable parking spot
- records entry time

When the vehicle exits:

- exit time is stored
- parking fee is calculated
- payment is recorded
- the parking spot becomes available again


## Main Entities Used

This ERD includes the following main entities:

    ### Event
    Stores event details such as Comic-Con India and event duration.
    
    ### VehicleCategory
    Stores vehicle types like Bike, Car, SUV, Cab, and EV.

    ### AccessCategory
    Stores special access types such as VIP, Staff, Exhibitor, and Cosplayer.
    
    ### Vehicle
    Stores vehicle information like plate number and owner details.
    
    ### ParkingZone
                Represents different parking zones inside the venue.
            
            Example:
            - Zone A
            - Zone B
            - VIP Zone

    ### ParkingLevel
    Represents multiple levels or floors inside a zone.
    
            Example:
            - Level 1
            - Basement
            - Floor 2
    
    ### SpotCategory
    Defines the type of parking spot.
    
            Example:
            - Bike Spot
            - SUV Spot
            - EV Charging Spot
    
    ### ParkingSpot
    Represents the actual physical parking spot.
    
    ### SpotReservationCategory
    Used for reserved parking spots such as VIP or staff-only spots.
    
    ### ParkingSession
    Tracks entry and exit of each vehicle.
    
    This is one of the most important tables.
    
    ### ParkingTicket
    Stores the ticket generated during entry.
    
    ### Payment
    Stores payment information for each parking session.



##  Key Relationships

Some important relationships in this design:

- One event can have multiple parking zones
- One zone can have multiple levels
- One level can have multiple parking spots
- One vehicle can visit multiple times
- One parking spot can be reused over time
- One parking session belongs to one vehicle
- One session generates one ticket
- One session has payment details

## Tools Used

- **Eraser** for ER Diagram
- Database design concepts
- Normalization principles
- Primary and Foreign Key relationships


##  Learning Purpose

This project helped in understanding:

- ERD design
- primary keys and foreign keys
- one-to-many relationships
- normalization
- real-world database modeling
- system thinking

