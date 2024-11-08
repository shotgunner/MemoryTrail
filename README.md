# MemoryTrail

MemoryTrail is a web application that allows travelers to capture, share, and relive their travel memories.

## Introduction

This project consists of two main parts:

1. **Design the Architecture**: Based on provided specifications, design the system architecture, including necessary diagrams and explanations of design choices.

2. **Implement REST API Endpoints**: Develop a set of RESTful API endpoints that interact with a PostgreSQL database to support the feature.

## Feature Description: Travel Memories Sharing Platform

We aim to introduce a new feature that allows users to share specific travel memories (photos, notes, locations) with friends and family, even if they are not registered on the app. This feature enhances user engagement and allows for broader sharing of travel experiences.

## Task Details

### Part 1: Design the Architecture

#### Objective
Design the backend architecture for the "Travel Memories Sharing Platform" feature.

#### Requirements
- **Scalability**: The system should handle a high volume of users and data
- **Performance**: Optimized for quick data retrieval and minimal latency
- **Security**: Secure endpoints, especially when sharing content with non-registered users
- **Maintainability**: Clean separation of concerns and modular design

#### Deliverables
1. **System Architecture Diagram**
   - Visual representation of system components and their interactions
   - Tools: Lucidchart, draw.io, or Google Drawings

2. **Database Schema Diagram**
   - ER diagram showing tables, fields, and relationships

3. **Design Explanation Document** (max 2 pages)
   - Overview: Brief description of architecture
   - Justification: Reasons behind design decisions
   - Considerations: How scalability, performance, security, and maintainability are addressed

#### Key Considerations
- User authentication and authorization management
- Secure content sharing with non-registered users
- Data models for users, memories, and shared links
- Access control implementation

### Part 2: Implement REST API Endpoints

#### Objective
Develop RESTful API endpoints using Python (preferably with FastAPI).

#### Requirements

1. **User Authentication**
   - Token-based authentication
   - Secure endpoint access

2. **API Endpoints**
   - Memory Management:
     ```
     POST /memories/              # Create new memory
     GET /memories/{memory_id}/   # Retrieve specific memory
     PUT /memories/{memory_id}/   # Update memory
     DELETE /memories/{memory_id}/ # Delete memory
     ```
   - Sharing Memories:
     ```
     POST /memories/{memory_id}/share/ # Generate shareable link
     GET /shared/{share_token}/        # Access shared memory
     ```
   - User Registration & Authentication:
     ```
     POST /users/register/  # Register new user
     POST /users/login/     # Authenticate and get token
     ```

3. **Database Interaction**
   - PostgreSQL implementation
   - Mock data population for testing

4. **Security Features**
   - Owner-only memory management
   - Limited access shared links (expiration time, one-time view)

#### Deliverables

1. **Source Code**
   - Organized Python codebase
   - Virtual environment and requirements.txt

2. **README File**
   - Environment setup instructions
   - Application and testing instructions
   - Development assumptions and decisions

3. **Tests**
   - Unit tests for critical components
   - Testing instructions

#### Technical Considerations
- Query optimization and indexing
- Comprehensive error handling
- API documentation (Swagger or similar)

## General Guidelines

### Time Allocation
- Up to 7 hours for completion

### Communication
- Questions and clarifications via provided Slack channels

### Tools
- Diagram creation tools of choice
- Preferred libraries and frameworks
- Git version control with regular commits

### Submission
- Git repository link (GitHub/GitLab)
- Complete, organized deliverables

## Evaluation Criteria

### Architecture Design (25%)
- Diagram clarity and completeness
- Design decision soundness
- System requirements consideration

### Code Quality (25%)
- Code readability and organization
- Python best practices
- Documentation quality

### Functionality (20%)
- Endpoint implementation
- Database integration
- Authentication/authorization

### Testing (15%)
- Unit test coverage
- Edge case handling

### Performance (10%)
- Query efficiency
- Caching implementation

### Error Handling (5%)
- User-friendly error messages
- Input validation

## Additional Information

- Create sample data as needed
- Document assumptions in README
- Creative problem-solving encouraged
