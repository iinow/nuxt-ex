<template>
  <div class="layout">
    <div class="tabs">
      <ul>
        <li class="tab" :for="page" v-for="(page, index) in pages" :key="index">
          <input type="radio" :checked="index === 0" :name="pages" :id="page">
          <label :for="page">{{page}}</label>
          <div class="tabCon" v-for="(page, index) in contents" :key="index">
            {{page.content}}
          </div>
        </li>    
      </ul>
    </div>
    <!-- <div class="layout">
      <input name="nav" type="radio" class="nav home-radio" id="home" checked="checked" />
      <div class="page home-page">
        <div class="page-contents">
          <h1>Home</h1>
          <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quas voluptates dolore id aspernatur odit minus quidem deleniti ab rerum exercitationem dolores neque officiis explicabo possimus blanditiis sed, voluptatem ut. Ab?</p>
          <p>
            <label for="about">Learn more</label>
          </p>
        </div>
      </div>
      <label class="nav" for="home">
        <span>
          <svg
            viewBox="0 0 24 24"
            width="24"
            height="24"
            stroke="currentColor"
            stroke-width="2"
            fill="none"
            stroke-linecap="round"
            stroke-linejoin="round"
            class="css-i6dzq1"
          >
            <path d="M3 9l9-7 9 7v11a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z" />
            <polyline points="9 22 9 12 15 12 15 22" />
          </svg>
          Home
        </span>
      </label>

      <input name="nav" type="radio" class="about-radio" id="about" />
      <div class="page about-page">
        <div class="page-contents">
          <h1>About</h1>
          <p>Amet consectetur adipisicing elit. Sed ipsam ad exercitationem, quo quae ullam, quidem laudantium corporis quis minima debitis nesciunt repellat. Quos dolore ex quis voluptas, minus ut?</p>
        </div>
      </div>
      <label class="nav" for="about">
        <span>
          <svg
            viewBox="0 0 24 24"
            width="24"
            height="24"
            stroke="currentColor"
            stroke-width="2"
            fill="none"
            stroke-linecap="round"
            stroke-linejoin="round"
            class="css-i6dzq1"
          >
            <circle cx="12" cy="12" r="10" />
            <path d="M9.09 9a3 3 0 0 1 5.83 1c0 2-3 3-3 3" />
            <line x1="12" y1="17" x2="12" y2="17" />
          </svg>
          About
        </span>
      </label>

      <input name="nav" type="radio" class="contact-radio" id="contact" />
      <div class="page contact-page">
        <div class="page-contents">
          <h1>Contact</h1>
          <p>Eaque accusamus magnam error unde nam, atque provident omnis fugiat quam necessitatibus vel nulla sed quibusdam fuga veritatis assumenda alias quidem asperiores?</p>
          <p>
            <a href="#">Get in touch</a>
          </p>
        </div>
      </div>
      <label class="nav" for="contact">
        <span>
          <svg
            viewBox="0 0 24 24"
            width="24"
            height="24"
            stroke="currentColor"
            stroke-width="2"
            fill="none"
            stroke-linecap="round"
            stroke-linejoin="round"
            class="css-i6dzq1"
          >
            <path
              d="M21 11.5a8.38 8.38 0 0 1-.9 3.8 8.5 8.5 0 0 1-7.6 4.7 8.38 8.38 0 0 1-3.8-.9L3 21l1.9-5.7a8.38 8.38 0 0 1-.9-3.8 8.5 8.5 0 0 1 4.7-7.6 8.38 8.38 0 0 1 3.8-.9h.5a8.48 8.48 0 0 1 8 8v.5z"
            />
          </svg>
          Contact
        </span>
      </label>
    </div> -->
  </div>
</template>

<script>
export default {
  data () {
    return {
      pages: ['Home', 'About', 'Contact'],
      contents: [
        {
          name: 'Home',
          content: '여기가 홈이야'
        },
        {
          name: 'About',
          content: '여기가 어바웃이야'
        },
        {
          name: 'Contact',
          content: '여기가 컨텍트이야'
        }
      ]
    }
  }
}
</script>

<style>
.layout {
  height: auto;
}

* {
  font-family: "Work Sans", sans-serif;
}

.tabs {
  display: inline-block;
  margin: 0 auto;
  user-select: none;
}

.tabs ul li{
  display: inline-block;
  text-align: center;
  background-color: #f9f9f9;
  line-height: 40px;
  padding-left: 0px;
}

.tabs label {
  display: block;
  width: 100%;
  height: 40px;
  line-height: 40px;
}

.tabs input {
  display: none;
}

.tab label {
  padding: 10px 20px;
}

.tab {
  cursor: pointer;
}

.tabs .tab input:checked ~ label {
  background: #ccc;
}

.tabCon {
  display: none;
}

.tabs .tab input:checked ~ .tabCon {
  display: block;
}
</style>
