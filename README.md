# Purpose Bound Money

Purpose Bound Money proposes a common protocol to specify conditions for the use of digital money. 

The PBM Whitepaper can be found [here](https://www.mas.gov.sg/publications/monographs-or-information-paper/2022/project-orchid-whitepaper)

# Using the EIP

## Understanding the EIP 
This EIP sets out the common interface on what constitutes a PBM. It allows developers from all over the world to have a common understanding on the types of function to implement. 

It's crucial to read and understand the whitepaper first, as it provides valuable insights into the goals of the specification.


## Evaluate Compatibility
This EIP necessitates the use of a Solidity compiler with a minimum version of 0.8.0. Utilizing a prior version is permissible, contingent upon adequate scrutiny and security assessments.

## Implementing the EIP

There's 2 main interface in this repository, namely: `interface IPBMRC1` and `PBMRC2_NonPreloadedPBM `. Depending on the specific requirements of the PBM, either interface can be chosen for implementation. 

### Sample code: 

```solidity

pragma solidity ^0.8.0;


contract PBMDemo is IPBMRC1 {

    // implement and override all functions within the interface itself.
}

```


In both of the interface, additional business logic can either be implemented as a state variable referencing an external smart contract, writen within a contract function or injected via the init function `function initialise(address _spotToken, uint256 _expiry, address _pbmWrapperLogic) external;`  


