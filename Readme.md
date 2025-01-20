# TechStackMastery

Web application for demonstrating technology proficiency

## Description

TechStackMastery is a web application that demonstrates deep knowledge of modern web development technologies. Its main function is to provide an interactive platform for project management, including users, tasks, and real-time analytics.

## Technical Stack

### Frontend (Angular)

#### PWA (Progressive Web App)
- Offline access to core functionality
- Using Service Workers for resource caching
- Web App Manifest for mobile device adaptation

#### NgRx (State Management)
- Managing users, tasks, and settings state through NgRx Store
- Effects (NgRx Effects) for asynchronous backend interaction
- Using selectors for efficient data access

#### Performance Optimization
- ChangeDetectionStrategy OnPush
- ChangeDetectorRef detach() and detectChanges()

### Backend

#### Express.js
- JWT authentication and authorization
- CRUD operations with users (MongoDB)
- File management through AWS S3
- Redis caching

#### Nest.js
- Task management (PostgreSQL)
- WebSocket communication
- Analytics and statistics
- Redis caching

### AWS and Infrastructure

- AWS Lambda for background tasks
- MongoDB Atlas
- AWS RDS (PostgreSQL)
- Redis on AWS ElastiCache
- AWS S3 for static files
- AWS CloudWatch for monitoring

## Main Pages

### 1. Dashboard
- Categorized task list
- Filtering and sorting
- Push notifications
- Real-time updates

### 2. Tasks Page
- Task creation/editing
- Draft auto-save
- Duplicate checking

### 3. User Profile
- Personal data management
- Notification settings
- Activity history

### 4. Analytics
- Performance charts
- Report export
- Automatic distribution

## Authentication

### Login Methods
- Email/password
- OAuth (Google, GitHub)
- JWT tokens

### Security
- Frontend and backend validation
- CSRF protection
- Secure password storage

## Offline Mode
- Access to recent tasks
- Local change storage
- Automatic synchronization

## Conclusion

TechStackMastery demonstrates comprehensive use of modern web technologies to create a scalable, performant, and secure task management application.

## Functional Justification of Technology Choices

### Frontend (Angular)

PWA technology is justified by the need for:
- Offline task access
- Synchronization after connection restoration
- Push notifications for reminders

NgRx is justified by the need to:
- Manage user state, task lists, and their statuses through centralized Store
- Handle asynchronous backend requests with Effects
- Optimize data access with selectors

OnPush strategy is used for components where data changes infrequently, reducing change detection cycles and improving performance.

### Backend (Express.js & Nest.js)

- Redis caches frequently used data like task lists and user sessions
- MongoDB stores unstructured data like task change history and user activity logs
- PostgreSQL stores structured data like user information, projects, and task statuses

### AWS and Server Infrastructure

- AWS Lambda executes background tasks like report generation and notifications
- AWS S3 stores attached files like images or task-related documents
- AWS CloudWatch monitors performance and stores application logs

## Page Details

### 1. Dashboard
Features:
- Task list display with categorization (active, completed, overdue)
- Task filtering and sorting
- Color highlighting for urgent tasks
- Push notifications for important deadlines (PWA)

Technologies:
- NgRx Store for task list management
- NgRx Effects for asynchronous task retrieval
- OnPush Change Detection for performance
- Redis caching for quick task list retrieval

### 2. Task Creation/Editing Page
Features:
- New task creation with deadline, priority, and attachment options
- Automatic draft saving (PWA, offline mode)
- Automatic duplicate task checking

### 3. User Profile Page
Features:
- Personal information editing
- Notification and interface settings
- Activity history

### 4. Analytics Page
Features:
- Performance charts and diagrams
- PDF/Excel report export
- Automatic weekly email reports

### 5. Offline Mode (PWA)
Features:
- Access to recent tasks without internet
- Local change storage and automatic synchronization

## Authentication Details

### User Registration
- Email, name, and password input
- Frontend and backend validation
- Unique user ID generation
- PostgreSQL stores core user data
- MongoDB stores user activity logs
- Email confirmation via AWS SES

### Authentication
- Email/password verification
- JWT token generation
- Redis caches active sessions

### OAuth Login
- Google and GitHub integration
- Automatic registration for first-time social login

### Password Recovery
- Email-based password reset
- 10-minute valid reset links
- Redis temporary token storage

### Role Management
- Admin user management capabilities
- PostgreSQL role and permission storage
- NgRx UI permission management
