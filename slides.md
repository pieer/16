---
theme: seriph
fonts:
  sans: 'Bangers'
  mono: 'Open Sans'
background: null
class: 'text-center'
lineNumbers: false
clicks: 4
---

<Bubble :direction="$slidev.nav.clicks < 4 ? 'left' : 'right'">
<h2 v-if="$slidev.nav.clicks === 1" v-motion-slide-bottom>Ahoy!</h2>
<h2 v-if="$slidev.nav.clicks === 2" v-motion-slide-bottom>My name is <br/><strong class='text-4xl'>Pierre</strong></h2>
<h2 v-if="$slidev.nav.clicks === 3" v-motion-slide-bottom>I'm a frontend developer</h2>
<h2 v-if="$slidev.nav.clicks === 4" v-motion-slide-bottom>And I would like to work with you!</h2>
</Bubble>

<Face :chat="$slidev.nav.clicks"
      :style='$slidev.nav.clicks === 4 ? "transform: scaleX(-1); transform-origin: 50%;" : ""'/>

<div class="pt-12" v-if="$slidev.nav.clicks < 1">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="text-white bg-white bg-opacity-10">
    Press Space <carbon:arrow-right class="inline"/>
  </span>
</div>

<img
  v-if="$slidev.nav.clicks < 1"
  class="absolute -bottom-9 -left-7 w-80 opacity-50"
  src="https://sli.dev/assets/arrow-bottom-left.svg"
/>
<div v-if="$slidev.nav.clicks < 1" class="ft-2 absolute bottom-45 left-71 opacity-30 transform -rotate-42">Options here!</div>
---
theme: seriph
background: null
layout: two-cols
---

<h1 v-motion-slide-visible-left>What can I bring to the project?</h1>

<v-clicks>
<p v-motion-slide-visible-left><span class='opacity-50'>I'm glad you ask!</span></p>

<p v-motion-slide-visible-bottom><carbon:education class="inline-block mr-3"/>15 years of frontend and backend experience</p>
<p v-motion-slide-visible-bottom><carbon:touch-1-down class="inline-block mr-3"/>My passion for design, UX and animation</p>
<p v-motion-slide-visible-bottom><carbon:cognitive class="inline-block mr-3"/>My independent and pro-active attitude</p>
<p v-motion-slide-visible-bottom><carbon:events class="inline-block mr-3"/>An awesome team spirit</p>
<p v-motion-slide-visible-bottom><carbon:train-heart class="inline-block mr-3"/>My motivation to create the best UX!</p>
</v-clicks>

::right::
<img src="/scene-work.svg" class="-my-2" alt="Experience" v-motion-slide-visible-right/>

---
theme: seriph
background: null
layout: two-cols
---

<h1 v-motion-slide-visible-left>Skills</h1>

<v-clicks>
  <p v-motion-slide-visible-left><span class='opacity-50'>Where should I start...</span></p>

  <h3 class="opacity-100">Frontend</h3>
  <p v-motion-slide-visible-bottom>
    <carbon:arrow-right class="inline-block mr-3"/>
    SCSS, SASS, Stylus... Bootstrap, Windicss...
  </p>
  <p v-motion-slide-visible-bottom>
    <carbon:arrow-right class="inline-block mr-3"/>
    Vue 2 - 3, React, Polymer... Webpack... Axios...
  </p>

  <h3 class="opacity-100">Backend</h3>
  <p v-motion-slide-visible-bottom>
    <carbon:arrow-right class="inline-block mr-3"/>
    Nuxt, Laravel, Firebase...
  </p>
  <p v-motion-slide-visible-bottom>
    <carbon:arrow-right class="inline-block mr-3"/>
    Nginx, Google cloud, Cloudfare
  </p>

  <h3 class="opacity-100 mt-6">
    Ok, ok... I sniffed your technology stack...
    <carbon:face-wink class="inline-block mr-3"/>
  </h3>

  <h3 class="opacity-100">
    but honestly, I've worked with pretty much everything!
    <carbon:face-cool class="inline-block mr-3"/>
  </h3>

  <h3 class="opacity-100">
    And tested every single library!
    <carbon:rocket class="inline-block mr-3"/>
  </h3>
</v-clicks>

::right::
<img src="/scene-experience.svg" class="-my-2" alt="Experience" v-motion-slide-visible-right/>

---
theme: seriph
background: null
layout: full
class: 'text-center'
clicks: 2
---

<h1 v-motion-slide-top class="pb-4">Experience</h1>

<p v-if="$slidev.nav.clicks === 0" v-motion-slide-bottom class="max-w-screen-sm m-auto">
  For the past few years I've been working with Greg Pollack and Evan You to create the Vue Mastery website that teaches developers to use Vue.
</p>
<p v-if="$slidev.nav.clicks === 1" v-motion-slide-bottom class="max-w-screen-sm m-auto">
  I'm also an active developer on the project Group Income that is an efficient, fair, decentralized Basic Income system for everyone.
</p>
<p v-if="$slidev.nav.clicks === 2" v-motion-slide-bottom class="max-w-screen-sm m-auto">
  For 10 years I had the opprotunity to work with talented people in creative agencies and received few awards along the way.
</p>

<Carousel/>

---
theme: seriph
background: null
layout: two-cols
clicks: 4
---

<h1 v-motion-slide-top>Remote worker / traveler</h1>

<v-clicks>
  <p v-motion-slide-top>
    <span class='opacity-50'>Living my best life until...
    <span v-if="$slidev.nav.clicks > 0">you know <carbon:face-mask class="inline-block"/></span>
  </span>
  </p>
  <p>
    I've been working remotely for the past 5 years, learning along the way how to manage my time and fighting procrastination.
  </p>
  <p>
    I'm currently living in Koh Phangan, Thailand waiting for the world to open again.
  </p>
  <p>
    I developed here a great balance between work and personal life which boost my efficiency and productivity.
  </p>
</v-clicks>


::right::
<img v-if="$slidev.nav.clicks < 4" src="/scene-traveling.svg" class="-my-2" alt="Experience" v-motion-slide-visible-right/>
<img v-else src="/scene-relax.svg" class="-my-2" alt="Experience" v-motion-slide-visible-right/>

---
layout: center
class: text-center
---

# Learn More

[Email](mailto:schweiger.pierre@gmail.com) · [GitHub](https://github.com/pieer) · [Linkedin](https://www.linkedin.com/in/schweigerpierre/)
