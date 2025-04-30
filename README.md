# DAOGovernance

A decentralized governance system that enables token-weighted voting for decentralized autonomous organizations.

## Overview

DAOGovernance is a blockchain-based governance framework that empowers token holders to participate in decision-making through a transparent and trustless proposal and voting mechanism. The system allows for community-driven decision making where voting power is proportional to token holdings.

## Features

- **Token-Weighted Voting**: Voting power is proportional to the number of governance tokens held
- **Proposal Creation**: Any token holder can create proposals for community consideration
- **Decentralized Decision Making**: Automated execution of passed proposals
- **Flexible Parameters**: Adjustable quorum thresholds, proposal durations, and fees
- **Governance Analytics**: Comprehensive voting statistics and proposal status tracking
- **Customizable Governance**: Contract parameters can be updated through governance

## Contract Functions

### Read-Only Functions

- `get-proposal`: Retrieve details about a specific proposal
- `get-vote`: View vote information from a specific voter on a proposal
- `proposal-exists`: Check if a proposal exists
- `is-proposal-active`: Verify if a proposal is still active
- `has-proposal-ended`: Check if a proposal's voting period has ended
- `get-token-balance`: View governance token balance for an account
- `get-total-supply`: Get the total supply of governance tokens
- `get-proposal-results`: Get detailed results for a specific proposal
- `get-current-proposal-id`: Get the next available proposal ID

### Public Functions

- `create-proposal`: Create a new governance proposal
- `cast-vote`: Cast a vote on an active proposal
- `cancel-proposal`: Cancel an active proposal (by creator only)
- `finalize-proposal`: Update proposal status after voting period ends
- `execute-proposal`: Execute a passed proposal
- `mint-tokens`: Administrative function to create governance tokens
- `update-proposal-fee`: Update the fee required to create proposals
- `update-min-proposal-duration`: Update the minimum proposal voting period
- `update-default-quorum-threshold`: Update the default participation threshold
- `transfer-ownership`: Transfer contract administrative rights

## Getting Started

### Prerequisites

- A compatible blockchain wallet
- Governance tokens for participation

### Creating a Proposal

1. Define your proposal details (title, description, external link)
2. Set the voting period duration and quorum threshold
3. Pay the proposal fee in governance tokens
4. Call the `create-proposal` function with these parameters

### Casting a Vote

1. Find an active proposal using its ID
2. Choose your vote type: For, Against, or Abstain
3. Call the `cast-vote` function with the proposal ID and your vote type
4. Your vote's weight is automatically calculated based on your token balance

### Finalizing and Executing Proposals

1. After the voting period ends, anyone can call `finalize-proposal`
2. If the proposal passes (quorum reached and more For than Against votes), its status changes to "Passed"
3. Call `execute-proposal` to implement the proposal's intended changes

## Governance Parameters

- **Proposal Fee**: A small fee required to create proposals (prevents spam)
- **Minimum Proposal Duration**: The shortest allowed voting period
- **Default Quorum Threshold**: Minimum participation required for a valid vote
- **Vote Types**: For (support), Against (oppose), or Abstain (neutral)

## Security Considerations

- Only proposal creators can cancel their proposals
- Proposal execution only possible after voting period ends
- Only one vote per account per proposal
- Token-weighted voting prevents sybil attacks
- Administrative functions protected by ownership controls

## Future Development

- Integration with multiple token standards
- Delegated voting system
- Quadratic voting option
- Proposal templates
- Time-locked execution
- Automated proposal execution
- Multi-signature administrative controls

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.
