# OnlyVibes 🎶✨

## 📜 Project Overview

**OnlyVibes** is a web-based application designed to enhance event discovery and participation through personalized experiences. Developed as part of a university course on Software Engineering, the project was structured across three development phases, adhering to the methodology and deliverables required by the syllabus.

OnlyVibes enables users to browse, review, follow, and interact with venues and events, while also empowering verified users and venues to create and manage their own event listings. The system emphasizes user engagement, seamless UI/UX, and role-based access control.

## 🗂️ Structure of the Deliverables

The project is divided into three major assignments:

---

### ✅ Assignment 1: Requirements & User Experience

This phase focuses on gathering and documenting the system requirements.

- **Functional Requirements**  
  We specified 20+ concrete functional requirements across five actor categories: Admin, System, User, Registered User, Verified User, and Venue.  
  Each requirement clearly defines what the system must allow its actors to perform (e.g., "The registered user must be able to like an event").

- **Non-Functional Requirements**  
  These include constraints such as system reliability, security, performance expectations, and user privacy.

- **User Stories & Features**  
  Twelve feature-based stories were developed, each with **happy** and **unhappy paths**, including contextual scenarios for actions such as viewing event details, requesting verification, liking events, and receiving personalized recommendations.

- **Mockups**  
  Graphical mockups represent the UI flow for major features and user interactions.

- **Diagrams**  
  - Use Case Diagram: Illustrates all user roles and their accessible actions.  
  - Activity Diagrams: Depict process flows for complex tasks like verification requests and reviewing events.

---

### 🧩 Assignment 2: System Design

This phase transitions from what the system does to how it is built.

- **Class Diagram**  
  A UML class diagram models the application's key entities, including inheritance (e.g., `User → RegisteredUser → VerifiedUser`) and associations (e.g., `Venue` creates many `Events`).

- **Design Patterns**  
  We applied:  
  - **Proxy**: For database access and role-based verification control  
  - **Singleton**: For managing centralized system state  
  - **Observer**: For push notifications and reminders  

- **Sequence Diagrams**  
  We provide detailed sequence diagrams for:  
  - Viewing an event  
  - Liking and unliking events  
  - Requesting and processing verification  
  - Receiving event reminders and notifications  

---

### 🔧 Assignment 3: REST API Documentation (OpenAPI)

The final phase involved formalizing the backend interface.

- **OpenAPI Specification**  
  All REST endpoints are fully described in `openapi.json`, covering:  
  - CRUD operations for events, users, venues  
  - Role-specific actions like verification handling and recommendations  
  - Custom endpoints such as `/events/{eventId}/like`, `/user/{userId}/notifications`

- **Error Schema**  
  A consistent error response model is implemented across endpoints:
  ```json
  {
    "code": 400,
    "message": "Invalid request parameters"
  }
  ```
- **Security & Roles**  
  Each endpoint specifies expected user roles (e.g., only verified users can create events), and appropriate error responses (401 Unauthorized, 403 Forbidden, etc.).

- **Resource Modeling**  
Includes structured data models for User, Event, Venue, Notification, and Recommendation.

## 🌟 Why OnlyVibes?

OnlyVibes is not a generic event app—it is designed around meaningful social interactions, trust, and personalization. The application supports verified user accounts, venue pages, recommendations based on preferences, and a notification system that keeps users informed. This combination creates a richer experience compared to traditional event listings.

The system design balances flexibility and structure: verified users and venues can create and manage content, while regular users benefit from discovery, filtering, and social features like following and liking. Each of these components is linked to concrete user needs and course-defined functional requirements.

---

## 🚀 How to Explore the Project

To navigate this repository:

1. Open the `UserStories.pdf` to see the full set of feature-driven user stories.
2. Explore `FunctionalRequirements.pdf` to understand the expected capabilities by role.
3. Examine the class diagram and sequence diagrams for architectural understanding.
4. Review the OpenAPI spec (`OnlyVibes_API.json`) for full REST endpoint documentation.
5. Connect endpoints to user stories and functional requirements—everything is traceable.

---

## 🧠 Final Notes

The OnlyVibes project follows a complete methodology across all three assignments:

- **Assignment 1**: Requirement analysis, user stories, mockups, use case and activity diagrams.
- **Assignment 2**: Class design, pattern selection, sequence modeling.
- **Assignment 3**: RESTful API design with full OpenAPI documentation and error schema.     

Every feature is documented and justified. The diagrams match the code, and the REST structure respects best practices, including role-based control and consistent response modeling.


The system is modular, RESTful, and extensible, with every endpoint traceable back to a specific feature or requirement. The architecture is clear, the documentation is rigorous, and the platform is ready for future iterations.

---


