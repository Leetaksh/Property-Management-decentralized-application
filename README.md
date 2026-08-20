## Property-Management-decentralized-application
# Core Features 
1. Property Listing   – Owner registers property with address, price per night, capacity   – Property stored on-chain with owner address
2. Booking System   – Renter selects property and date range   – Calculate total cost = nights × pricePerNight   – Create booking record on-chain with status (Pending, Confirmed, Completed)
3. Payment Handling   – Renter sends MATIC to contract for booking   – Contract holds payment in escrow   – Owner claims payment after rental completes
4. Frontend Interface (React)   – Browse available properties   – Connect wallet (MetaMask)   – Create booking with transaction confirmation   – View booking history

# Getting Started
Step 1: Design Smart Contract   struct Property {     address owner;
                                                      string location;                   
                                                      uint pricePerNight;      
                                                      bool isActive;   }   
                                 struct Booking {     uint propertyId;     
                                                      address renter;       
                                                      uint checkIn;       
                                                      uint checkOut;       
                                                      uint totalPrice;       
                                                      BookingState state;   }

Step 2: Implement Contract Functions   – listProperty() - owner registers property   
                                       – createBooking()  - renter initiates booking + sends payment     
                                       – confirmBooking() - owner confirms (optional)     
                                       – completeBooking() - mark rental as finished     
                                       – claimPayment() - owner withdraws funds

Step 3: Frontend Setup   – npx create-react-app property-dapp     
                         – Install ethers.js: npm install ethers     
                         – Create WalletConnect component (MetaMask) 

Step 4: Connect Contract to Frontend   – Create ABI from contract compilation     
                                       – Initialize ethers.Contract with ABI + address     
                                       – Implement property listing UI     
                                       – Build booking form with ethers.js transaction calls

Step 5: Test End-to-End   – Test on Polygon Mumbai testnet     
                          – Verify transaction confirmations in frontend

# How to Get Started For Each Project: 
1. Clone the GitHub template (link TBD)
2. Read the contract specification in /docs
3. Write tests first (TDD approach)
4. Implement contract functions to pass tests
5. Deploy to testnet
6. Record your explanation video
7. Submit via GitHub + link to deployment

# Checkpoints 
Project 1 (Wallet):   Week 1 (Day 1–3): Contract design review   Week 2 (Day 4–10): Testing & deployment   Week 3 (Day 11–15): Demo + presentationProject 2 (DAO):   Week 4 (Day 1–3): State machine & function signatures   Week 5 (Day 4–10): Implementation & tests   Week 6 (Day 11–15): Demo + documentationProject 3 (dApp):   Week 7 (Day 1–3): Contract + frontend scaffolding   Week 8–9 (Day 4–24): Full implementation   Week 10 (Day 25–35): Polish, deploy, demo 

# Resources 
Solidity Fundamentals:   • Solidity by Example (solidity-by-example.org)   • OpenZeppelin Contracts (github.com/OpenZeppelin/openzeppelin-contracts)Development Tools:   • Hardhat Docs (hardhat.org)   • ethers.js API Reference (docs.ethers.org)Testing & Deployment:   • Hardhat Testing Guide   • Polygon Docs for testnet setupReference Projects:   • Awesome Web3 Projects (GitHub)   • 100 Beginner Solidity Projects (GitHub) 
