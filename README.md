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

## API Security

## CI/CD Pipeline

