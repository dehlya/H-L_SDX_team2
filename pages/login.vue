<script setup>

import { ref } from 'vue';

const isLoggedIn = ref(false);
const username = ref('');
const password = ref('');
const employee = ref(null);

// Demo data for employee profiles
const employeeProfiles = [
  { id: 1, username: 'JohnDoe', password: 'john123', tokens: 120, co2Saved: 1500 },
  { id: 2, username: 'JaneSmith', password: 'jane456', tokens: 90, co2Saved: 1100 },
  { id: 3, username: 'AlexJohnson', password: 'alex789', tokens: 70, co2Saved: 950 },
  { id: 4, username: 'EmilyBrown', password: 'emily234', tokens: 110, co2Saved: 1300 },
  { id: 5, username: 'MikeWilliams', password: 'mike567', tokens: 85, co2Saved: 1050 },
  { id: 6, username: 'AmandaTaylor', password: 'amanda890', tokens: 95, co2Saved: 1150 },
  { id: 7, username: 'ChrisMartinez', password: 'chris123', tokens: 75, co2Saved: 980 },
  { id: 8, username: 'SophieClark', password: 'sophie456', tokens: 100, co2Saved: 1200 },
  // Add more employee profiles as needed
];


const login = () => {
  const user = employeeProfiles.find((profile) => profile.username === username.value && profile.password === password.value);

  if (user) {
    isLoggedIn.value = true;
    employee.value = user;
} else {
    alert('Invalid username or password. Please try again.');
  }
};
</script>

<template>
    <div v-if="!isLoggedIn">
        <div class="login-section">
            <div class="login-section-header">
                <p>Log in</p>
            </div>
            <form @submit.prevent="login">
                <div class="login-section-line">
                    <div class="login-wrapper">
                        <input class="login-input" v-model="username" placeholder="Username">
                    </div>
                </div>
                <div class="login-section-line">
                    <div class="login-wrapper">
                        <input class="login-input" v-model="password" type="password" placeholder="Password">
                    </div>
                </div>
                <div class="login-section-line-button">
                    <button type="submit" class="btn">
                        Login
                    </button>
                </div>
            </form>
        </div>
    </div>

    <div v-else>
        <div class="employee-section">
            <div class="employee-section-header">
                <p>Welcome back !</p>
                <p class="time">{{ employee.username }}</p>
            </div>
            <div class="employee-boxes jsGridView">
                <div class="employee-box-wrapper">
                <div class="employee-box" style="background-color: #f0ffff;">
                    <div class="employee-box-header">
                    <span>Balance</span>
                    
                </div>
                <div class="employee-box-content-header">
                <p class="box-content-header">{{ employee.tokens }}</p>
                <p class="box-content-subheader">GreenBits</p>
                </div>
                <div class="box-progress-wrapper">
                      
                </div>
                <div class="employee-box-footer">
                    <NuxtLink :to="{ name: 'wallet', query: { employeeData: JSON.stringify(employee) } }">
                        <button class="btn">See wallet</button>
                    </NuxtLink> 
                </div>
            </div>
            </div>
            <div class="employee-box-wrapper">
                <div class="employee-box" style="background-color: #f0ffff;">
                    <div class="employee-box-header">
                    <span>Carbon</span>
                    
                </div>
                <div class="employee-box-content-header">
                <p class="box-content-header">{{ employee.co2Saved }}</p>
                <p class="box-content-subheader">kCo2 saved</p>
                </div>
                <div class="box-progress-wrapper">
                      
                </div>
                <div class="employee-box-footer">
                    <NuxtLink :to="{ name: 'wallet', query: { employeeData: JSON.stringify(employee) } }">
                        <button class="btn">Enter commuting</button>
                    </NuxtLink> 
                </div>
            </div>
            </div>
            <div class="employee-box-wrapper">
                <div class="employee-box" style="background-color: #f0ffff;">
                    <div class="employee-box-header">
                    <span>Transactions</span>
                    
                </div>
                <div class="employee-box-content-header">
                <p class="box-content-header">0</p>
                <p class="box-content-subheader">pending</p>
                </div>
                <div class="box-progress-wrapper">
                      
                </div>
                <div class="employee-box-footer">
                    <NuxtLink :to="{ name: 'wallet', query: { employeeData: JSON.stringify(employee) } }">
                        <button class="btn">See transactions</button>
                    </NuxtLink> 
                </div>
            </div>
            </div>            
        </div>
    </div>

        <Dashboard/> 
        </div>


    <Leaderboard/>
</template>
