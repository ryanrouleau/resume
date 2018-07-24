<template>
  <div id="app">
    <header>
      <h1>Ryan Rouleau</h1>
      <h2>An Aspiring Full Stack Developer</h2>
      <div class="contact">
        <ul>
          <li>
              ryan@ryanrouleau.com
          </li>
          <li>
              (484) 599 2539
          </li>
          <li>
              github.com/ryanrouleau
          </li>
        </ul>
      </div>
      <!-- <div class="seperator"></div> -->
    </header>

    <resume-section>
      <span slot="section-header">Education</span>
      <div slot="sub-sections">
        <sub-section>
          <span slot="sub-section-header">University of Colorado - Boulder</span>
          <span slot="dates">Aug 2015 - May 2019</span>
          <ul slot="bullets">
            <li>
              B.S. Computer Science - <span class="bold">GPA: 3.78</span>
            </li>
            <li>
              <span class="bold italic">Coursework -</span> Machine Learning, Big Data Architecture, Intro to AI, Data Science, Data Mining, Object Oriented Design, Programming Languages, Database System,  Algorithms, Software Dev, Numerical Computation, Computer Systems
            </li>
          </ul>
        </sub-section>
      </div>
    </resume-section>

    <resume-section>
      <span slot="section-header">Experience</span>
      <div slot="sub-sections">
        <sub-section>
          <span slot="sub-section-header">CA Technologies (formerly Rally Software)</span>
          <span slot="dates">June 2018 - Present</span>
          <ul slot="bullets">
            <li>
              <span class="bold">Software Engineering Intern</span>
            </li>
            <li>
              Contributed in developing new features and fixing defects with heavy collaboration with other devs. React.
            </li>
          </ul>
        </sub-section>
        <sub-section>
          <span slot="sub-section-header">Laboratory for Atmospheric and Space Physics (LASP)</span>
          <span slot="dates">May 2017 - May 2018</span>
          <ul slot="bullets">
            <li>
              <span class="bold">Undergrad Software Engineer</span>
            </li>
            <li>
              Developed, maintained, and supported software for the ground operations of several NASA missions and spacecraft. Mostly Python & C++
            </li>
            <li>
              Worked with users, and managers to define features and deliver quality software on agreed upon schedules
            </li>
          </ul>
        </sub-section>
        <sub-section>
          <span slot="sub-section-header">CU Boulder Computer Science Department</span>
          <span slot="dates">Jan 2017 - May 2017</span>
          <ul slot="bullets">
            <li>
              <span class="bold">Course Assistant: Data Structures</span>
            </li>
            <li>
              Worked closely with struggling students to improve their understanding of Data Structures course material, concepts, and projects.  Improved, understood, and debugged large amounts of C++ code
            </li>
          </ul>
        </sub-section>
      </div>
    </resume-section>

    <resume-section>
      <span slot="section-header">Notable Personal Projects, &nbsp;<span class="fade" style="font-weight:700;font-size:18px;">github.com/ryanrouleau</span></span>
      <div slot="sub-sections">
        <sub-section>
          <span slot="sub-section-header">Dwllr</span>
          <span slot="dates">Jan 2018 - May 2018</span>
          <ul slot="bullets">
            <li>
              A tool gathering huge amounts of data on every zip code in the US, and utilizing machine learning to aid in determining and recommending cities that fit you best
            </li>
            <li>
              Responsible for defining Machine Learning model and designing & engineering the Vue.js frontend.  Utilized Google Maps API, our custom API and (tons of) performant animations
            </li>
          </ul>
        </sub-section>
        <sub-section>
          <span slot="sub-section-header">Song Serve</span>
          <span slot="dates">Jul 2017 - Aug 2017</span>
          <ul slot="bullets">
            <li>
              A node.js app for creating and serving a music library from mp3 files on a user's machine (utilizing Spotify's API)
            </li>
            <li>
              Designed and implemented a RESTful API to interact with server
            </li>
            <li>
              Used API to develop a fully featured browser based music player and library viewer w/ Vue.js & webpack
            </li>
          </ul>
        </sub-section>
        <sub-section>
          <span slot="sub-section-header">OBD Buddy, &nbsp;<span class="fade">Winner at HackCU 2017</span></span>
          <span slot="dates">Apr 2017</span>
          <ul slot="bullets">
            <li>
              A full stack app developed w/ a team that streams on board diagnostics data from a car to a server
            </li>
            <li>
              Uses stream to give contextual info to a user (e.g. auto reroute guidance to gas station when gas gets too low)
            </li>
          </ul>
        </sub-section>
        <sub-section>
          <span slot="sub-section-header">TheCryptoTicker.com</span>
          <span slot="dates">Nov 2016</span>
          <ul slot="bullets">
            <li>
              Interface displaying real time trading data on all currencies (~90) listed on the cryptocurrency exchange poloniex
            </li>
            <li>
              Utilizes websockets to deliver updates to user as fast as possible
            </li>
          </ul>
        </sub-section>
      </div>
    </resume-section>

    <resume-section>
      <span slot="section-header">Technical Skills</span>
      <div slot="sub-sections">
        <sub-section :show-seperator="false">
          <ul id="ulscope" slot="bullets" style="padding-top:8px; padding-bottom: 6px;">
            <li >
              <span class="bold italic">Languages -</span> JavaScript (experienced), Python (experienced), C++, SQL, some Scala
            </li>
            <li>
              <span class="bold italic">Notable Tools & Frameworks -</span> React, Vue, Node, express.js, webpack, git, Jupyter & related Machine Learning tools
            </li>
            <li>
              <span class="bold italic">Other -</span> Eagle Scout
            </li>
          </ul>
        </sub-section>
      </div>
    </resume-section>
