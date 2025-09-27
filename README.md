```mermaid
graph TD
    A[New User Arrives on Platform] --> B{Choose Path: Viewer or Coordinator?};

    B --> C[Viewer Path];
    B --> D[School Coordinator Path];
    
    C --> C1[Browse Public Content];
    C --> C2[Register as Viewer (Optional)];
    C2 --> C3[Login as Viewer];
    C3 --> C4[Access Personalized Content: Favorite Matches, etc.];

    D --> D1[Submit "Become a School Coordinator" Application Form];
    D1 --> DB1(Application Stored in DB);
    DB1 --> E[Admin/Volunteer Review Application];
    E --> F{Application Verified Offline?};
    F -->|No| G[Contact Applicant for More Info];
    G --> E;
    F -->|Yes| H{Admin/Sport Coordinator Approval?};
    H -->|No| I[Application Rejected: Notify Applicant];
    H -->|Yes| J[Account Created: User Assigned "School Coordinator" Role];
    J --> K[Credentials Sent to New School Coordinator];
    K --> L[School Coordinator Logs In];

    L --> N{Additional Roles Assignment};
    N --> N1[Admin Assigns "Volunteer" Role];
    N1 --> N2[Volunteer Logs In];
    N --> N3[Admin Assigns "Sport Coordinator" Role];
    N3 --> N4[Sport Coordinator Logs In];
```
