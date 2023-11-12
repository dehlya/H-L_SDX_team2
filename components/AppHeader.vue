<template>
  <div class="app-header">
      <div class="app-header-left">
        <svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" viewBox="0 0 40 40" fill="none">
          <rect width="40" height="40" rx="8" fill="#0C0349"/>
          <path d="M23.1105 11.1954C23.1105 10.5579 23.1458 10.1066 23.2185 9.77966C23.2889 9.46289 23.3819 9.3202 23.46 9.24218C23.538 9.16417 23.6807 9.07112 23.9974 9.00072C24.3243 8.92807 24.7757 8.89275 25.4132 8.89275H28.647C29.2845 8.89275 29.7358 8.92807 30.0627 9.00072C30.3795 9.07112 30.5222 9.16417 30.6002 9.24218C30.6782 9.3202 30.7713 9.46289 30.8417 9.77966C30.9143 10.1066 30.9497 10.5579 30.9497 11.1954V14.4293C30.9497 15.0667 30.9143 15.5181 30.8417 15.845C30.7713 16.1617 30.6782 16.3044 30.6002 16.3825C30.5222 16.4605 30.3795 16.5535 30.0627 16.6239C29.7358 16.6966 29.2845 16.7319 28.647 16.7319H25.4132C24.7757 16.7319 24.3243 16.6966 23.9974 16.6239C23.6807 16.5535 23.538 16.4605 23.46 16.3825C23.3819 16.3044 23.2889 16.1617 23.2185 15.845C23.1458 15.5181 23.1105 15.0667 23.1105 14.4293V11.1954Z" stroke="white" stroke-width="1.78549"/>
          <g filter="url(#filter0_d_93_2489)">
            <path d="M8 16.0259C8 13.3946 8.56398 12.8306 11.1954 12.8306H14.4293C17.0606 12.8306 17.6246 13.3946 17.6246 16.0259V19.2598C17.6246 21.8912 17.0606 22.4552 14.4293 22.4552H11.1954C8.56398 22.4552 8 21.8912 8 19.2598V16.0259Z" fill="#00FFFF"/>
          </g>
          <path d="M19.3412 25.6451C19.3412 23.0137 19.9052 22.4497 22.5366 22.4497H25.7704C28.4018 22.4497 28.9658 23.0137 28.9658 25.6451V28.879C28.9658 31.5104 28.4018 32.0743 25.7704 32.0743H22.5366C19.9052 32.0743 19.3412 31.5104 19.3412 28.879V25.6451Z" fill="white"/>
          <defs>
            <filter id="filter0_d_93_2489" x="7.86774" y="12.8306" width="9.88915" height="9.88903" filterUnits="userSpaceOnUse" color-interpolation-filters="sRGB">
              <feFlood flood-opacity="0" result="BackgroundImageFix"/>
              <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha"/>
              <feOffset dy="0.132259"/>
              <feGaussianBlur stdDeviation="0.0661293"/>
              <feComposite in2="hardAlpha" operator="out"/>
              <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.25 0"/>
              <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_93_2489"/>
              <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_93_2489" result="shape"/>
            </filter>
          </defs>
        </svg>
        <p class="app-name">GreenBits</p>
      </div>
      <div class="app-header-right">
        <div v-if="!isLoggedIn">
          <NuxtLink to="/login">
            <button class="profile-btn">
              <span>Log in</span>
            </button>
          </NuxtLink>   
        </div>

        <div v-else>
            <button class="profile-btn">
              <img src="" />
              <span>Aybüke C.</span>
            </button>
        </div>
      </div>
  </div>
</template>