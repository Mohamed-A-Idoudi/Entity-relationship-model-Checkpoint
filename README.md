# Entity-relationship-model-Checkpoint

Entities and Attributes:
  1-Gymnasium:
   *Attributes:
     *Name (Primary Key)
      *Address
      *Phone Number

  2-Member:
    *Attributes:
      *MemberID (Primary Key)
      *Last Name
      *First Name
      *Address
      *Date of Birth
      *Gender
      *Gymnasium Name (Foreign Key)
   
  3-Session:
    *Attributes:
      *SessionID (Primary Key)
      *Type of Sport
      *Schedule (Date/Time)
      *Max Capacity (20 members)

  4-Coach:
    *Attributes:
      *CoachID (Primary Key)
      *Last Name
      *First Name
      *Age
      *Specialty

Relationships:
  1-Gymnasium and Member:
    *Relationship: One Gymnasium has many Members.
    *Cardinality: 1 (One-to-Many)
    *Explanation: A member can register at one gymnasium, but a gymnasium can have many members.
    
  2-Member and Session:
    *Relationship: Many Members can attend many Sessions (up to 20 members per session).
    *Cardinality: M  (Many-to-Many)
    *Explanation: A member can enroll in multiple sessions, and a session can have up to 20 members.
  
  3-Session and Coach:
    *Relationship: Many Sessions can be led by many Coaches (up to 2 coaches per session).
    *Cardinality: M (Many-to-Many)
    *Explanation: A session can have up to 2 coaches, and a coach can lead multiple sessions.




Entity-Relationship Diagram (ERD) Overview:
  -Gymnasium ↔ Member
    *Gymnasium (1) ———< Member (N)
  -Member ↔ Session
    *Member (M) ———< Session (N)
  -Session ↔ Coach
    *Session (M) ———< Coach (N)
