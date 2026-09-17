# VitalSync — Healthcare EHR Dashboard

## 1. Overview & Business Utility
VitalSync is an enterprise-grade Electronic Health Record (EHR) dashboard designed for healthcare providers, clinical administrators, and staff. It streamlines patient data management, clinical appointments, diagnostic record tracking, and real-time healthcare analytics while enforcing strict role-based access control and data security protocols.

## 2. Designated Track
**Option 2: VitalSync (Healthcare EHR Dashboard)**

## 3. Tech Stack
* **Frontend:** React.js / Next.js, Redux Toolkit / Zustand, Tailwind CSS
* **Backend:** Node.js, Express.js
* **Database:** MongoDB (Mongoose ODM)
* **Authentication:** JWT (JSON Web Tokens) with Role-Based Access Control (RBAC)
* **Design & Architecture:** Figma, Draw.io

---

## 4. Product Requirements & Feature Hierarchy

### Phase 1: Base MVP (Priority 0 - Mandatory)
- [ ] **Authentication & Security:** JWT-based login/register with Role-Based Access Control (`Admin`, `Doctor`, `Nurse`).
- [ ] **Patient Record Management (CRUD):** Create, update, view, and soft-delete patient profiles (Medical History, Demographics, Vitals).
- [ ] **Clinical Dashboard:** Primary view with key metrics (Total Patients, Today's Appointments, Pending Reports).
- [ ] **Appointment Scheduling:** Book, update status (Scheduled, In-Progress, Completed, Canceled), and assign appointments to doctors.

### Phase 2: Core Platform Features (Priority 1)
- [x] **Figma UI/UX Design System:**
  - Public Link: [VitalSync Figma Wireframes](https://www.figma.com/design/5ILOD4JFm6xsOacWrFtLyg/VitalSync-Wireframes?node-id=0-1&t=2QRbo4aLohTgfALx-1)
  - Core Viewports: Auth Screen, Clinical Dashboard, Patient Details/EHR View.
- [ ] **EHR Medical History & Lab Reports:** Upload and attach lab results and medical notes to specific patient records.
- [ ] **Search & Filtering:** Dynamic client/server-side search by Patient ID, Name, or Medical Condition.

### Phase 3: System Architecture & Optimization (Priority 2)
- [ ] **Entity Relationship Diagram (ERD):** Relational mapping of MongoDB collections (Users, Patients, Appointments, MedicalLogs).
- [ ] **State Tree & API Map:** Redux/Zustand state tree breakdown and documented REST API endpoints (`/api/v1/auth`, `/api/v1/patients`, `/api/v1/appointments`).
- [ ] **Data Analytics:** Visual chart integrations for patient admission trends and department load.

---

## 5. Proposed MongoDB Schema Overview
* **Users Collection:** `_id`, `name`, `email`, `passwordHash`, `role`, `department`
* **Patients Collection:** `_id`, `fullName`, `dob`, `gender`, `contact`, `vitals`, `assignedDoctorId`
* **Appointments Collection:** `_id`, `patientId`, `doctorId`, `appointmentDate`, `status`, `notes`
