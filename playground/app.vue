<template>
  <div class="cv-container">
    <!-- Partículas fosforescentes -->
    <span class="particle"></span>
    <span class="particle"></span>
    <span class="particle"></span>
    <span class="particle"></span>
    <span class="particle"></span>

    <button id="modoOscuro" @click="toggleDarkMode">
      {{ isDark ? '☀️' : '🌙' }} Modo {{ isDark ? 'Claro' : 'Oscuro' }}
    </button>

    <header>
      <h1>Aaron Antonio Guzmán Morán</h1>
      <p>Estudiante de Tecnologías de la Información</p>
      <div class="contact-bar">
        <span>📧 aaronmoran20148@gmail.com</span>
        <span>📱 55 4803 7442</span>
      </div>
    </header>

    <main>
      <section class="card">
        <h2>Sobre mí</h2>
        <p>
          Estudiante de Tecnologías de la Información con interés en desarrollo
          de software y optimización de procesos mediante soluciones
          tecnológicas. Experiencia académica sólida en programación, bases de
          datos y desarrollo web. He participado en dos proyectos reales de
          migración de bases de datos con éxito.
        </p>
      </section>

      <div class="grid-2">
        <section class="card">
          <h2>Herramientas / Tecnologías</h2>
          <div class="skills-grid">
            <span>SQL Server</span>
            <span>Oracle</span>
            <span>Python</span>
            <span>Redes</span>
          </div>
        </section>

        <section class="card">
          <h2>Idiomas</h2>
          <ul>
            <li>Inglés – Nivel básico</li>
          </ul>
        </section>
      </div>

      <section class="card">
        <h2>Experiencia relevante</h2>
        <ul class="experience-list">
          <li>Migración de SQL Server 2012 → SQL Server 2019 (servidor físico a servidor físico)</li>
          <li>Automatización de base de datos SQL Server mediante stored procedures (archivado mensual automático)</li>
        </ul>
      </section>

      <section class="card">
        <h2>Logros técnicos destacados</h2>
        <ul class="achievements">
          <li>Migración exitosa sin pérdida de datos ni downtime crítico</li>
          <li>Implementación de automatización que redujo tiempo manual en >90%</li>
          <li>Reorganización y optimización de estructuras de datos en entornos productivos</li>
        </ul>
      </section>

      <section class="card">
        <h2>Soft Skills</h2>
        <div class="skills-grid">
          <span>Trabajo en equipo</span>
          <span>Resolución de problemas</span>
          <span>Aprendizaje rápido</span>
          <span>Adaptabilidad</span>
          <span>Comunicación técnica</span>
        </div>
      </section>
    </main>

    <footer>
      <p>Actualizado • febrero 2026</p>
    </footer>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const isDark = ref(false)

const toggleDarkMode = () => {
  isDark.value = !isDark.value
  document.documentElement.classList.toggle('dark', isDark.value)
}
</script>
