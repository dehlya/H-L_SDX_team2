<script setup>
import { ref, onMounted } from 'vue';
import { useRoute } from 'vue-router';
import AddCommuteRecord from '~/components/AddCommutingRecord.vue';

const recipient = ref(null);
const tokens = ref(1);
const route = useRoute();
const employee = ref(null);

// get employee data (demo purposes only)
onMounted(() => {

    if (route && route.query && route.query.employeeData) {
        const employeeData = JSON.parse(route.query.employeeData);
        if (employeeData) {
            employee.value = employeeData;
        }
    }
  
});

const colleagues = ref([
  { id: 1, username: 'JohnDoe' },
  { id: 2, username: 'JaneSmith' },
  { id: 3, username: 'AlexJohnson' },
  { id: 4, username: 'EmilyBrown' },
  { id: 5, username: 'MikeWilliams' },
  { id: 6, username: 'AmandaTaylor' },
  { id: 7, username: 'ChrisMartinez' },
  { id: 8, username: 'SophieClark' },
  // Add more colleagues as needed
]);


const sendTokens = () => {
  // Simulate sending tokens (replace with actual logic)
  // Update employee tokens directly
  employee.tokens -= tokens.value;

  // Clear the form
  recipient.value = null;
  tokens.value = 1;

  alert('Tokens sent successfully!');
};

</script>

<template>
  <div v-if="employee">
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
                    
                </div>
            </div>
            </div>            
        </div>
        <div class="login-section">
            <div class="login-section-header">
                <p>Log a commute</p>
            </div>
        </div>
        <div class="login-section">
            <div class="login-section-header">
                <p>Create transaction</p>
            </div>
        </div>
    </div>
  </div>
  <Leaderboard/>
</template>

