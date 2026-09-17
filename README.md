# 🚇 Metro Ticket Generating System in ServiceNow

## 📌 Project Overview

The **Metro Ticket Generating System** is a ServiceNow-based project developed to digitize and automate the metro ticket booking process.

The system allows passengers to select their source and destination stations, choose the journey type, specify the number of passengers, select a payment mode, calculate the ticket amount, and generate a QR-based digital ticket.

The main goal is to reduce waiting time, minimize manual effort, improve fare calculation accuracy, and provide a convenient paperless ticketing experience.

---

## 🎯 Objectives

* Digitize the metro ticket booking process using ServiceNow.
* Reduce passenger waiting time and manual ticketing effort.
* Provide easy source and destination station selection.
* Automate fare calculation.
* Support digital payment options such as UPI and Card.
* Generate QR-based digital metro tickets.
* Reduce paper usage through digital tickets.
* Improve operational efficiency and commuter convenience.

---

## 👥 Stakeholders

* **Passengers** – Book metro tickets and receive digital QR-based tickets.
* **Station Managers** – Maintain metro station information.
* **Metro Operations Team** – Support metro ticketing and operational activities.
* **IT Administrators** – Maintain and manage the ServiceNow application.

---

## 🛠️ Technologies Used

* **ServiceNow**
* **Service Catalog**
* **Custom ServiceNow Tables**
* **Catalog Variables**
* **Catalog Client Scripts**
* **UI Policies**
* **Process Automation Engine**
* **JavaScript**
* **Service Portal**
* **ServiceNow Widgets**
* **QR Code Integration**
* **ServiceNow ACLs**
* **GitHub**

---

## 🏗️ Main Components

### 1. Metro Station Details Table

A custom ServiceNow table is used to store and manage metro station information.

**Table Name:**

```text
u_metro_station_s_details
```

The table provides station information used in the ticket booking form, including:

* Starting From
* Going To

This station information is mapped to the corresponding catalog variables for ticket booking.

---

### 2. Book A Metro Ticket

A Service Catalog item is created to provide the passenger with a digital metro ticket booking form.

**Catalog Item:**

```text
Book A Metro Ticket
```

The form contains the following variables:

* Starting From
* Going To
* Type Of Journey
* No Of Passengers
* Amount For Single Journey
* Amount Including Return
* Mode Of Payment

---

### 3. Journey Type

Passengers can select the required type of journey:

* **Single Journey**
* **Return Journey**

The selected journey type is used during the ticket and fare processing.

---

### 4. Number of Passengers

The booking form supports passenger selection from:

* 1 Passenger
* 2 Passengers
* 3 Passengers
* 4 Passengers

The selected passenger count is considered during fare calculation.

---

### 5. Payment Mode

The system provides the following payment options:

* **UPI**
* **Card**
* **Others**

This provides flexibility for digital and other payment methods.

---

### 6. Fare Calculation

The system calculates the ticket amount based on the selected journey type and number of passengers.

The booking form displays the applicable amount for:

* Single Journey
* Return Journey

This reduces manual fare calculation and helps improve accuracy.

---

### 7. QR Code Generation

After successful ticket processing, a QR-based digital ticket is generated.

The QR code provides a convenient way to represent and verify the generated metro ticket information.

---

### 8. Metro QR Widget

A custom ServiceNow widget is used to display the generated QR code and related scanning information.

**Widget Name:**

```text
Metro QR Widget
```

**Widget ID:**

```text
metro_qr_widget
```

The widget provides the passenger with the digital QR ticket after booking.

---

## ⚙️ ServiceNow Automation

The system uses ServiceNow automation features to simplify the ticket booking process.

### Catalog Client Scripts

Used for client-side form behavior, default values, and automatic field handling.

### UI Policies

Used to control field behavior such as:

* Mandatory fields
* Read-only fields
* Field visibility
* Dynamic form behavior

### Process Automation Engine

Used for field mapping and automatically populating values based on information entered or selected by the passenger.

### Field Validation

The system validates important booking information such as:

* Source station
* Destination station
* Journey type
* Number of passengers
* Travel-related information
* Fare details

---

