# GreenBits

## Description

Project created during the [Hack'n'Lead Hackaton](https://www.womenplusplus.ch/hackandlead).
It concerns the challenge proposed by SDX.

This is an app built on Nuxt.js, allowing companies to encourage their employees in making sustainable choices with a gamification system based on Tokens and the Ethereum blockchain.

## Table of Contents

- [App Overview](#overview)
- [Features](#features)
- [Demo](#demo)
- [Installation](#installation)


## Overview

GreenBits is a cutting-edge web application designed to foster sustainability and environmental consciousness within workplace environments. 
The platform introduces a unique blend of environmental responsibility, health promotion, and teambuilding, offering a holistic approach to corporate well-being.

### Goals:

1. **Reducing Carbon Emissions**: GreenBits aims to significantly decrease the company's carbon footprint by encouraging employees to adopt eco-friendly commuting habits, such as walking or car-sharing.
2. **Improving Employee Health**: Beyond environmental impact, the program focuses on enhancing the health and well-being of employees, promoting physical activity and stress reduction.
3. **General Environmental Impact**: By fostering a culture of sustainability, GreenBits contributes to the broader goal of reducing carbon emissions and creating a positive impact on the environment.
4. **Teambuilding**: The platform facilitates teambuilding through activities like small group walks or car-sharing, fostering collaboration and camaraderie among colleagues.

### Implementation:

1. **Leaderboards and Integration**: GreenBits features dynamic leaderboards, seamlessly integrated into ERP profiles and communication channels, enhancing visibility and engagement.
2. **Improvement Graphs**: Employees can track their commuting habits over time through interactive improvement graphs, providing insights into their environmental contributions.
3. **Innovative Rewards**: The platform introduces innovative rewards for participants, such as:
   - Days Off: Rewarding sustainable actions with additional days off, ensuring a positive impact without harming the environment.
   - Sports Coupons: Promoting a healthy lifestyle, employees can redeem sports coupons for fitness activities or wellness services.
   - Contribution to Travel Expenses: Offering financial incentives by contributing to travel expenses, supporting green modes of transportation like public transit, biking, or e-scooters.
4. **Recognition Initiatives**: GreenBits celebrates achievements through initiatives like "Employee of the Month" LinkedIn posts, acknowledging and promoting sustainability champions.
   
GreenBits is a transformative platform that aligns corporate values with individual well-being and environmental stewardship. 
Join us in creating a workplace where sustainability, health, and teamwork converge for a brighter future.


### Interest for companies
GreenBits isn't just a platform; it's a catalyst for transforming workplaces into sustainable ecosystems. 
By adopting GreenBits, companies can:

1. **Boost Employee Engagement:**
   Encourage a sense of purpose and community among employees by aligning corporate values with sustainable practices.

2. **Enhance Corporate Responsibility:**
   Demonstrate a commitment to environmental stewardship, contributing to a positive corporate image and attracting socially conscious talent.

3. **Drive Green Initiatives:**
   Empower employees to actively participate in eco-friendly initiatives, reducing the company's carbon footprint and contributing to a healthier planet.

4. **Foster Healthy Competition:**
   Implement gamification strategies to cultivate a competitive yet collaborative atmosphere, inspiring employees to outperform in sustainability efforts.

5. **Improve Workplace Morale and Well-being:**
   Celebrate and recognize employees for their contributions, creating a positive work environment that boosts morale and job satisfaction.
   By going to work by bike or foot, the employees also improve their health and well-being, leading to a more vibrant and fulfilling lifestyle.
   
7. **Gain a competitive Advantage**:
   - Recruitment and Retention: Offering innovative and socially responsible benefits can attract and retain top talent, especially among individuals who prioritize companies with a strong commitment to sustainability.
   - Differentiation in the Market: Implementing a blockchain-based system adds a technological edge, differentiating the company from competitors and showcasing innovation.
     
8. **Get Data-Driven Insights**:
   The data collected from the blockchain can provide valuable insights into commuting patterns, allowing companies to make informed decisions about policies, rewards, and resource allocation.

## Blockchain
GreenBits seamlessly integrates blockchain for a host of advantages that elevate your company's sustainability initiatives.
Its based on the Ethereum Blockchain because of its reputation of the most sustainable blockchain.

Here's why we use the blockchain technology:
1. **Immutability**:
   - Data Integrity: Transactions recorded on the blockchain are highly resistant to tampering. Once data is added to a block and confirmed by the network, it becomes part of a permanent and unchangeable record. This ensures the integrity of the data, particularly important for maintaining the credibility of sustainability-related transactions.
     
2. **Transparency**:
   - Visibility and Trust: Blockchain transactions are transparent and can be audited by participants. This transparency fosters trust among employees, employers, and any external parties involved. It's particularly beneficial when showcasing the company's commitment to sustainability to customers, investors, or regulatory bodies.
     
3. **Decentralization**:
   - Trustless Transactions: Blockchain operates on a decentralized network, eliminating the need for a central authority. This decentralized nature allows for trustless transactions, reducing the dependence on intermediaries and ensuring that the system is not controlled by a single entity.
     
4. **Smart Contracts**:
   - Automated Execution: Smart contracts, self-executing contracts with the terms of the agreement directly written into code, can automate the execution of reward transactions based on predefined conditions. This reduces the need for manual intervention and ensures that transactions are executed as intended.
     
5. **Security**:
   - Resilience to Attacks: Blockchain technology employs cryptographic techniques that make it resistant to various types of cyber attacks. This enhances the security of the system, especially when dealing with sensitive information and transactions related to sustainability and employee rewards.

6. **Traceability**:
  - Auditable History: The entire transaction history is traceable on the blockchain. This feature is beneficial for auditing purposes, allowing companies to track the flow of tokens, rewards, and sustainability-related transactions over time.


## Features
Key Features:
1. Employee Dashboard:
Personalized dashboards for each employee, showcasing key metrics like token balance, carbon savings, and pending transactions.
2. Gamification:
Gamification elements, including token rewards and leaderboard rankings, make sustainability efforts enjoyable and rewarding.
3. Transactions:
Employees can utilize their earned tokens to make transactions with their coworkers, against services or as gifts.
4. Marketplace:
Employees have the possibility to exchange their tokens. The exchange possibilities are defined by the employer. Some recommandations include Public transportation tickets, gym coupons or days off.
5. Leaderboard:
A dynamic leaderboard ranks employees based on their CO2 savings, fostering friendly competition and recognizing top contributors.
6. Visibility:
The app is made to be included in the company's website. This allows them to show their engagement in sustainable actions. 


## Demo

### Prototype
The prototyping and workflow can be consulted [here](https://www.figma.com/proto/xnfmwgEo40esXbiGRnU5rz/Powerpuffs?type=design&node-id=104-2954&t=GV0BBNr1U1Ixblbn-0&scaling=contain&page-id=0%3A1&starting-point-node-id=104%3A2954).


### Current State
The current application can be consulted [here](https://h-l-sdx-team2.vercel.app/).
This demo version includes the login, in case you want to try it, here is a temporary login : 
- username: "JohnDoe"
- password: "john123"
  

**Homepage**:

![Homepage](/public/Screenshot%20from%202023-11-12%2016-35-30.png)

**Login page**:

![Login](/public/Screenshot%20from%202023-11-12%2016-36-47.png)

**Employee Dashboard**:

![Employee Dashboard](/public/Screenshot%20from%202023-11-12%2016-37-26.png)


## Installation

Setup : 
```bash
# Clone the repository
git clone https://github.com/dehlya/H-L_SDX_team2.git

# Navigate to the project directory
cd H-L_SDX_team2

# Install dependencies
npm install

## Development Server

Start the development server on `http://localhost:3000`:

```bash
# npm
npm run dev

# yarn
yarn dev

```

## Production

Build the application for production:

```bash
# npm
npm run build

# yarn
yarn build

```
