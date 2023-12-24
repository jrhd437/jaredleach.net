<template>
  <div class="skills">
    <h1>Education</h1>

    <EduAwardView
        title="AAS, Web Development Technology"
        year="2011"
        image="rsc.jpg"
        institution="Rose State College"
        description="Included classes covering: PHP, JavaScript, JAVA OOP, XHTML/CSS, Multimedia, Advanced Photoshop, Cyber Security,
      Marketing, and general education."
    />

    <EduAwardView
        title="BS, Comp. Science &amp; Business"
        year="2021"
        image="lu.jpg"
        institution="Liberty University"
        description="Included classes covering: Relational Databases, Node Runtime, Object-Oriented Programming, Business Communication,
        Entrepreneurship, and more.."
    />

    <EduAwardView
        title="Security+"
        year="2022"
        image="sp.jpg"
        institution="CompTIA"
        description="CompTIA 601, Security Plus Certification."
    />

    <EduAwardView
        title="MA, Theological Studies"
        year="2024"
        image="lud.jpg"
        institution="Liberty Divinity School"
        description="Included classes covering: Systematic Theology, Hermeneutics, Old Testament, New Testament, Koine Greek,
        Classical Hebrew, and more."
    />
    
  </div>
</template>

<script setup>
import EduAwardView from "@/components/EduAwardView.vue";
</script>