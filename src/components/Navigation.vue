<template>
  <header>
    <div class="logo">
      <img alt="An incredibly handsome red-bearded developer." src="/jaredsm.jpg" />
      <div class="logo-text">
        Jared Leach
      </div>
    </div>
    <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/skills">Skills</RouterLink>
        <RouterLink to="/education">Education</RouterLink>
<!--        <RouterLink to="/about">Experience</RouterLink>-->
        <RouterLink to="/notes">Notes</RouterLink>
    </nav>
  </header>
</template>

<style scoped>
@media (min-width: 1024px) {
  header {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    max-width: 1024px;
    margin-left: auto;
    margin-right: auto;
  }

  .logo{
    margin-top: 1.5rem;
    display: flex;
    flex-direction: row;
    img{
      margin-left: 0.75rem;
      width: 50px;
      height: 50px;
      border-radius: 25px;
    }
    .logo-text{
      color: #555;
      padding: .2rem 1.5rem;
      text-decoration: none;
      font-size: 1rem;
      margin-top: 10px;
      font-weight: bold;
    }
  }

  nav {
    margin-top: 1.5rem;
    display: flex;
    flex-direction: row;
    margin-bottom: 3rem;
  }

  nav a.router-link-exact-active {
    border-bottom: 5px solid #1c9c78;
  }

  nav a {
    color: #555;
    padding: .4rem 1.1rem;
    text-decoration: none;
    font-size: 1rem;
    border-bottom: 5px solid #FFF;
  }

  nav a:last-child {
    border-right: none;
  }

  nav a:hover{
    border-bottom: 5px solid #DDD;
  }
}


@media (max-width: 1023px) {
  header {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    margin-left: auto;
    margin-right: auto;
  }
  .logo{
    display: block;
    text-align: center;
    padding: 1.5rem 0;
    img{
      width: 75px;
      height: 75px;
      border-radius: 40px;
      margin-left: auto;
      margin-right: auto;
    }
    .logo-text{
      color: #1c9c78;
      font-family: 'Crete Round', serif;
      padding: .1rem 0;
      text-decoration: none;
      font-size: 1.5rem;
      font-weight: bold;
    }
  }

  nav {
    margin-top: 0.5rem;
    display: flex;
    flex-direction: row;
    margin-bottom: 3rem;
    justify-content: space-between;
    padding: 0 1.5rem;
  }

  nav a.router-link-exact-active {
    border-bottom: 3px solid #1c9c78;
  }

  nav a {
    color: #555;
    padding: .4rem 0;
    text-decoration: none;
    font-size: 0.9rem;
    border-bottom: 3px solid #FFF;
  }

  nav a:last-child {
    border-right: none;
  }

  nav a:hover{
    border-bottom: 3px solid #DDD;
  }
}





</style>
