---
title: "Home"
---
<style>
html, body {
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100%;
  color: #fff;
  background: url('/img/background/image.png') no-repeat center center fixed;
  background-size: cover;
}
.home {
  text-align: center;
  padding: 0em 1em 6em 1em;
}
.home img {
  width: 700px;
  height: auto;
}
.home h1 {
  font-size: 4vw;
  font-weight: 800;
  margin-bottom: 20px;
}
.home h2 {
  font-size: 2.8vw;
  font-weight: 600;
  margin-bottom: 30px;
}
.home h3 {
  font-size: 1.8vw;
  font-weight: 400;
  margin-bottom: 50px;
}
.home h3 a {
  color: #ffd700;
  font-weight: 700;
  border-radius: 5px;
  transition: background-color 0.3s ease, color 0.3s ease;
  font-size: 1em;
}
.home h3 a:hover {
  color: #fff;
}
.home .buttons {
  margin-top: 30px;
  margin-bottom: 40px;
  display: flex;
  justify-content: center;
  gap: 2em;
}
.buttons a {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  padding: 1em 2em;
  width: 380px;
  height: 90px;
  border-radius: 15px;
  background: #5a67d8;
  color: #fff;
  text-decoration: none;
  font-size: clamp(16px, 1.4vw, 22px);
  font-weight: 600;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  transition: background 0.3s ease, transform 0.3s ease, box-shadow 0.3s ease;
  gap: 0.8em;
}
.buttons a i {
  font-size: 1.2em;
}
.buttons a:hover {
  background: #434190;
  transform: scale(1.05);
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.2);
}
.divider {
  width: 100%;
  max-width: 600px;
  height: 1px;
  background: linear-gradient(90deg,
    transparent,
    rgba(255, 255, 255, 0.2),
    transparent
  );
  margin: 3em auto;
}
.community-buttons {
  display: flex;
  justify-content: center;
  gap: 2em;
  max-width: 600px;
  margin: 0 auto;
}
.community-button {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  padding: 1em 2em;
  width: 280px;
  height: 90px;
  border-radius: 15px;
  background: rgba(255, 255, 255, 0.1);
  color: #fff;
  text-decoration: none;
  font-size: clamp(16px, 1.4vw, 22px);
  font-weight: 600;
  border: 1px solid rgba(255, 255, 255, 0.2);
  backdrop-filter: blur(5px);
  transition: all 0.3s ease;
  gap: 0.8em;
}
.community-button i {
  font-size: 1.2em;
}
.community-button:hover {
  background: rgba(255, 255, 255, 0.2);
  transform: scale(1.05);
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}
.cncf-banner {
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 30px 0;
  width: 100vw;
  margin-top: -5em;
  margin-bottom: 4em;
  margin-left: calc(-50vw + 50%);
  margin-right: calc(-50vw + 50%);
  position: relative;
}
.cncf-banner-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
}
.cncf-banner img {
  height: 50px;
  margin-bottom: 15px;
  filter: none;
}
.cncf-banner p {
  margin: 0;
  font-size: 18px;
  line-height: 1.4;
  color: #fff;
  text-align: center;
}
.cncf-banner a {
  color: #3EDCFF;
  text-decoration: none;
  transition: color 0.3s ease;
  font-weight: 500;
}
.cncf-banner a:hover {
  color: #fff;
  text-decoration: underline;
}
@media (max-width: 768px) {
  .cncf-banner {
    padding: 20px 0;
  }
  .cncf-banner-container {
    flex-direction: column;
    text-align: center;
  }
  .cncf-banner img {
    height: 42px;
    margin-bottom: 12px;
  }
  .cncf-banner p {
    font-size: 16px;
  }
}
footer {
  background: #333;
  padding: 2em 0;
  text-align: center;
  color: #fff;
}
footer a {
  color: #5a67d8;
  text-decoration: none;
}
@media (max-width: 768px) {
  .home h1, .home h2, .home h3, .buttons a {
    font-size: 5vw;
  }
  .home img {
    width: 85%;
  }
  .buttons {
    flex-direction: column;
    align-items: center;
  }
  .buttons a,
  .community-button {
    width: 80%;
    height: 50px;
    padding: 1em;
    font-size: 16px;
  }
  .community-buttons {
    flex-direction: column;
    align-items: center;
  }
  .community-button i {
    margin-right: 8px;
  }
}
</style>
<div class="home">
<img src="/img/logos/main-logo.svg" alt="Tokenetes Logo">
<h2>Transaction Tokens Service</h2>
<h3>Assure identity and context in microservices with <a href="https://tokenetes.io/docs/transaction-token/" target="_blank">Transaction Tokens</a>.</h3>
<div class="buttons">
  <a href="/docs" class="button">
    <i class="fas fa-book-open"></i>
    Learn More
  </a>
  <a href="/docs/quickstart" class="button">
    <i class="fas fa-rocket"></i>
    Get Started
  </a>
</div>
<div class="divider"></div>
<div class="community-buttons">
  <a href="https://github.com/orgs/tokenetes/discussions" class="community-button" target="_blank" rel="noopener noreferrer">
    <i class="fab fa-github"></i>
    Join the Discussion
  </a>
  <a href="https://github.com/tokenetes" class="community-button" target="_blank" rel="noopener noreferrer">
    <i class="fab fa-github"></i>
    View on GitHub
  </a>
</div>
</div>

<div class="cncf-banner">
  <div class="cncf-banner-container">
    <img src="/img/logos/cncf-color-bg.svg" alt="CNCF Logo">
    <p>Tokenetes is a <a href="https://www.cncf.io/" target="_blank" rel="noopener noreferrer">Cloud Native Computing Foundation</a> sandbox project.</p>
  </div>
</div>