## 🔐 Access Control

ServiceNow ACLs are used to control access to application data.

Passengers can use the ticket booking interface without directly accessing the underlying database tables.

The custom tables use the default ACLs created by ServiceNow during table creation. No additional custom ACLs were configured specifically for restriction purposes.

---

## 🔄 Ticket Booking Flow

```text
Passenger
    ↓
ServiceNow Service Portal
    ↓
Book A Metro Ticket
    ↓
Select Starting From
    ↓
Select Going To
    ↓
Select Journey Type
    ↓
Select Number of Passengers
    ↓
Calculate Fare
    ↓
Select Payment Mode
    ↓
Submit Booking
    ↓
Request / Requested Item Generated
    ↓
Generate QR Code
    ↓
Display Digital QR Ticket
```

---

## 🗺️ Project Execution Roadmap

```text
Catalog Form Setup
        ↓
Variables Configuration
        ↓
Station Details Mapping
        ↓
Fare Calculation Logic
        ↓
QR Code Integration
        ↓
Metro QR Widget
        ↓
Field Validation
        ↓
QA Testing
        ↓
UAT & Deployment
```

---

## 🧪 QA Testing

The system is tested to ensure correct form behavior and ticket generation.

### Testing Areas

* Source and destination validation
* Mandatory field validation
* Journey type selection
* Passenger count validation
* Fare calculation
* Payment mode selection
* Auto-population of fields
* Station details mapping
* Request generation
* Requested Item generation
* QR code generation
* QR ticket visibility

### Validation

**Mandatory Fields:**
Required fields must be completed before submitting the booking.

**Station Validation:**
Valid source and destination stations must be selected.

**Fare Validation:**
The generated fare should correspond to the selected journey type and number of passengers.

**Field Mapping:**
Values entered or selected by the passenger are mapped to the corresponding ServiceNow fields.

---

## 📊 Data Architecture

The system uses ServiceNow tables and catalog variables to collect, store, and process metro ticket booking information.

```text
Passenger Input
      ↓
Catalog Variables
      ↓
ServiceNow Automation
      ↓
Metro Station Details
      ↓
Fare Processing
      ↓
Ticket Information
      ↓
QR Code
```

The custom station table provides the station information required by the booking form, while the Service Catalog manages the passenger's ticket request.

---

## 🎥 Demo Video

A demonstration of the Metro Ticket Generating System is available below:

**[▶️ Watch the Project Demo](https://drive.google.com/file/d/1_n5l0LV2WJAr40OnDQjY0JU9HehS3drd/view?usp=drive_link)**

The demo demonstrates the ticket booking form, station selection, journey selection, passenger selection, fare calculation, payment mode selection, request generation, and QR-based digital ticket.

---

## 📸 Screenshots

Screenshots of the ServiceNow implementation can be added here.

Recommended screenshots:

1. ServiceNow Dashboard
2. Metro Station Details Table
3. Metro Station Records
4. Book A Metro Ticket Catalog Item
5. Catalog Variables
6. Ticket Booking Form
7. Submitted Request
8. Requested Item
9. Fare Calculation
10. Metro QR Widget
11. Generated QR Ticket

---

## 🔮 Future Enhancements

The system can be further enhanced with:

* UPI payment gateway integration
* Real-time metro fare calculation
* Live station and route information
* Automated passenger notifications
* Mobile application integration
* WhatsApp-based ticket booking
* Real-time QR ticket validation
* Metro gate/QR scanner integration
* Passenger and operational analytics

---

## 🌱 Environmental Benefits

The system supports paperless ticketing by replacing physical tickets with digital QR-based tickets.

This can help reduce paper consumption while providing passengers with a faster and more convenient ticketing experience.

---

## 📌 Conclusion

The **Metro Ticket Generating System in ServiceNow** provides a digital and automated approach to metro ticket booking.

By combining **Service Catalog, custom tables, catalog variables, automation, station mapping, fare calculation, validation, and QR-based digital tickets**, the system reduces manual effort and improves the overall ticket booking experience.

The project demonstrates how the ServiceNow platform can be used to develop an automated and user-friendly solution for digital metro ticketing.

---


