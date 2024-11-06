# Club Management App

## Table of Contents
1. [Introduction](#introduction)
2. [Features](#features)
3. [Technologies Used](#technologies-used)
4. [Getting Started](#getting-started)
   - [Prerequisites](#prerequisites)
   - [Installation](#installation)
5. [Application Overview](#application-overview)
   - [Login and Authentication](#login-and-authentication)
   - [Dashboard](#dashboard)
   - [Events Management](#events-management)
     - [In-Person Events](#in-person-events)
     - [Virtual Events](#virtual-events)
   - [Clubs Directory](#clubs-directory)
   - [Profile Management](#profile-management)
     - [User Profile](#user-profile)
     - [Membership Management](#membership-management)
   - [Referral Rewards System](#referral-rewards-system)
6. [Data Models](#data-models)
7. [API Endpoints](#api-endpoints)
   - [User Endpoints](#user-endpoints)
   - [Club Endpoints](#club-endpoints)
   - [Event Endpoints](#event-endpoints)
   - [Referral Rewards Endpoints](#referral-rewards-endpoints)
8. [Development and Contribution](#development-and-contribution)
   - [Project Structure](#project-structure)
   - [Contributing Guidelines](#contributing-guidelines)
9. [Future Enhancements](#future-enhancements)
10. [License](#license)

## Introduction
The Club Management App is a comprehensive web-based platform designed to streamline the management of student clubs, events, and memberships within an educational institution or organization. This system aims to improve visibility, participation, and communication across campus activities, providing an intuitive and responsive user interface for both students and club coordinators.

The application offers a simplified, user-friendly experience with a focus on responsive design, allowing users to access and interact with the platform seamlessly on both desktop and mobile devices. The platform provides a centralized hub for managing club-related activities, events, memberships, and referral rewards, enhancing the overall student experience and fostering a more vibrant and engaged campus community.

## Features
The Club Management App offers the following key features:

1. *Dashboard*: Provides an overview of recent activities, upcoming events, and personalized information for the user.
2. *Events Management*: Allows users to create, view, and manage both in-person and virtual events organized by various clubs.
3. *Clubs Directory*: Enables users to browse and search for clubs within the organization, view detailed club information, and manage their club memberships.
4. *Profile Management*: Allows users to view and edit their personal profile information, as well as manage their club memberships and positions.
5. *Referral Rewards System*: Tracks and manages referral bonuses and rewards for users who encourage their peers to join the platform and engage with campus activities.
6. *Responsive Design*: Ensures a seamless and consistent user experience across desktop and mobile devices, allowing users to access and interact with the application from anywhere.

## Technologies Used
The Club Management App is built using the following technologies:

- *Frontend*: React, Next.js, TypeScript, Tailwind CSS, Shadcn/UI components, Lucide React icons
- *Backend*: Node.js, Express
- *Database*: MongoDB

These technologies were chosen to provide a modern, scalable, and efficient platform that delivers a high-quality user experience while maintaining robust functionality and extensibility.

## Getting Started

### Prerequisites
Before you can set up the Club Management App, ensure that you have the following installed on your system:

- Node.js (v14 or later)
- npm or yarn

### Installation
Follow these steps to set up the Club Management App on your local machine:

1. Clone the repository:
bash
git clone https://github.com/your-username/club-management-app.git

2. Navigate to the project directory:
bash
cd club-management-app

3. Install dependencies:
bash
npm install
# or
yarn install

4. Set up environment variables: Create a .env.local file in the root directory and add the necessary environment variables (e.g., database URI, API keys).
5. Run the development server:
bash
npm run dev
# or
yarn dev

6. Open http://localhost:3000 in your browser to see the application.

## Application Overview

### Login and Authentication
The Club Management App provides a secure login system for both students and club coordinators. Users can securely authenticate themselves using their credentials, ensuring that sensitive information and functionalities are accessible only to authorized individuals.

Upon successful login, users are directed to the main dashboard, where they can access the various features of the application.

### Dashboard
The Dashboard serves as the central hub of the Club Management App, providing users with an overview of their recent activities, upcoming events, and personalized information.

The Dashboard features:
- Notification window for real-time event reminders
- Summary of upcoming events, including event details and attendance information
- Personalized recommendations and highlights based on the user's club memberships and interests

### Events Management
The Events Management feature of the Club Management App allows users to create, view, and manage both in-person and virtual events organized by various clubs on campus.

#### In-Person Events
For in-person events, users can:
- Browse a calendar view of upcoming events
- View detailed event information, including date, time, location, and event description
- RSVP and manage their attendance for events
- Coordinators can create new in-person events and manage existing ones

#### Virtual Events
The platform also supports virtual events, enabling club officers and members to:
- Host online meetings and discussions using Google Meet integration
- Live-stream club events, guest speaker sessions, or workshops using Google Meet
- Participate in virtual club activities and events from the comfort of their own devices

### Clubs Directory
The Clubs Directory provides users with a comprehensive overview of all the clubs available within the organization. Users can:
- Browse and search for clubs, filtering by categories (e.g., Sci-Tech, Cultural)
- View detailed club information, such as club description, active members, club president, and core members
- Manage their club memberships, including joining or leaving clubs

### Profile Management
The Profile Management feature allows users to view and edit their personal information, as well as manage their club memberships and positions.

#### User Profile
The user profile section includes:
- Overview of general user details, such as name, email, and avatar
- Ability to update personal information and preferences

#### Membership Management
In the Membership section, users can:
- View all the clubs they are currently active in
- See their position or role within each club (e.g., member, officer, coordinator)
- Club coordinators can also view and modify the profiles of club members

### Referral Rewards System
The Referral Rewards System tracks and manages referral bonuses and rewards for users who encourage their peers to join the platform and engage with campus activities.

Users can:
- View their current referral bonus and earning rate
- Track the progress of their referrals and the rewards they have earned
- Club coordinators can also monitor and update the referral rewards for individual users

## Data Models
The Club Management App utilizes the following data models to represent the core entities within the application:

1. *User*
   - id: Unique identifier for the user
   - name: Full name of the user
   - email: Email address of the user
   - role: User's role (e.g., student, coordinator)
   - avatar: URL of the user's profile picture
   - memberships: List of the user's club memberships

2. *Club*
   - id: Unique identifier for the club
   - name: Name of the club
   - description: Description of the club
   - members: Number of active club members
   - image: URL of the club's profile image
   - events: List of events organized by the club

3. *Event*
   - id: Unique identifier for the event
   - name: Name of the event
   - description: Description of the event
   - date: Date of the event
   - time: Time of the event
   - location: Location of the in-person event
   - clubId: Identifier of the club organizing the event

4. *Membership*
   - id: Unique identifier for the membership
   - userId: Identifier of the user
   - clubId: Identifier of the club
   - role: User's role within the club (e.g., member, officer, coordinator)

5. *ReferralReward*
   - id: Unique identifier for the referral reward
   - userId: Identifier of the user who received the referral reward
   - bonus: Amount of the referral bonus
   - earningRate: Rate at which the user earns referral rewards
   - startDate: Date when the referral reward program started
   - endDate: Date when the referral reward program ends

## API Endpoints
The Club Management App interacts with a backend API to manage the various functionalities of the application. The following are the main API endpoints:

### User Endpoints
- GET /api/users/:id: Fetch user details by ID
- PUT /api/users/:id: Update user profile information
- GET /api/users/:id/memberships: Fetch all memberships for a user

### Club Endpoints
- GET /api/clubs: Retrieve a list of all clubs
- GET /api/clubs/:id: Fetch details of a specific club
- POST /api/clubs: Create a new club (admin access)

### Event Endpoints
- GET /api/events: Fetch a list of all events
- GET /api/events/:id: Retrieve details of a specific event
- POST /api/events: Create a new event
- DELETE /api/events/:id: Delete an event (admin access)

### Referral Rewards Endpoints
- GET /api/referral-rewards/:userId: Fetch referral rewards details for a user
- PUT /api/referral-rewards/:userId: Update referral reward information for a user

## Development and Contribution

### Project Structure
The Club Management App follows a modular and scalable project structure, making it easier for developers to navigate, maintain, and extend the codebase. The main directories and files are organized as follows:


club-management-app/
├── components/
├── pages/
├── services/
├── utils/
├── styles/
├── models/
├── controllers/
├── routes/
├── next.config.js
├── package.json
├── tsconfig.json
└── README.md


### Contributing Guidelines
We welcome contributions to the Club Management App! To contribute, please follow these steps:

1. Fork the repository.
2. Create a new branch: git checkout -b feature-branch-name.
3. Make your changes and commit them: git commit -m 'Add some feature'.
4. Push to the branch: git push origin feature-branch-name.
5. Submit a pull request.

Before submitting a pull request, please ensure that your code adheres to the project's coding standards and that you have tested your changes thoroughly.

## Future Enhancements
The Club Management App is designed with extensibility in mind, and we have plans to introduce several future enhancements to improve the overall functionality and user experience. Some of the planned improvements include:

1. *Integration with Campus Calendar*: Seamlessly integrate the app's event management system with the campus-wide calendar, allowing for better visibility and coordination of club activities.
2. *Mobile App Development*: Develop a dedicated mobile application for the Club Management App, providing users with a native and optimized experience on their smartphones and tablets.
3. *Notification System Improvements*: Enhance the notification system to include features like push notifications, email alerts, and in-app notifications to keep users informed about important updates and events.
4. *Data Analytics and Reporting*: Introduce advanced data analytics and reporting capabilities to help club coordinators and administrators gain deeper insights into club activity, membership trends, and event performance.
5. *Gamification and Engagement Features*: Implement gamification elements, such as achievements, leaderboards, and rewards, to promote user engagement and foster a more vibrant campus community.

## License
The Club Management App is licensed under the [MIT License](LICENSE.md).
