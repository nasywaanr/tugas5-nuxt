<template>
    <!-- BEGIN NAVBAR -->
  <div class="navbar">
      <a href="#about">About</a>
      <a href="#experience">Experience</a>
      <a href="#education">Education</a>
      <a href="#projects">Projects</a>
      <a href="#skills">Skills</a>
      <a href="#contact">Contact</a>
    </div>
    <!-- END NAVBAR -->

    <div class="container">

      <!-- HEADER -->
      <div class="jumbotron">
        <div class="jumbotron-text">
          <h1>Nasywa Nur Aini</h1>
          <p>D3 Brawijaya University</p>
        </div>
        <div class="jumbotron-social">
          <ul class="ul-social">
            <li class="li-social-links">
              <a class="social" href="https://github.com/nasywaanr" target="_blank"><i class="fa fa-github" aria-hidden="true"></i></a>
            </li>
            <li class="li-social-links">
              <a class="social" href="https://www.linkedin.com/in/nasywaa-nuraini-011480289?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app" target="_blank"><i class="fa fa-linkedin" aria-hidden="true"></i></a>
            </li>
          </ul>
        </div>
        <div id="down-arrow">
          <span><a href="#about"><i class="fa fa-chevron-down" aria-hidden="true"></i></a></span>
        </div>
      </div>
      <!-- END HEADER -->

      <!-- BEGIN ABOUT -->
      <div class="row white box-shadow">
        <div class="side-content"></div>
        <div class="main-content">
          <div class="content-header">
            <a class="anchor" name="about"></a>
            <h2>About</h2>
          </div>
          <div class="content-body">
            <p>Nama saya nasywa nur aini biasa dipanggil gendis, umur saya 19 tahun. Saya berasal dari gunung putri Bogor, Jawa Barat. Saya Mahasiswi Prodi Teknologi Informasi Universitas Brawijaya </p>
            <p>Saya suka memasak, tapi saya lebih suka makan. makanan yang paling saya sukai adalah pempek buatan mama saya dan seblak. Saya adalah pribadi yang ceria dan mudah bersosialisasi dengan orang lain.</p>
          </div>
        </div>
        <div class="side-content"></div>
      </div>
      <!-- END ABOUT -->

      <!-- BEGIN EXPERIENCE -->
      <div class="row">
        <div class="side-content"></div>
        <div class="main-content">
          <div class="content-header">
            <a class="anchor" name="experience"></a>
            <h2>Experience</h2>
          </div>
          <!-- CARD #1 -->
          <div class="content-body">
            <div class="card" v-for="experience in experiences">
              <div class="card-header">
                <h4>{{experience.company}} <span class="job-title">{{experience.job_title}}</span></h4>
              </div>
              <div class="card-content">
                <p>{{ experience.description }}</p>
              </div>
            </div>
          </div>
        </div>
        <div class="side-content"></div>
      </div>
      <!-- END EXPERIENCE -->

      <!-- BEGIN EDUCATION -->
      <div class="row white box-shadow">
        <div class="side-content"></div>
        <div class="main-content">
          <div class="content-header">
            <a class="anchor" name="education"></a>
            <h2>Education</h2>
          </div>
          <div class="content-body">

            <!-- EDUCATION DATA -->
            <div class="card" v-for="education in educations">
              <div class="card-header">
                <h4>{{education.name}} <span class="job-title">{{education.date_attended}}</span></h4>
              </div>
              <div class="card-content">
                <!-- baru deh disini dipanggil si description tadi --> 
                <p>{{ education.description }}</p>
              </div>
            </div>

          </div>
        </div>
        <div class="side-content"></div>
      </div>
      <!-- END EDUCATION -->

      <!-- BEGIN PROJECTS -->
      <div class="row">
        <div class="side-content-sm"></div>
        <div class="main-content-lg">
          <div class="content-header">
            <a class="anchor" name="projects"></a>
            <h2>Projects</h2>
          </div>
          <div class="content-body">
            <!-- CARD #1 -->
            <div class="project-card" v-for="project in projects">
              <div class="project-content">
                <h4>{{project.project_name}}</h4>
                <a :href="project.link">Project repository</a>
                <p></p>
              </div>
            </div>
          </div>
        </div>
        <div class="side-content-sm"></div>
      </div>
      <!-- END PROJECTS -->

      <!-- BEGIN SKILLS -->
      <div class="row white box-shadow">
        <div class="side-content"></div>
        <div class="main-content">
          <div class="content-header">
            <a class="anchor" name="skills"></a>
            <h2>Skills</h2>
          </div>
          <div class="content-body">
            <ul class="ul-skills">
              <li class="li-skills" v-for="skill in skills">{{ skill }}</li>
            </ul>
          </div>
        </div>
        <div class="side-content"></div>
      </div>
      <!-- END SKILLS -->

      <!-- BEGIN FOOTER -->
      <div class="row">
        <div class="side-content"></div>
        <div class="main-content">
          <div class="content-header">
          </div>
          <div class="content-body">
            <p>Copyright Nasywa 2017</p>
          </div>
        </div>
        <div class="side-content"></div>
      </div>
      <!-- END FOOTER -->
    </div>
</template>
<style>
@import url("~/assets/style.css");
</style>

<script>
export default {
  data(){
    return{
      // Data Personal
      skills: ["HTML", "Javascript", "PHP", "Laravel", "Python"],

      educations: [
        {name: "Universitas Brawijaya", date_attended:"2023 - Now", description:"Saya mahasiswi Prodi Teknologi Informasi Fakultas Vokasi Universitas Brawijaya "},
        {name: "SMKN 1 GUNUNG PUTRI", date_attended:"2020 - 2023", description:"Saya Lulusan Rekayasa Perangkat Lunak di SMKN 1 GUNUNG PUTRI kab. Bogor Jawa Barat"}, 
      ],

      experiences: [
        {company: "PT. Restu Agung Narogong", job_title: " Staff Administrasi,Keuangan", description:" Saya Magang selama 2 Bulan di PT restu agunng narogong dan berpindah job dalam sebulan sekali bersama partner saya "},
        {company: "SMKN 1 GUNUNG PUTRI", job_title: " Sharing Session", description:" Saya menjadi pembicara pada acara sharing session di smk saya dan berkesempatan berada di panggung bersama tokoh-tokoh penting masyarakat"},
      ],

      projects: [
        {project_name: "Color change, Increment, Carousel using Vue JS", description: "", link: "https://github.com/nasywaanr/tugas-vue"},
        {project_name: "Contactform using PHP", description: "", link: "https://github.com/nasywaanr/contactform"},
      ]
    }
  }
}
</script>