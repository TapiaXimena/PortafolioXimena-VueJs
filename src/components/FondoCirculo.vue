<template>
  <svg viewBox="0 0 100 100" preserveAspectRatio="xMidYMid slice">
    <!-- Fondo sólido -->
    <rect width="100%" height="100%" fill="#2A0A3D"/>
    <!-- Círculos geométricos animados -->
    <circle cx="20" cy="20" r="10" fill="#4facfe" class="circle1"/>
    <circle cx="50" cy="40" r="8" fill="#00f2fe" class="circle2"/>
    <circle cx="80" cy="60" r="12" fill="#43e97b" class="circle3"/>
    <circle cx="35" cy="75" r="7" fill="#48cae4" class="circle4"/>
    <circle cx="65" cy="25" r="9" fill="#0096c7" class="circle5"/>
  </svg>
</template>

<style scoped>
@keyframes float {
  0% { transform: translateY(0px); }
  50% { transform: translateY(10px); }
  100% { transform: translateY(0px); }
}

.circle1 { animation: float 8s ease-in-out infinite; transform-origin: 20px 20px; }
.circle2 { animation: float 10s ease-in-out infinite alternate; transform-origin: 50px 40px; }
.circle3 { animation: float 12s ease-in-out infinite; transform-origin: 80px 60px; }
.circle4 { animation: float 9s ease-in-out infinite alternate; transform-origin: 35px 75px; }
.circle5 { animation: float 11s ease-in-out infinite; transform-origin: 65px 25px; }

svg {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: -1; /* texto encima del fondo */
}
</style>
