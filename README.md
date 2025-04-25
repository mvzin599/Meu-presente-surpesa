body, html {
  margin: 0;
  padding: 0;
  height: 100%;
  overflow: hidden;
  font-family: 'Brush Script MT', cursive;
}

.romantic-section {
  position: relative;
  height: 100vh;
  background-color: #ffd9ec;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
}

.romantic-photo {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
  filter: brightness(0.5) blur(2px);
  z-index: 1;
}

.overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(255, 192, 203, 0.3);
  z-index: 2;
}

.romantic-message {
  position: relative;
  z-index: 3;
  padding: 30px;
  max-width: 800px;
  background: rgba(255, 255, 255, 0.75);
  border-radius: 20px;
  font-size: 24px;
  color: #d63384;
  animation: fadeIn 2s ease;
}

@keyframes fadeIn {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

/* Corações flutuando */
.hearts {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  pointer-events: none;
  overflow: hidden;
  z-index: 3;
}

.heart {
  position: absolute;
  width: 20px;
  height: 20px;
  background: pink;
  transform: rotate(45deg);
  animation: floatHearts 8s infinite ease-in;
}

.heart::before,
.heart::after {
  content: '';
  position: absolute;
  width: 20px;
  height: 20px;
  background: pink;
  border-radius: 50%;
}

.heart::before {
  top: -10px;
  left: 0;
}

.heart::after {
  left: -10px;
  top: 0;
}

@keyframes floatHearts {
  0% {
    transform: translateY(100vh) rotate(45deg);
    opacity: 0;
  }
  50% {
    opacity: 1;
  }
  100% {
    transform: translateY(-10vh) rotate(45deg);
    opacity: 0;
  }
}

/* Posições aleatórias para os corações */
.heart:nth-child(1) { left: 10%; animation-delay: 0s; }
.heart:nth-child(2) { left: 30%; animation-delay: 2s; }
.heart:nth-child(3) { left: 50%; animation-delay: 4s; }
.heart:nth-child(4) { left: 70%; animation-delay: 1s; }
.heart:nth-child(5) { left: 90%; animation-delay: 3s; }
