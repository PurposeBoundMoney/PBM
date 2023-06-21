This repository and its contents are made available on an “as-is” basis without warranties of any kind. The content in this repository does not constitute regulatory, financial, legal or any other professional advice and should not be acted on as such. MAS shall not be liable for any damage or loss of any kind howsoever caused as a result of the use of the information contained or referenced in this report.


# Purpose Bound Money

Purpose Bound Money proposes a common protocol to specify conditions for the use of digital money. The “Purpose Bound Money Technical Whitepaper”, provides technical overview to the concept of PBM. The report is available at: https://www.mas.gov.sg/publications/monographs-or-information-paper/2023/purpose-bound-money-whitepaper.

The whitepaper was supported by the release of software prototypes that demonstrate the concept of PBM, which enables senders to specify conditions, such as validity period and types of shops, when making transfers in digital money across different systems.

For illustration purposes, a sample PBM implementation is provided here. This was developed with reference to the Ethereum Improvement Proposal (EIP) as a design document providing information or describing new features or its processes or environment, to spur further industry development.

The PBM design is technology neutral and aims to work across different types of ledgers and assets. It is envisioned that PBM could be implemented on both distributed and non-distributed ledgers. It is envisioned that future implementations of PBM could be based on a different ledger system from the ones referenced in this paper and in the samples provided. 

## Understanding the Specification 
This design document sets out the common interface on what constitutes a PBM. It allows developers from all over the world to have a common understanding on the types of function to implement. 

It's crucial to read and understand the whitepaper first, as it provides valuable insights into the goals of the specification.


## Evaluate Compatibility
This specification necessitates the use of a Solidity compiler with a minimum version of 0.8.0. Utilizing a prior version is permissible, contingent upon adequate scrutiny and security assessments.

## Implementing the Specification

There's 2 main interface in this repository, namely: `interface IPBMRC1` and `PBMRC2_NonPreloadedPBM `. Depending on the specific requirements of the PBM, either interface can be chosen for implementation. 

### Sample code: 

```solidity

pragma solidity ^0.8.0;


contract PBMDemo is IPBMRC1 {

    // implement and override all functions within the interface itself.
}

```


In both of the interface, additional business logic can either be implemented as a state variable referencing an external smart contract, writen within a contract function or injected via the init function `function initialise(address _spotToken, uint256 _expiry, address _pbmWrapperLogic) external;`  


