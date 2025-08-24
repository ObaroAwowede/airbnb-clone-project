# airbnb-clone-project.

## Project Description

This project is a full-stack clone of the popular accommodation booking platform AirBnB. The goal is to build a functional web application that allows users to browse property listings, view detailed property information, and complete bookings.


## Team Roles
<p>Backend Developer: Responsible for implementing API endpoints, database schemas, and business logic.</p>
<p>Database Administrator: Manages database design, indexing, and optimizations.</p>
<p>DevOps Engineer: Handles deployment, monitoring, and scaling of the backend services.</p>
<p>QA Engineer: Ensures the backend functionalities are thoroughly tested and meet quality standards.</p>

## Technology Stack
<p>Django: A high-level Python web framework used for building the RESTful API.</p>
<p>Django REST Framework: Provides tools for creating and managing RESTful APIs.</p>
<p>PostgreSQL: A powerful relational database used for data storage.</p>
<p>GraphQL: Allows for flexible and efficient querying of data.</p>
<p>Celery: For handling asynchronous tasks such as sending notifications or processing payments.</p>
<p>Redis: Used for caching and session management.</p>
<p>Docker: Containerization tool for consistent development and deployment environments.</p>

## Database Design
<h3>Users</h3>
<p>Fields:</p> <p>Username, email, password, id, first_name, last_name</p>
<h3>Properties</h3>
<p>Fields:</p> <p>Property_name, Listing_price, Owner (This is a foreign key to users, therefore multiple properties can be attributed to one owner)</p>
<h3>Bookings </h3>
<p>Fields:</p> <p>Date, User (This is a one to one relationship)</p>
<h3>Reviews</h3>
<p>Fields:</p> <p>title, rating, description, published_date</p>
<h3>Payments</h3>
<p>Fields:</p> <p>amount, user (one to one relationship with a user), property (one to one relationship with a property), Booking (One to one relationship with a booking)</p>

## Feature Breakdown
###1.<p>User Management: Implement a secure system for user registration, authentication, and profile management.</p>
###2.<p>Property Management: Develop features for property listing creation, updates, and retrieval.</p>
###3.<p>Booking System: Create a booking mechanism for users to reserve properties and manage booking details.</p>
###4.<p>Payment Processing: Integrate a payment system to handle transactions and record payment details.</p>
###5.<p>Review System: Allow users to leave reviews and ratings for properties.</p>
###6.<p>Data Optimization: Ensure efficient data retrieval and storage through database optimizations.</p>

## API Security

### 1. Authentication
- **Implementation**: JSON Web Tokens (JWT) will be used for user authentication. Tokens are generated upon login and must be included in the headers of subsequent requests.
- **Why it matters**: Ensures that only verified users can access protected resources (e.g., booking a property, viewing personal reservations). This prevents impersonation and protects accounts.

### 2. Authorization
- **Implementation**: Role-based and resource-based authorization. For example, only a host can manage their own listings, and only the booking owner can cancel their reservation.
- **Why it matters**: Protects user data by ensuring users cannot access or modify data that doesn’t belong to them. Prevents unauthorized actions like tampering with someone else’s booking.

### 3. Rate Limiting
- **Implementation**: Throttling requests (e.g., max X requests per minute per IP) to mitigate brute-force attacks and abuse.
- **Why it matters**: Prevents denial-of-service (DoS) attacks, protects login endpoints from brute-force attempts, and ensures system stability for all users.

### 4. Data Validation & Sanitization
- **Implementation**: Strict validation for all incoming data (e.g., property descriptions, booking dates) and sanitization to avoid malicious input.
- **Why it matters**: Protects against common web vulnerabilities such as SQL Injection, XSS (Cross-Site Scripting), and malformed data that could break the system.

### 5. Secure Data Storage & Transmission
- **Implementation**: 
  - Passwords hashed with strong algorithms (e.g., bcrypt).
  - HTTPS enforced for encrypted communication.
- **Why it matters**: Prevents sensitive data (like login credentials or payment details) from being stolen during transmission or if the database is compromised.

### 6. Payment Security
- **Implementation**: Payments are processed via a trusted third-party provider (e.g., Stripe/PayPal) using secure APIs. No raw payment details are stored on our servers.
- **Why it matters**: Protects financial information and reduces liability by relying on established


## CI/CD Pipeline

