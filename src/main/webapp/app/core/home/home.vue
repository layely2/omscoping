<template>
  <div class="home row">
    <div class="col-md-3">
      <span class="hipster img-fluid rounded"></span>
    </div>
    <div class="col-md-9">
      <h4 class="display-5" v-text="t$('home.title')"></h4>
      <!--p class="lead" v-text="t$('home.subtitle')"></p-->
      <div>
        <form>
          <span class="col-md-12">
            <span class="col-md-3"> <h5>Money Transfer</h5></span>
            <span class="col-md-3">MSISDN:</span>
            <span class="col-md-3">
              <input type="text" class="col-md-3" />
            </span>
            <span class="col-md-3">Amount:</span>
            <span class="col-md-3">
              <input type="text" class="col-md-3" />
            </span>
            <span class="col-md-1">
              <input type="submit" value="Send" disabled />
            </span>
          </span>
        </form>
        <br />
        <br />
      </div>
      <div>
        <div>
          <img class="col-md-6" src="../../../../resources/IMG-20240524-WA0013.jpeg" />
          <img class="col-md-6" src="../../../../resources/IMG-20240524-WA0015.jpeg" />
        </div>
        <br />
        <div>
          <img class="col-md-6" src="../../../../resources/IMG-20240522-WA0030.jpeg" />
          <img class="col-md-6" src="../../../../resources/IMG-20240522-WA0032.jpeg" />
        </div>
        <br />
        <div>
          <img class="col-md-6" src="../../../../resources/IMG-20240522-WA0034.jpeg" />
          <img class="col-md-6" src="../../../../resources/IMG-20240522-WA0038.jpeg" />
        </div>
        <br />
        <div>
          <img class="col-md-12" src="../../../../resources/IMG-20240522-WA0042.jpg" />
        </div>
      </div>
      <div>
        <div class="alert alert-success" v-if="authenticated">
          <span v-if="username" v-text="t$('home.logged.message', { username: username })"></span>
        </div>

        <div class="alert alert-warning" v-if="!authenticated">
          <span v-text="t$('global.messages.info.authenticated.prefix')"></span>
          <a class="alert-link" v-on:click="openLogin()" v-text="t$('global.messages.info.authenticated.link')"></a
          ><span v-html="t$('global.messages.info.authenticated.suffix')"></span>
        </div>
        <div class="alert alert-warning" v-if="!authenticated">
          <span v-text="t$('global.messages.info.register.noaccount')"></span>&nbsp;
          <router-link class="alert-link" to="/register" v-text="t$('global.messages.info.register.link')"></router-link>
        </div>
      </div>

      <p v-text="t$('home.question')"></p>

      <ul>
        <li><a href="https://www.orange.fr/" target="_blank" rel="noopener noreferrer" v-text="t$('home.link.homepage')"></a></li>
        <li>
          <a href="https://www.orange.fr/" target="_blank" rel="noopener noreferrer" v-text="t$('home.link.stackoverflow')"></a>
        </li>
        <li>
          <a href="https://www.orange.fr/" target="_blank" rel="noopener noreferrer" v-text="t$('home.link.bugtracker')"></a>
        </li>
        <li>
          <a href="https://www.orange.fr/" target="_blank" rel="noopener noreferrer" v-text="t$('home.link.chat')"></a>
        </li>
        <li>
          <a href="https://www.orange.fr/" target="_blank" rel="noopener noreferrer" v-text="t$('home.link.follow')"></a>
        </li>
      </ul>

      <p>
        <span v-text="t$('home.like')"></span>
        <a href="https://www.orange.fr/" target="_blank" rel="noopener noreferrer" v-text="t$('home.github')"></a>!
      </p>
    </div>
  </div>
</template>

<script lang="ts" src="./home.component.ts"></script>
