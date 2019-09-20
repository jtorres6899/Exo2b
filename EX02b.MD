# Step one: Identify Candidate Key
* #### PET-AND-OWNER(***PetName***,Petype, Petbreed, PetDOB, Ownerlastname, OwnerFirstName ,OwnerPhone, OwnerEmail, Service,Date,Charge) 
### PET AND OWNER Candidate Keys: (PetName, Date) 
## Functional Dependencies:
  - #### Petname--> (Petype, Petbreed, PetDOB, Ownerlastname, OwnerFirstName ,OwnerPhone, OwnerEmail)  
  - #### OwnerEmail --> (OwnerLastname, OwnerFirstName, OwnerPhone)
  - #### OwnerPhone --> (OwnerLastName, OwnersFirstName, OwnerEmail)
  - #### (Petname, Date)--> (Service, Charge)


# Step Two: Identify Dependencies
### Two Relations: Owner and Pet-Service
  - #### OWNER (OwnersLastName ,OwnersFirstName, OwnerPhone, OwnerEmail)
  - #### PET- SERVICE (Petname, PetType, PetBreed, PetDOB, Service, Date, Charge) 
### Owner Dependencies
   - #### OwnerEmail--> (OwnerLastName, OwnerFistName, OwnerPhone)
   - #### OwnerPhone--> (OwnerLastName, OwnerFistName, OwnerPhone)
### Owner Candidate Keys: OwnerPhone and OwnerEmail
## Primary Key: OwnerPhone
  - #### OWNER(***OwnerPhone***, OwnerLastName, OwnerFistName, OwnerEmail)
  - #### PET-SERVICE(***PetName***,Petype, Petbreed, PetDOB, OwnerPhone, Service,Date,Charge)
## Pet-Service Dependencies 
  - #### Petname--> (Petype, Petbreed, PetDOB,OwnerPhone)
  - #### (PetName, Date)-->(Service, Charge)
## Pet and Service Candidate keys: (PetName, Date) 


# Step Three: Make all Determinants into a Candidate Key
### Two Relations: Pet and Service 
  - #### OWNER(***OwnerPhone***,OwnersLastName ,OwnersFirstName, OwnerEmail)
  - #### PET(***PetName***,Petype, Petbreed, PetDOB, OwnerPhone)
  - #### SERVICE(***PetName***,***Date***, Service, Charge) 
## PET Dependencies
  - #### PetName-->(Petype, Petbreed, PetDOB, OwnerPhone)
### PET Candidate Keys: Petname 
## SERVICE Dependencies 
  - #### (Petname, Date)-->(Service, Charge) 
# Normalized Realtions:
  - ### OWNER(***OwnerPhone***, OwnerLastName, OwnerFistName, OwnerEmail)
  - ### PET(***PetName***,Petype, Petbreed, PetDOB, OwnerPhone) 
  - ### SERVICE(***PetName***,***Date***, Service, Charge) 
