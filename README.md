# IT Equipment Request Management System – ServiceNow

A complete **IT Equipment Request Management System** built on **ServiceNow**, designed to streamline how employees request hardware and how IT fulfills them.  
This project covers everything from UI design to backend automation, approvals, integrations, and secure access control.

---

## 🚀 Features

### 📄 Custom Forms
- **Admin Form** – Add, edit, and manage IT equipment (laptops, monitors, accessories, etc.)
- **User Request Form** – Submit new equipment requests and track lifecycle

### 💡 Client Scripts
- Auto-calculates item total price (Unit Price × Quantity)
- Real-time validation and dynamic field updates

### ⚙️ Business Rules
- Automatically assigns the requester’s manager
- Controls lifecycle states and backend logic
- Ensures data consistency between Request and Fulfillment Tasks

### 🔁 Flow Designer Automation
- Sends approval requests to managers
- Creates fulfillment tasks automatically upon approval
- Handles approval/rejection flows and notifications

### 🌐 Scripted REST API (Full CRUD)
External systems can:
- **GET** equipment requests  
- **POST** new requests  
- **PUT** updates  
- **DELETE** records  
Perfect for HR, onboarding, or third-party integrations.

### 🔐 ACL Security
- Only the requester, manager, and IT staff can view or update the request
- Role-based access control for Admin features
- Ensures data confidentiality and correct permissions

---

## 🧰 Tech Stack
- **ServiceNow** (Rome → Vancouver compatible)
- **JavaScript** (Client Scripts)
- **Business Rules**
- **Flow Designer**
- **Scripted REST APIs**
- **ACLs & Roles**

---





---

## 📡 API Example
### POST Request
```
POST https://dev313196.service-now.com/api/x_1858574_it_reque/it_request/request

BODY
{
  "item":"0ae345dd93193210fd263a6efaba 1075" ,
  "opened_by":"6816f79cc0a8016401c5a33be04be441" ,
  "requesrted_for" ; "6816f79cc0a8016401c5a33be04be441"
}
```


### Example Response
```json
"result": {
    "id" ; "d880fe9293ddf21Øfd263a6efaba1076",
    "requested for" : "62d78687c0a010e00b3d84178adc913",
    "total cost": "140"
}
```

### GET Request
```
GET https://dev313196.service-now.com/api/x_1858574_it_reque/it_request/request/{req_sys_id}
```

### Example Response
```json
"result": {
"sys ld" : "d88Øfe9293ddf21Øfd263a6efaba1Ø76",
"Opened by" : "6816f79ccea8Ø164e1c5a33beø4be441",
"Requested_for" : "62d78687cea8Ø1øeøeb3d84178adc913",
"Item": "0ae345dd9319321Øfd263a6efaba1Ø75",
"Quantity" ; "2"
"Total Cost": "140
"Status": "requested"
}
```

---

## ✨ What I Learned
- Designing ServiceNow forms for real-world use cases  
- Building scalable workflows using **Flow Designer**  
- Creating secure and reusable **Scripted REST APIs**  
- Writing clean **client-side** and **server-side** scripts  
- Applying **ACLs** to ensure proper data access  

---



## 📬 Contact
Feel free to reach out if you'd like to collaborate or discuss ServiceNow development!
