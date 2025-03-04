# SkillXSync
 
SkillXSync is a **full-stack web application** for managing workshop bookings and one-on-one meetings. The backend is built with **Spring Boot**, and the frontend is built with **React** and **Tailwind CSS**. It uses **Spring Security** for authentication, **PostgreSQL** for data storage, and the **Google Calendar API** for scheduling. The application ensures all bookings occur on weekdays (Monday to Friday) between 07:00 and 17:00.
 
---
 

## **Features**
 

### **1\. Authentication**
 

*   Secure user access using **Spring Security**.
     
*   Users can register and log in with their email and password.
     
*   User roles include **Mentor** and **Peer**.
     

### **2\. Booking System**
 

*   **Mentor Sessions**:
     
    *   Fetch and display a list of available mentors.
         
    *   Request a meeting with a selected mentor.
         
*   **Peer Sessions**:
     
    *   Search for peers by availability or expertise.
         
    *   Schedule one-on-one meetings with peers.
         

### **3\. Google Calendar Integration**
 

*   Create calendar events for confirmed bookings.
     
*   Send invites to all participants automatically.
     
*   Enforce meeting times strictly on weekdays between 07:00 and 17:00.
     

### **4\. Frontend Functionality**
 

*   **Login/Signup**: Authenticate the user.
     
*   **Dashboard**: Display upcoming workshops and available mentors.
     
*   **Request Meeting**: Request a mentor or peer session.
     
*   **View Bookings**: Display a list of all confirmed bookings.
     
*   **Cancel Booking**: Allow users to cancel an existing booking.
     

---
 

## **Technologies Used**
 

### **Backend**
 

*   **Spring Boot**: REST API development.
     
*   **Spring Security**: Authentication and authorization.
     
*   **Spring Data JPA**: Database interaction with PostgreSQL.
     
*   **Google Calendar API**: Scheduling meetings.
     
*   **PostgreSQL**: Database for storing users, meetings, and workshop requests.
     

### **Frontend**
 

*   **React**: Frontend framework.
     
*   **Tailwind CSS**: Styling.
     
*   **Axios**: API calls to the backend.
     
*   **React Router**: Navigation.
     

---
 

## **Setup Instructions**
 

### **1\. Prerequisites**
 

*   **Java 17+**: For Spring Boot backend.
     
*   **Node.js**: For React frontend.
     
*   **PostgreSQL**: Database.
     
*   **Google Cloud Account**: For Google Calendar API.
     

### **2\. Backend Setup**
 

1.  Clone the repository:
     
    
        git clone https://github.com/your-repo/skillxsync.git
        cd skillxsync/backend
        
    
2.  Set up PostgreSQL:
     
    *   Create a database named `skillxsync`.
         
    *   Update the `application.properties` file with your database credentials:
         
        
            spring.datasource.url=jdbc:postgresql://localhost:5432/skillxsync
            spring.datasource.username=your-username
            spring.datasource.password=your-password
            spring.jpa.hibernate.ddl-auto=update
            
        
3.  Run the Spring Boot application:
     
    
        ./mvnw spring-boot:run
        
    

### **3\. Frontend Setup**
 

1.  Navigate to the frontend directory:
     
    
        cd ../frontend
        
    
2.  Install dependencies:
     
    
        npm install
        
    
3.  Start the development server:
     
    
        npm start
        
    
4.  Open the application in your browser:
     
    
        http://localhost:3000
        
    

### **4\. Google Calendar API Setup**
 

1.  Create a project in the [Google Cloud Console](https://console.cloud.google.com/) .
     
2.  Enable the **Google Calendar API**.
     
3.  Generate API credentials and download the `credentials.json` file.
     
4.  Place the `credentials.json` file in the `backend/src/main/resources` directory.
     

---
 

## **API Endpoints**
 

### **Authentication**
 

*   `POST /api/auth/signup`: Register a new user.
     
*   `POST /api/auth/login`: Authenticate user.
     

### **Meetings**
 

*   `GET /api/mentors`: Fetch list of mentors.
     
*   `POST /api/meetings`: Schedule a meeting.
     
*   `GET /api/bookings`: Fetch user's bookings.
     
*   `DELETE /api/bookings/{id}`: Cancel a booking.
     

---
 

## **Stretch Features**
 

1.  **Notifications**:
     
    *   Send email notifications for meeting confirmations and reminders.
         
2.  **Feedback System**:
     
    *   Allow users to rate and leave feedback for mentors and peers.
         
3.  **Search Filters**:
     
    *   Enable filtering mentors/peers by expertise or availability.
         

---
 

## **Deployment**
 

### **Backend**
 
Deploy the Spring Boot application to a cloud platform like **AWS**, **Heroku**, or **Google Cloud**.
 

### **Frontend**
 
Deploy the React application to a static hosting service like **Netlify** or **Vercel**.
