# dVoting System Guide

## Table of Contents
1. [System Overview](#system-overview)
2. [Prerequisites](#prerequisites)
3. [User Roles](#user-roles)
4. [Admin Guide](#admin-guide)
5. [Voter Guide](#voter-guide)
6. [MetaMask Integration](#metamask-integration)
7. [System Workflow](#system-workflow)
8. [Technical Details](#technical-details)

## System Overview
dVoting is a decentralized voting system built on Ethereum blockchain technology. It provides a secure, transparent, and immutable way to conduct elections where votes cannot be altered once cast.

## Prerequisites
Before using the system, ensure you have:
- A modern web browser (Chrome, Firefox, or Edge recommended)
- MetaMask browser extension installed
- Sufficient ETH in your wallet for gas fees
- Stable internet connection

## User Roles

### 1. Admin
- Has full control over the election process
- Can initialize and end elections
- Manages voter verification
- Views election results
- Can only be one admin per election instance

### 2. Voter
- Can register to participate in elections
- Must be verified by admin
- Can cast one vote per election
- Can view election results after voting
- Cannot change their vote once cast

## Admin Guide

### Initial Setup
1. Install MetaMask and connect to the appropriate network
2. Deploy the smart contract using Truffle
3. Initialize the election with:
   - Election title
   - Candidate details
   - Election duration
   - Any specific rules

### During Election
1. Monitor voter registrations
2. Verify voter eligibility by checking:
   - Blockchain address
   - Name
   - Phone number
3. Approve or reject voter registrations
4. Monitor election progress
5. Can end election at any time

### Post Election
1. View final results
2. Generate election report
3. To start a new election:
   - Must deploy a new smart contract
   - Initialize new election instance
   - Cannot reuse previous contract

## Voter Guide

### Registration Process
1. Connect MetaMask wallet
2. Navigate to registration page
3. Provide required information:
   - Full name
   - Phone number
   - Ethereum address (auto-filled from MetaMask)
4. Submit registration
5. Wait for admin verification

### Voting Process
1. Ensure MetaMask is connected
2. Navigate to voting page
3. Select candidate
4. Confirm transaction in MetaMask
5. Wait for transaction confirmation
6. View confirmation of vote

### Viewing Results
1. Access results page
2. View:
   - Total votes cast
   - Individual candidate results
   - Winner announcement (if election ended)

## MetaMask Integration

### Setup
1. Install MetaMask browser extension
2. Create or import wallet
3. Connect to appropriate network:
   - Local: http://127.0.0.1:8545 (Chain ID: 1337)
   - Testnet/Production: As specified by admin

### Usage in dVoting
1. **Connection**
   - Click "Connect Wallet" button
   - Approve connection request in MetaMask
   - Ensure correct account is selected

2. **Transactions**
   - Registration: Requires gas fee
   - Voting: Requires gas fee
   - All transactions are permanent and immutable

3. **Security**
   - Never share private keys
   - Always verify transaction details
   - Keep MetaMask locked when not in use

## System Workflow

### 1. Election Initialization
1. Admin deploys smart contract
2. Sets up election parameters
3. Adds candidates
4. Starts election

### 2. Voter Registration
1. Voter connects wallet
2. Submits registration
3. Admin verifies details
4. Admin approves/rejects registration

### 3. Voting Phase
1. Approved voters connect wallet
2. Select candidate
3. Confirm transaction
4. Vote is recorded on blockchain

### 4. Election Conclusion
1. Admin ends election
2. Results are calculated
3. Results are displayed
4. New election requires new contract deployment

## Technical Details

### Smart Contract
- Written in Solidity
- Deployed on Ethereum network
- Handles:
  - Voter registration
  - Vote casting
  - Result calculation
  - Admin controls

### Security Features
- One vote per verified address
- Immutable vote records
- Admin-only controls for critical functions
- Transparent transaction history

### Gas Fees
- Required for all blockchain transactions
- Varies based on network congestion
- Paid in ETH
- Required for:
  - Registration
  - Voting
  - Admin operations

### Network Requirements
- Local Development:
  - Ganache CLI running
  - Port 8545 (default)
  - Chain ID: 1337
- Production:
  - As specified by deployment

## Important Notes
1. All transactions are permanent and cannot be reversed
2. Each election requires a new contract deployment
3. Gas fees are required for all transactions
4. Admin verification is mandatory for voting
5. Results are automatically calculated and cannot be manipulated
6. System requires MetaMask for all interactions
7. Network connection must be stable during transactions

## Troubleshooting
1. **MetaMask Connection Issues**
   - Ensure correct network is selected
   - Check if MetaMask is unlocked
   - Verify internet connection

2. **Transaction Failures**
   - Ensure sufficient ETH for gas
   - Check network congestion
   - Verify transaction parameters

3. **Registration Issues**
   - Verify all required information
   - Check if already registered
   - Ensure admin verification status

4. **Voting Issues**
   - Verify registration approval
   - Check if already voted
   - Ensure election is active

For additional support, join our Discord community: [discord.gg/3jmfdNsHWr](https://discord.gg/3jmfdNsHWr) 