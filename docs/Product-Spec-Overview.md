<p align="center">
  <img src="../assets/logo.png" width="180" alt="URGLDN Logo">
</p>
# URGLDN – Product Specification Overview  
*A timing-first financial wellness tool for banks, credit unions, and fintech partners.*

---

## 1. Product Purpose

URGLDN is designed to solve one of the most common financial stressors:  
**bill timing that doesn’t match income timing.**

The system ensures users always have funds ready for upcoming payments by:

- Locking money ahead of time  
- Protecting it from accidental spending  
- Releasing it at the exact moment a bill is due  

URGLDN functions as a **timing automation layer** that sits on top of existing banking infrastructure.

---

## 2. Core System Components

### **2.1 Vaults**
A Vault represents a bill or recurring payment.

**Attributes:**
- Vault ID  
- User ID  
- Bill name (e.g., “Car Insurance”)  
- Amount required  
- Locked balance  
- Next release date/time  
- Recurrence pattern (weekly, bi-weekly, monthly, custom)  
- Status (funded, underfunded, pending release)

**Purpose:**  
Hold funds safely until the scheduled release moment.

---

### **2.2 Schedules**
Schedules define *when* a vault releases funds.

**Attributes:**
- Schedule ID  
- Vault ID  
- Release date/time  
- Recurrence rule  
- Optional buffer (e.g., release 24 hours early)

**Purpose:**  
Ensure precise timing for bill coverage.

---

### **2.3 Release Engine**
The Release Engine is the automation logic that:

- Monitors upcoming release times  
- Unlocks funds at the exact scheduled moment  
- Moves funds back to the user’s main account  
- Sends alerts before and after release  
- Flags shortfalls or missed funding

**Purpose:**  
Guarantee bill coverage without user intervention.

---

### **2.4 Notifications & Alerts**
URGLDN provides proactive communication:

- “Vault underfunded” alerts  
- “Upcoming release in 24 hours”  
- “Funds released successfully”  
- “Shortfall detected — add $X to stay covered”  

**Purpose:**  
Reduce stress and prevent surprises.

---

## 3. User Flows

### **3.1 Create a Vault**
1. User selects “Create Vault”  
2. Enters bill name, amount, due date  
3. Chooses recurrence  
4. Moves money into the vault  
5. URGLDN locks the funds

---

### **3.2 Funding a Vault**
- User manually adds money  
- OR bank auto‑routes deposits into vaults  
- System checks if vault is fully funded  
- Alerts user if more is needed

---

### **3.3 Release Flow**
1. Release Engine detects scheduled release  
2. Funds are unlocked  
3. Funds move to main account  
4. User receives confirmation  
5. Vault resets for next cycle

---

## 4. Integration Model (Bank/Fintech)

URGLDN is designed to integrate through:

### **4.1 API Layer**
Banks can connect via:

- REST API  
- Webhooks  
- Secure OAuth user authentication  

**Endpoints include:**
- Create Vault  
- Fund Vault  
- Get Vault Status  
- Create Schedule  
- Trigger Release  
- Get Upcoming Releases  

---

### **4.2 Data Requirements**
URGLDN requires access to:

- User account balances  
- Transaction history (optional)  
- Bill payment schedules (optional)  
- Transfer capabilities between internal accounts  

---

### **4.3 Security & Compliance**
- Follows Canadian banking standards  
- Uses institution’s existing authentication  
- No external data sharing  
- All analytics anonymized and aggregated  

---

## 5. Future Enhancements

### **5.1 AI Timing Insights**
Predicts:

- Best days to lock funds  
- Risk of shortfall  
- Pay cycle patterns  
- Bill timing conflicts  

### **5.2 Multi‑Account Support**
Joint accounts, business accounts, and family vaults.

### **5.3 “Stay Golden” Mode**
Automatically adds small buffers to reduce risk.

---

## 6. Target Partners

- Credit unions  
- Challenger banks  
- Payroll providers  
- Fintech budgeting apps  
- Financial wellness programs  

---

## 7. Status

URGLDN is currently in the **concept + specification** phase, with:

- Clear problem definition  
- Strong market need  
- Bank-ready executive summary  
- Product specification  
- Repo structure prepared for development  

URGLDN is ready for **licensing, co‑development, or pilot exploration**.

