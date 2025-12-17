# ZeroID: Formal Security Verification

**Author:** AIT BEN IYCHE Omar  
**Protocol:** ZeroID (Privacy-Preserving Authentication with zk-SNARKs)  
**Verification Tool:** ProVerif 2.05

This repository contains the formal symbolic analysis of the **ZeroID** protocol. The model uses the applied pi-calculus to verify that the integration of OpenID Connect (OIDC) with Zero-Knowledge Proofs guarantees strong authentication and user privacy (unlinkability) against a Dolev-Yao active adversary.

---

## 📂 Repository Structure

- **`zeroID.pv`**: The main ProVerif model source code. It defines:
  - **Cryptographic Primitives:** `ZeroID_Proof` (zk-SNARK), `ZeroID_Verify`, `Poseidon` hashing.
  - **Protocol Participants:** `RunZeroID_Client` and `RunZeroID_Server`.
  - **Security Query:** Injective correspondence for authentication.

---

## 🚀 How to Run

1. **Install ProVerif:**
   Ensure `proverif` is installed and in your system PATH.

2. **Execute the Verification:**
   Run the following command in your terminal:
   ```bash
   proverif zeroID.pv