<!--
    <div class="designed">
      Designed by me
    </div>
-->
 </div>
</template>

<script>
import ResumeSection from './ResumeSection.vue'
import SubSection from './SubSection.vue';
export default {
  name: 'app',
  data () {
    return {
    }
  },
  components: {
    ResumeSection,
    SubSection
  }
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css?family=Raleway:400,700,800,900');
@import url('https://fonts.googleapis.com/css?family=Open+Sans:400,400i,700,700i,800');
#ulscope {
    margin-bottom: 0px !important;
}
#app {
  font-family: 'Open Sans';
  position: relative;
  width: 819px;
  //height: 1060px;
  overflow-y: hidden;
  background: #f2f2f2;
  border: 1px solid rgba(0,0,0,0.3);
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;

  * {
    box-sizing: border-box;
    -webkit-print-color-adjust:exact;
-webkit-filter:opacity(1);
  }
}
.designed {
  position: absolute;
  bottom: 0;
  right: 0;
  font-size: 9px;
  margin-bottom: 3px;
  margin-right: 28px;
  color: rgba(0,0,0,0.8)
}
.bold {
  font-weight: bold;
}
.italic {
  font-style: italic;
}
header {
  position: relative;
  height: 100px;
  width: 100%;
  background: #fff;
  padding-left: 35px;
  box-shadow: 0px 0px 30px 0px rgba(0, 0, 0, 0.08), 0px 3px 2px 0px rgba(0, 0, 0, 0.05);
  h1 {
    position: absolute;
    font-family: 'Raleway';
    margin-top: 12px;
    font-weight: 900;
    font-size: 40px;
    color: rgba(0,0,0,0.85);
    //background: linear-gradient(150deg, rgba(0,0,0,0.5), rgba(0,0,0,0.9));
    //-webkit-background-clip: text;
    //-webkit-text-fill-color: transparent;
    text-shadow: 2px 2px 8px rgba(0,0,0,0.08);
    .fade {
      font-weight: 800;
      color: rgba(0,0,0,0.6);
    }
  }
  h2 {
    position: absolute;
    bottom: 0;
    margin-bottom: 13px;
    margin-left: 7px;
    font-size: 16px;
    color: rgba(0,0,0,0.7);
    .fade {
      //color: rgba(0,0,0,0.6);
    }
  }
  .contact {
    position: absolute;
    right: 0;
    margin-top: -3px;
    padding-right: 30px;
    text-align: right;
    font-weight: 600;
    color: rgba(0,0,0,0.7);
    font-size: 16px;
    li {
      padding-bottom: 4px;
      list-style: none;
    }
  }
  .seperator {
    position: absolute;
    width: 2px;
    height: 54px;
    margin-top: 23px;
    border-radius: 2px;
    margin-left: 525px;
    background: rgba(0,0,0,0.15);
  }
}
.fade {
  color: rgba(0,0,0,0.6);
}

</style>
