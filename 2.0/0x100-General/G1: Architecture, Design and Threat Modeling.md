# G1: Architecture, design and threat modeling

## Control Objective

Architecture, design and threat modeling in the context of creating secure smart contracts.
Consider all possible threats before the implementation of the smart contract.

Ensure that a verified contract satisfies the following high-level requirements:
* All related smart contracts are identified and used properly,
* Specific smart contracts security assumptions are considered during the design phase.

Category “G1” lists requirements related to the architecture, design and threat modeling of the smart contracts.

## Security Verification Requirements

| # | Description |
| --- | --- |
| **1.1** | Verify that every introduced design change is preceded by an earlier threat modeling. |
| **1.2** | Verify that the documentation clearly and precisely defines all trust boundaries in the contract (trusted relations with other contracts and significant data flows).  |
| **1.3** | Verify that the SCSVS, security requirements or policy is available to all developers and testers. |
| **1.4** | Verify that the events for the (state changing/crucial for business) operations are defined. |
| **1.5** | Verify that there exists a mechanism that can temporarily stop the sensitive functionalities of the contract in case of a new attack. This mechanism should not block access to the assets (e.g. tokens) for their owners. |
| **1.6** | Verify that the amount of unused cryptocurrencies kept on the contract is controlled and at the minimum acceptable level so as not to become a potential target of an attack. |
| **1.7** | Verify that if fallback function can be called by anyone, it is included in the threat modeling. |
| **1.8** | Verify that the business logic in contracts is consistent. Important changes in the logic should be allowed for all or none contract. |
| **1.9** | Verify that code analysis tools are in use that can detect potentially malicious code. |
| **1.10** | Verify that the latest version of the major Solidity release is used. |
| **1.11** | Verify that, when using the external implementation of contract, you use the current version which has not been superseded. |
| **1.12** | Verify that when functions are overridden to extend functionality, the super keyword is used to maintain functionality. |
| **1.13** | Verify that the order of inheritance is carefully specified. |
| **1.14** | Verify that there is a component that monitors contract activity using events. |
| **1.15** | Verify that the threat model includes whale transactions. |
| **1.16** | Verify that there are no vulnerabilities associated with system architecture and design. |

## References

For more information, see also:

* [Instant Threat Modeling - SecuRing](https://www.youtube.com/watch?v=IwR4PAmRhhg&list=PL-lO2xrptAtav4SZgCdDkVxChWhVU3kmP&index=18)
* [OWASP Threat Modeling Cheat Sheet](https://github.com/OWASP/CheatSheetSeries/blob/master/cheatsheets/Threat_Modeling_Cheat_Sheet.md)
* [OWASP Attack Surface Analysis Cheat Sheet](https://github.com/OWASP/CheatSheetSeries/blob/master/cheatsheets/Attack_Surface_Analysis_Cheat_Sheet.md)
* [OWASP Threat modeling](https://www.owasp.org/index.php/Application_Threat_Modeling)
* [Microsoft SDL](https://www.microsoft.com/en-us/sdl/)
* [NIST SP 800-57](https://csrc.nist.gov/publications/detail/sp/800-57-part-1/rev-4/final)
* [Use events to monitor contract activity](https://consensys.github.io/smart-contract-best-practices/recommendations/#use-events-to-monitor-contract-activity)
* [An example of superseded contract - EIP 1820](https://eips.ethereum.org/EIPS/eip-1820)