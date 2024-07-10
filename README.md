# HospitalManagementSystem

Our Project is designed to manage information about
- Patients: People who came to get medical care in our hospital.
- Doctors: Part of a medical staff that takes care of patients.
- Nurses: Part of a medical staff that helps patients and assists doctors.
- Admin: Administrative personnel that takes care of managing hospital operations.
- Appointments: Scheduled visits for patients to see a doctor.
- Rooms: There are different types of rooms where services are provided for patients.
- Schedule: A schedule created for organizing doctors, patients, and room’s schedule.
Our ER diagram is structured around project description more precisely it is designed
around essential entities that are listed above and the relationships that are described in the
project description, and attributes which are essential to each of the entities.
Relationships:
One of the most important aspects of ER-diagram is precise description of all relationships.
Creates describes relationship between admin, doctor, nurse. In this relationship we can see
that both doctor and nurse have total participation, which indicates that both entities con
only be “created” by admin entity.
Assigning Rooms describes the process of assigning rooms to appointments. Lack of total
participation between this relationship, doctor and appointment entities is based on the
project description which states that it is optional for doctor to assign a room to a given
appointment, hence it is also optional for an appointment to have a room assigned.
However, nurse and room entities must totally participate, because it is stated that if a room
is to be assigned a nurse must be assigned with it, as per project description.
List Room Availability relationship describes the fact that only doctors can assign whether
rooms are available or not, which is optional, hence the relationship between doctor and
List Room Availability is not total(optional),whereas if a room is to be listed as empty or
occupied it must be reflected in a schedule, and in order to recognize a specific room entity
must also be present in this relationship with total participation.
List Doc Availability is another relationship that adheres to the requirements of the project,
which indicates that only doctors can list their availability in the schedule. Similarly, to the
relationship above in order to make this listing schedule entity must be in a total
relationship.
Book/Cancel Is a relationship that allows patients to book or cancel their appointments.
Patients are only allowed to book free timeslots which is the reason for schedule entities
total presence. If a patient chooses to book or cancel an appointment, appointment entity
must always keep a record which is a reason for its total participation in this relationship.
Patients can choose to book or cancel their appointments which is optional meaning partial
participation.
To organize our hospital's data, we use DDL (SQL commands). Each table is designed to hold
specific pieces of information.
