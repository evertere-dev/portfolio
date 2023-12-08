<div id="socials-wrap">
  <div id="socials">
    <a href="https://dsc.bio/evertere" target="_blank"><img src="/src/images/icons/discord.svg" width="45" height="38px" alt="Discord Logo"></a>
    <a href="https://github.com/evertere-dev" target="_blank"><img src="/src/images/icons/github.svg" width="45" height="38px" alt="GitHub Logo"></a>
    <a href="https://www.linkedin.com/in/felix-schwendner-b58858208/" target="_blank"><img src="/src/images/icons/linkedin.svg" width="45px" height="38px" alt="LinkedIn Logo"></a>
   <a href="/contact"><img src="/src/images/icons/mail.svg" width="45" height="38px" alt="Contact Icon"></a>
  </div>
</div>

<style>
  #socials-wrap {
    position: fixed;
    text-align: center;
    bottom: 20px;
    left: 50%;
    transform: translateX(-50%);
    padding: 12px 20px;
    border: 2px solid #555555;
    background: #111111;
    border-radius: 18px;
  }

  #socials {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 25px;
  }

  #socials > a {
    display: block;
    height: 28px;
  }

  #socials > a:before {
    display: none;
  }

  #socials > a > img {
    transition: all .6s cubic-bezier(.47,2,.41,.8);
    filter: invert(1);
    height: 28px;
  }

  #socials > a:hover > img,
  #socials > a:focus > img {
    transform: translateY(1px);
  }
</style>