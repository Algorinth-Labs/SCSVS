# G105: Access control

## Control Objective

Access control is the process of granting or denying specific requests to obtain and use information and related information processing services.

Ensure that a verified contract satisfies the following high-level requirements:
* Users and other contracts are associated with a well-defined set of roles and privileges,
* Access is granted only to the privileged users and contracts.

Category “G105” lists requirements related to the access control mechanisms of the smart contracts.

## Security Verification Requirements

| # | Description |
| --- | --- |
| **105.1** | Verify that there are no vulnerabilities associated with access control. | 
| **105.2** | Verify that the principle of the least privilege exists. Other contracts should only be able to access functions and data for which they possess specific authorization. | 
| **105.3** | Verify that new contracts with access to the audited contract adhere to the principle of minimum rights by default. Contracts should have a minimal or no permission until access to the new features is explicitly granted. | 
| **105.4** | Verify that the creator of the contract complies with the rule of the least privilege and their rights strictly follow the documentation. |
| **105.5** | Verify that the contract enforces the access control rules specified in a trusted contract, especially if the dApp client-side access control is present and could be bypassed. | 
| **105.6** | Verify that the calls to external contracts are allowed only if necessary. | 
| **105.7** | Verify that the code of modifiers is clear and simple. The logic should not contain external calls to untrusted contracts. | 
| **105.8** | Verify that all user and data attributes used by access controls are kept in trusted contract and cannot be manipulated by other contracts unless specifically authorized. | 
| **105.9** | Verify that the access controls fail securely, including when a revert occurs. | 
| **105.10** | Verify that if the input (function parameters) is validated, the positive validation approach (allowlisting) is used where possible. | 

## References

For more information, see also:

* [OWASP Cheat Sheet: Access Control](https://github.com/OWASP/CheatSheetSeries/blob/master/cheatsheets/Access_Control_Cheat_Sheet.md)
* [OpenZeppelin: Role-Based Access Control](https://github.com/OpenZeppelin/openzeppelin-solidity/blob/852e11c2dbb19a4000decacf1840f5e4c29c5543/docs/access-control.md#role-based-access-control)
