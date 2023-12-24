<template>
  <article class="post skills">
    <h1>Skills</h1>
    <div class="skill-list">
        <h3>Languages</h3>
        <ul>
          <li>C#</li>
          <li>SQL</li>
          <li>JavaScript</li>
          <li>Go</li>
          <li>PHP</li>
          <li>HTML</li>
          <li>CSS</li>
          <li>Bash</li>
        </ul>
    </div>

    <div class="skill-list">
        <h3>Frameworks (Server)</h3>
        <ul>
            <li>ASP.NET MVC</li>
            <li>ASP.NET WebAPI</li>
            <li>ASP.NET Blazor</li>
            <li>ExpressJS</li>
            <li>Fiber</li>
            <li>FPDF</li>
        </ul>
    </div>

    <div class="skill-list">
        <h3>Frameworks (Client)</h3>
        <ul>
            <li>Vue</li>
            <li>ASP.NET Blazor WASM</li>
            <li>KnockoutJs</li>
        </ul>
    </div>

    <div class="skill-list">
      <h3>Databases</h3>
      <ul>
        <li>MySQL</li>
        <li>MariaDB</li>
        <li>PostgresSQL</li>
        <li>Microsoft SQL</li>
        <li>Oracle SQL</li>
        <li>SQLite</li>
      </ul>
    </div>

    <div class="skill-list">
      <h3>Applications</h3>
      <ul>
        <li>VS Code</li>
        <li>Visual Studio</li>
        <li>JetBrains Rider</li>
        <li>XCode</li>
        <li>NGinX</li>
        <li>Apache</li>
        <li>Adobe Photoshop</li>
        <li>Final Cut</li>
        <li>MacOS</li>
        <li>Linux</li>
        <li>Windows</li>
      </ul>
    </div>
    
  </article>
</template>

<style>
.skill-list{
  padding-left: 0.5rem;
  margin-bottom: 2.5rem;
  text-align: center;
}

.skill-list h3{
  font-size: 1.5rem;
  margin-bottom: 1.25rem;
  color: #1c9c78;
}

.skill-list ul{
  list-style-type: none;
}

.skill-list ul li{
  padding: 0.75rem 0rem;
  border-bottom: 1px dashed #1c9c78;
}
</style>
<script setup>
</script>