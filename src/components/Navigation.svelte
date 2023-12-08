<header>
  <nav>
    <ul>
      <li><a href="/"><img src="/src/images/icons/home.svg" alt="Home"></a></li>
      <li><a href="/skills"><img src="/src/images/icons/work.svg" alt="Skills"></a></li>
      <li><a href="/contact"><img src="/src/images/icons/contact.svg" alt="Contact"></a></li>
    </ul>
  </nav>
</header>


<style>
  header {
    display: flex;
    justify-content: center;
    position: fixed;
    top: 20px;
    left: 50%;
    width: 100%;
    max-width: max-content;
    transform: translateX(-50%);
    border: 2px solid #555555;
    border-radius: 18px;
    background: #111111;
    padding: 10px 25px;
  
  }
  nav ul {
    display: flex;
    list-style-type: none;
    gap: 25px;
    padding: 0;
    margin: 0;
  }
  nav a {
    color: #ffffff;
    font-size: 1.5rem;
    display: block;
    width: 28px;
    height: 28px;
  }
  nav a:before {
    display: none;
  }
  nav a > img {
    filter: invert(1);
    width: 28px;
    height: 28px;
  }
  nav li {
    position: relative;
    transition: all .2s;
    font-size: 1rem;
  }
  nav li:hover,
  nav li:focus {
    transform: translateY(-1px);
  }
</style>