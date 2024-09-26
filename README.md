# SnarkJS Extension Example

This project demonstrates how to run SnarkJS within a browser extension. Since SnarkJS cannot be executed directly due to security concerns, we have applied a **sandbox** policy to safely handle zk-SNARK operations within a separate iframe.

### Key Policies

- **Sandbox**: A separate iframe environment is used to run SnarkJS operations, isolating them from the rest of the browser. This ensures that zk-SNARK proof generation and verification are securely executed without interference from external code.
- **Content Security Policy (CSP)**: All scripts running within the extension are restricted to 'self' and 'unsafe-eval' policies, ensuring that SnarkJS operates only within the sandboxed iframe environment, thus enhancing overall security.
