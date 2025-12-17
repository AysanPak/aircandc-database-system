 # AirC&C Database System

  A relational database system for a short-term property rental platform, similar to Airbnb. Built as a term project for Database Management course at Istanbul Technical University.

  ## Project Overview

  AirC&C manages the complete lifecycle of property rentals: user registration, property listings, bookings, messaging between hosts and guests, and review management. The system includes analytical views for business intelligence and data validation.

  ## Database Schema

  ### Entities (8 Tables)

  | Entity | Description |
  |--------|-------------|
  | **User** | Platform users (hosts and guests) with profile and authentication data |
  | **Property** | Rental listings with pricing, amenities, and property type |
  | **Booking** | Reservations linking guests to properties with status tracking |
  | **Review** | Guest feedback and ratings for properties |
  | **Message** | Communication between hosts and guests |
  | **Location** | Geographic address data for properties |
  | **Country** | Country reference for location hierarchy |
  | **PropertyPictures** | Images associated with property listings |

  ## SQL Views (9 Analytical Views)

  ### Data Validation
  | View | Purpose |
  |------|---------|
  | `InvalidBillingData` | Detects pricing inconsistencies between booking cost and calculated price |
  | `InvalidDateTimeData` | Identifies logical date errors (check-in before listing date, etc.) |
  | `BookingOverlapCheck` | Finds double-bookings and guest scheduling conflicts |
  | `ReviewIntegrityCheck` | Flags suspicious reviews (no booking, canceled booking, timing issues) |

  ### Business Analytics
  | View | Purpose |
  |------|---------|
  | `PropertyPerformance` | Revenue, occupancy rate, and property categorization (Premium/Standard/Economy) |
  | `UserSpending_FrequencyAnalysis` | Customer segmentation with Recency-Frequency-Monetary labels |
  | `HostEarningsAnalysis` | Host performance metrics and activity status |
  | `BookingTimeAnalysis` | Monthly booking trends and revenue patterns |
  | `PopularPropertyTypes` | Property type performance by bookings, revenue, and ratings |

  ## Entity-Relationship Diagram

  The database follows a normalized relational design with:
  - Foreign key constraints for referential integrity
  - Indexed fields for query optimization
  - ENUM types for status fields (BookingStatus, AccountType, EditorApproval)

  ## Team

  This project was developed as a 3-person team collaboration for academic purposes.
  
  ## Course

  Database Management and Big Data - Istanbul Technical University
