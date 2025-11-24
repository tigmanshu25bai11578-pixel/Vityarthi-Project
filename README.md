# Vityarthi-Project
## 🏥 Hospital Management System (Python)

This is a simple console-based **Hospital Management System** written in Python for managing patient check-in, calculating billing, and storing patient records.

---

### 📝 Features

* [cite_start]**Patient Check-in:** Collects essential patient information such as name [cite: 1][cite_start], nationality, address [cite: 1][cite_start], contact number, blood group [cite: 2][cite_start], check-in/out dates [cite: 2, 6][cite_start], and medical issue[cite: 2].
* [cite_start]**Vitals Recording:** Records the patient's **Body Temperature** and **Blood Pressure**[cite: 2].
* [cite_start]**Condition-Based Ward Assignment:** Based on the patient's condition[cite: 3]:
    * [cite_start]If the condition is **"Critical"**, the patient is admitted to the **ICU**[cite: 3].
    * [cite_start]Otherwise, the patient is admitted to the **General Ward**[cite: 3].
* [cite_start]**Dynamic Billing:** Calculates the total bill based on the selected ward type, number of days of stay[cite: 6], and an added **GST** (Goods and Services Tax).
    * [cite_start]The GST rate is set at **20% (0.20)**[cite: 1].
* [cite_start]**Billing Summary:** Prints a detailed summary including the Ward Fee per Day, Amount (excluding GST), GST Amount, and Total Amount (including GST)[cite: 5].
* [cite_start]**Patient Record Storage:** Stores all entered patient and billing details in a dictionary called `patient_record`[cite: 1, 7].
* [cite_start]**Multi-Patient Support:** Allows for continuous entry and billing of multiple patients until the user chooses to exit[cite: 7, 8].

---

### 💻 Ward Charges

[cite_start]The system uses the following predefined charges for different ward types (per day)[cite: 4]:

| Ward Type | Charge (per day) |
| :-------- | :--------------- |
| **1** | $1,800$ |
| **2** | $2,500$ |
| **3** | $3,500$ |
| **4** | $5,000$ |

> [cite_start]**Note:** If a user selects a ward type other than 1-4, the default charge of $5,000$ will be applied[cite: 4].

---

### 🚀 Getting Started

#### Prerequisites

* You must have **Python 3** installed on your system.

#### Running the Script

1.  **Save the Code:** Save the provided Python code as a file (e.g., `hospital_management.py`).
2.  **Execute:** Open your terminal or command prompt, navigate to the directory where you saved the file, and run the script:

    ```bash
    python hospital_management.py
    ```

3.  [cite_start]**Follow Prompts:** The system will guide you through entering patient details, selecting the ward type, and entering the number of days of stay[cite: 4].
4.  [cite_start]**View Records:** After processing all patients and exiting (by entering `no` when prompted [cite: 8][cite_start]), the complete `patient_record` will be printed to the console[cite: 8].

---

### ⚙️ How Billing Works

[cite_start]The total bill is calculated using the following steps[cite: 4, 1]:

1.  **Base Amount (Amount excluding GST):**
    $$\text{Base Amount} = \text{Ward Fee per Day} \times \text{Number of Days of Stay}$$
2.  **GST Amount:**
    $$\text{GST Amount} = \text{Base Amount} \times 0.20$$
3.  **Total Amount (including GST):**
    $$\text{Total Amount} = \text{Base Amount} + \text{GST Amount}$$
