# RTS API — Bruno Collection

Complete API test collection for the RTS (Request Tracking System) backend.

## Setup

1. Open Bruno desktop app
2. Click **Open Collection** → select this `RTS-API` folder
3. Select the **Local** environment (top-right dropdown)
4. Run **Health Check** first to confirm the backend is running

## Workflow — full 3-step approval test

```
1. Health Check            → confirm server is running
2. Login (as Requestor)    → token auto-saved
3. Create Request          → requestId auto-saved
4. Get All Requests        → verify request appears
5. Login (as RM)           → token auto-saved
6. Approve Request (RM)    → Step 1 approval
7. Login (as HOD)          → token auto-saved
8. Approve Request (HOD)   → Step 2 approval
9. Login (as DeptHOD)      → token auto-saved
10. Approve Request (DeptHOD) → Step 3 approval
11. Close Ticket            → ticket closed
12. Send Text Message       → should return 403 (closed)
```

## Environments

| Environment            | URL                          |
|------------------------|------------------------------|
| Local                  | http://localhost:5000/api     |
| Network (192.168.1.128)| http://192.168.1.228:5000/api |
| Production             | https://your-backend.com/api  |

## Credentials quick reference

| Role      | Email                         | Password             |
|-----------|-------------------------------|----------------------|
| Requestor | santhosh.sm9@gmail.com        | Santhosh@123         |
| RM        | kadakkath@gmail.com           | Anil@123             |
| HOD       | bhatraveendrabeegar@gmail.com | Raveendra@123        |
| DeptHOD   | software@rts.com              | Software@123         |
| DeptHOD   | operation@rts.com             | Operation@123        |
| Admin     | admin@rts.com                 | Admin@123            |

Full credentials list: see Login.bru docs tab
