<!-- Home view -->

<template>
    <div class="home-container">
      <div class="home">
        <img src="@assets/corner-left.svg" alt="corner" class="top-left-corner" />
        <img src="@assets/corner-right.svg" alt="corner" class="bottom-right-corner" />
        <span class="font-white">
          I'm Cesar 
          <img src="@assets/master-ball.png" alt="logo" class="logo" />
        </span>
        <span class="font-violet">
          web developer
        </span>
        <span class="font-white">
          from Guatemala
        </span>
        <a class="button custom-btn" href="#">
          <!-- <i> -->
          <img src="@assets/icons/download.svg" alt="download" class="download-icon" />
          <!-- </i> -->
          &nbsp;
          <span class="font-white btn-text">
            Download my CV
          </span>
        </a>
      </div>
    </div>
  </template>
  
  <style scoped>
  
    .top-left-corner,
    .bottom-right-corner {
      position: absolute;
    }
  
    .top-left-corner {
      top: 22%;
      left: 22%;
    }
  
    .bottom-right-corner {
      bottom: 21%;
      right: 22%;
    }
  
    .home-container {
      display: flex;
      justify-content: center;
      align-items: center;
      height: calc(100vh - 100px);
    }
  
    .home {
      font-weight: 800;
      font-size: 96px;
      line-height: 112px;
      display: flex;
      flex-direction: column;
    }
  
    .logo {
      margin-bottom: -2%;
      width: 135px;
      height: 135px;
    }
  
    .custom-btn {
      width: 310px;
      height: 60px;
      display: flex;
      align-items: center;
      justify-content: center;
      background: #AD47FF;
      margin-top: 10px;
      text-transform: none;
    }
  
    .btn-text {
      font-size: 20px;
      line-height: 23px;
      font-weight: 700;
    }
  
    .download-icon {
      width: 18px;
      height: 18px;
    }
  
    @media (max-width: 1669px) {
      .top-left-corner {
        left: 20%;
      }
  
      .bottom-right-corner {
        right: 20%;
      }
    }
  
    @media (max-width: 1550px) {
      .top-left-corner {
        left: 16%;
      }
  
      .bottom-right-corner {
        right: 16%;
      }
    }
  
    @media (max-width: 1400px) {
      .top-left-corner {
        left: 12%;
      }
  
      .bottom-right-corner {
        right: 12%;
      }
    }
  
    @media (max-width: 1255px) {
      .top-left-corner {
        left: 8%;
      }
  
      .bottom-right-corner {
        right: 8%;
      }
    }
  
    @media (max-width: 1130px) {
      .top-left-corner {
        left: 4%;
      }
  
      .bottom-right-corner {
        right: 4%;
      }
    }
  
    @media (max-width: 1000px) {
      .top-left-corner,
      .bottom-right-corner {
        display: none;
      }
  
      .logo {
        width: 100px;
        height: 100px;
      }
    }
  
    @media (min-width: 600px) and (max-width: 700px) {
      .home {
        font-size: 64px;
        line-height: 72px;
      }
  
      .logo {
        width: 50px;
        height: 50px;
      }
    }
  
    @media (max-width: 600px) {
      .home {
        font-size: 48px;
        line-height: 56px;
      }
  
      .logo {
        width: 50px;
        height: 50px;
      }
    }
  
  </style>