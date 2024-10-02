
# 🌐 Project Name: Anonymous Feedback dApp

A full-stack decentralized application (dApp) built on the Stellar blockchain 🌟. This dApp allows users to submit anonymous feedback seamlessly. The smart contract assigns a unique ID to each feedback entry, which can later be accessed using its corresponding feedback ID.

🔗 **Project Repository**: [Anonymous Feedback Blockchain](https://github.com/pkprajapati7402/Anonymous-Feedback-Blockchain)

---

## 📑 Table of Contents:
1. [Technologies Used](#-technologies-used)
2. [Smart Contract Info](#-smart-contract-info)
3. [⚠️ Current Issue](#%EF%B8%8F-current-issue)
4. [🛠️ Project Setup Guide](#%EF%B8%8F-project-setup-guide)

---

## 🛠️ Technologies Used:
- **Smart Contract**: Rust, Soroban-SDK
- **Wallet**: Freighter (Chrome extension)
- **Frontend**: ReactJS, TailwindCSS
- **Integration**: Stellar-SDK

---

## 📜 Smart Contract Info:

All smart contract-related files are located in the `anonymous-feedback-smartcontract` folder.

- **Smart Contract Path**:  
  `./anonymous-feedback-smartcontract/contracts/hello_world/src/lib.rs`

### 🔗 Deployed Smart Contract Address:  
`CDAN4KQKD633XF6MCOHI7Q3DJQX4E7ENCGKUBHGQKIKJWI6DVDPX54XW`

### ⚙️ Functions in the Anonymous Feedback Smart Contract:

1. **`send_feedback(env: Env, feedback_msg: String) -> u64`**:  
   Accepts a feedback message (`String`), assigns a unique ID, stores it on the blockchain, and returns the feedback ID.

2. **`fetch_feedback(env: Env, fb_id: u64) -> Feedback`**:  
   Retrieves feedback using the provided feedback ID (`u64`).

---

## ⚠️ Current Issue:

### 🛑 **Issue**: 
`undefined` when fetching data from the blockchain using Stellar-SDK.

#### ⚙️ Working Functions:
Both `send_feedback()` and `fetch_feedback()` function correctly when invoked via Stellar-CLI. 

#### 🐛 **Issue Details**:  
The `fetch_feedback()` function returns `undefined` when called via the `fetchFeedback()` interaction function using Stellar-SDK (located in `src/components/Soroban.js`).

Similarly, the `sendFeedback()` function correctly stores feedback on the blockchain but returns `undefined` instead of the expected feedback ID.

### 🗂️ **Soroban.js File Path**:  
`src/components/Soroban.js`

🔗 **Documentation Reference**:  
[Stellar Transaction Builder Guide](https://developers.stellar.org/docs/build/guides/transactions/invoke-contract-tx-sdk)

---

## 🖼️ Screenshots of the Issue:

1. **Creating Feedback via `send_feedback()`**:  
   ![image](https://github.com/user-attachments/assets/83bfebed-4b14-4ff9-b38d-575c9e89f9e2)
   
   - **Expected Output**: `4`
   - **Received Output**: `undefined`  
     ![image](https://github.com/user-attachments/assets/e0623442-1a5f-4773-8a53-adb7ecf90f9d)

2. **Fetching Feedback with ID `4` using `fetch_feedback()`**:  
   ![image](https://github.com/user-attachments/assets/1baba311-3c23-425e-977f-da052c90af54)
   
   - **Expected Output**: `Feedback Number 4`
   - **Received Output**: `undefined`  
     ![image](https://github.com/user-attachments/assets/c33ae590-1a3a-44c2-9501-35b92b1f9dda)

---

## 🛠️ Project Setup Guide:

1. Install the following:
   - NodeJS
   - Rust
   - Stellar-CLI
2. Add the [Freighter Wallet](https://www.freighter.app/) Chrome extension.
3. Clone the repository:  
   ```bash
   git clone https://github.com/pkprajapati7402/Anonymous-Feedback-Blockchain.git
   ```
4. Install project dependencies:  
   ```bash
   npm install
   ```
5. Start the project:  
   ```bash
   npm run start
   ```

---

Feel free to reach out if you encounter any issues or have suggestions for improvements! 😊
