<template>
  <div class="messages-section">
  <div class="messages-section-header">
    <p>Employee Leaderboard</p>
  </div>
  <div class="messages">
    <div v-for="(employee, index) in leaderboard" :key="employee.id" class="message-box">
      <img src="https://images.unsplash.com/photo-1438761681033-6461ffad8d80?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=2550&q=80" alt="profile image">
      <div class="message-content">
        <div class="message-header">
          <div class="name">{{index + 1}} - {{ employee.username }}</div>
          <div class="star-checkbox">
            <input type="checkbox" id="star-1">
            <label for="star-1">
              <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-star">
                <polygon points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2" /></svg>
            </label>
          </div>
        </div>
        <p class="message-line">
          {{ employee.totalCo2Saved }} KCo2 saved this month
        </p>
      </div>
    </div>
    
  </div>
</div>
</template>

<script setup>
const leaderboard = ref([
  { id: 1, username: 'JohnDoe', totalCo2Saved: 120 },
  { id: 2, username: 'JaneSmith', totalCo2Saved: 90 },
  { id: 3, username: 'AlexJohnson', totalCo2Saved: 70 },
  { id: 4, username: 'EmilyBrown', totalCo2Saved: 110 },
  { id: 5, username: 'MikeWilliams', totalCo2Saved: 85 },
  // Add more leaderboard data as needed
]);

</script>
