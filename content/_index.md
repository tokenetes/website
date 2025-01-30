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
  padding: 4em 1em 6em 1em;
}
.home img {
  width: 500px;
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
  font-size: 1.4vw;
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
  font-size: 1.4vw;
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
<img src="/img/logos/tokenetes - preview - transparent-01.png" alt="Tokenetes Logo">
<h1>Tokenetes</h1>
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