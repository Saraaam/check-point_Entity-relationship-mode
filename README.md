# check-point_Entity-relationship-mode

Here's an Entity-Relationship (ER) model based on the given requirements:

**Entities and Attributes:**

1. **Gymnasium**  
   - Gym_ID (Primary Key)  
   - Name  
   - Address  
   - Phone Number  

2. **Member**  
   - Member_ID (Primary Key)  
   - Last Name  
   - First Name  
   - Address  
   - Date of Birth  
   - Gender  
   - Gym_ID (Foreign Key → Gymnasium)  

3. **Coach**  
   - Coach_ID (Primary Key)  
   - Last Name  
   - First Name  
   - Age  
   - Specialty  

4. **Session**  
   - Session_ID (Primary Key)  
   - Sport Type  
   - Schedule  
   - Max Capacity (Fixed at 20)  
   - Gym_ID (Foreign Key → Gymnasium)  

**Relationships:**

1. **A Gymnasium has many Members** → One-to-Many (Gymnasium → Member)  
2. **A Gymnasium offers many Sessions** → One-to-Many (Gymnasium → Session)  
3. **A Member can register for many Sessions, and a Session can have many Members** → Many-to-Many (Member ↔ Session)  
   - This requires a **Registration** associative entity:  
     - Registration_ID (Primary Key)  
     - Member_ID (Foreign Key → Member)  
     - Session_ID (Foreign Key → Session)  
4. **A Coach can lead multiple Sessions, and a Session can be led by up to two Coaches** → Many-to-Many (Coach ↔ Session)  
   - This requires a **Coach_Assignment** associative entity:  
     - Assignment_ID (Primary Key)  
     - Coach_ID (Foreign Key → Coach)  
     - Session_ID (Foreign Key → Session)  

Would you like a visual representation of this ER diagram?
