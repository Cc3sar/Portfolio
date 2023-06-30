<!-- Home view -->

<template>
    <div id="home-container">
      <div>
        <p class="font-white principal-text">
          I'm Cesar <img class="master-ball" src="@assets/master-ball.svg" alt="master ball" />
        </p>
        <p class="font-white principal-text">
          <span class="font-violet">full stack developer</span>
          from Guatemala.
        </p>
      </div>
    </div>
  </template>
  
  <style scoped>
    #home-container {
      display: flex;
      justify-content: center;
      align-items: center;
      height: calc(100vh - 100px);
    }
  
    .master-ball {
      width: 60px;
      height: 60px;
      margin-bottom: -10px;
    }
  </style>