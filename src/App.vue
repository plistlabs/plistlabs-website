<template>
  <div id="app">
    <!-- Header -->
    <header>
      <div class="container">
        <div class="header-content">
          <a href="#" class="logo">plistlabs</a>
          <nav>
            <a href="#services">Services</a>
            <a href="#about">Über uns</a>
            <a href="#roi">ROI</a>
            <a href="#contact" class="btn-contact">Kontakt</a>
          </nav>
        </div>
      </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
      <div class="container">
        <div class="hero-content">
          <div>
            <h1>Prozessautomatisierung für <span class="highlight">Steuerberatungen</span></h1>
            <p>Wir entwickeln maßgeschneiderte KI-Lösungen, die wiederkehrende Routineaufgaben in Ihrer Kanzlei automatisieren – damit sich Ihr Team auf Beratung statt Dateneingabe konzentriert.</p>
            <div class="hero-buttons">
              <button class="btn-primary">Kostenlose Beratung</button>
              <button class="btn-secondary">Mehr erfahren</button>
            </div>
          </div>
          <div class="hero-image">
            🤖 Automatisierung für Steuerberatungen
          </div>
        </div>
      </div>
    </section>

    <!-- Services Section -->
    <section class="services" id="services">
      <div class="container">
        <h2 class="section-title">Unsere <span class="highlight">Services</span></h2>
        <div class="services-grid">
          <div class="service-card" v-for="service in services" :key="service.id">
            <div class="service-icon">{{ service.icon }}</div>
            <h3>{{ service.title }}</h3>
            <p>{{ service.description }}</p>
            <div class="service-roi" v-if="service.roi">{{ service.roi }}</div>
          </div>
        </div>
      </div>
    </section>

    <!-- About Section -->
    <section class="about" id="about">
      <div class="container">
        <div class="about-content">
          <div class="about-image">
            <img src="/daniel.jpg" alt="Daniel Plistiev">
          </div>
          <div class="about-text">
            <h2>Über <span class="highlight">plistlabs</span></h2>
            <p>Ich bin Daniel Plistiev, Gründer von plistlabs. Mit über 10 Jahren Erfahrung in der Steuerberatung und Prozessoptimierung habe ich erkannt, dass viele Kanzleien täglich Stunden mit Routineaufgaben verschwenden.</p>
            <p>Meine Mission: Steuerberatungen durch intelligente Automatisierung entlasten und ihnen ermöglichen, sich auf das zu konzentrieren, was wirklich zählt – die Beratung ihrer Mandanten.</p>
            <p>Mit plistlabs biete ich maßgeschneiderte KI-Lösungen, die nahtlos in bestehende Systeme wie DATEV integrieren und sofort Ergebnisse liefern.</p>
            <p class="name">Daniel Plistiev<br>Gründer & CEO, plistlabs</p>
          </div>
        </div>
      </div>
    </section>

    <!-- ROI Section -->
    <section class="roi" id="roi">
      <div class="container">
        <h2 class="section-title">Konkrete <span class="highlight">Einsparungen</span></h2>
        <div class="roi-grid">
          <div class="roi-card" v-for="roi in roiExamples" :key="roi.id">
            <div class="roi-number">{{ roi.savings }}</div>
            <h4>{{ roi.title }}</h4>
            <p>{{ roi.description }}</p>
          </div>
        </div>
      </div>
    </section>

    <!-- CTA Section -->
    <section class="cta" id="contact">
      <div class="container">
        <h2>Bereit für Automatisierung?</h2>
        <p>Lassen Sie uns gemeinsam Ihre Chancen entdecken</p>
        <button class="btn-primary">Kostenlose Potenzialanalyse buchen</button>
      </div>
    </section>

    <!-- Footer -->
    <footer>
      <div class="container">
        <div class="footer-content">
          <div class="footer-section">
            <h4>Unternehmen</h4>
            <a href="#about">Über uns</a>
            <a href="#services">Services</a>
            <a href="#roi">ROI Beispiele</a>
          </div>
          <div class="footer-section">
            <h4>Kontakt</h4>
            <a href="mailto:daniel@plistlabs.at">daniel@plistlabs.at</a>
            <a href="tel:+43123456789">+43 1 234 56789</a>
            <p style="color: #9ca3af; margin-top: 10px; font-size: 14px;">Schweidlgasse 24<br>1020 Wien, Österreich</p>
          </div>
          <div class="footer-section">
            <h4>Rechtliches</h4>
            <a href="#" @click="showImpressum">Impressum</a>
            <a href="#" @click="showDatenschutz">Datenschutzerklärung</a>
          </div>
        </div>
        <div class="footer-bottom">
          <p>&copy; 2025 plistlabs. Alle Rechte vorbehalten.</p>
        </div>
      </div>
    </footer>

    <!-- Impressum Modal -->
    <div class="impressum-content" :class="{ active: showImpressumModal }">
      <div class="modal-content">
        <button class="modal-close" @click="showImpressumModal = false">✕</button>
        <h2>Impressum</h2>
        <h3>Unternehmensdaten</h3>
        <p>
          <strong>Firmenname:</strong> plistlabs<br>
          <strong>Inhaber:</strong> Daniel Plistiev<br>
          <strong>Adresse:</strong> Schweidlgasse 24, 1020 Wien, Österreich<br>
          <strong>UID-Nummer:</strong> ATU72102912<br>
          <strong>E-Mail:</strong> daniel@plistlabs.at
        </p>
        <h3>Haftungsausschluss</h3>
        <p>Die Inhalte dieser Website werden mit größtmöglicher Sorgfalt erstellt. Für die Richtigkeit, Vollständigkeit und Aktualität der Inhalte können wir jedoch keine Gewähr übernehmen.</p>
        <h3>Externe Links</h3>
        <p>Unsere Website enthält Links zu externen Websites. Für den Inhalt dieser externen Seiten sind wir nicht verantwortlich.</p>
      </div>
    </div>

    <!-- Datenschutzerklärung Modal -->
    <div class="datenschutz-content" :class="{ active: showDatenschutzModal }">
      <div class="modal-content">
        <button class="modal-close" @click="showDatenschutzModal = false">✕</button>
        <h2>Datenschutzerklärung</h2>
        <h3>1. Verantwortliche Stelle</h3>
        <p>Verantwortlich für die Datenverarbeitung ist: Daniel Plistiev, Schweidlgasse 24, 1020 Wien, Österreich</p>
        <h3>2. Erhobene Daten</h3>
        <p>Wir erheben personenbezogene Daten nur, wenn Sie uns diese freiwillig mitteilen (z.B. über Kontaktformulare).</p>
        <h3>3. Verwendung der Daten</h3>
        <p>Ihre Daten werden ausschließlich zur Beantwortung Ihrer Anfragen verwendet und nicht an Dritte weitergegeben.</p>
        <h3>4. Ihre Rechte</h3>
        <p>Sie haben das Recht auf Auskunft, Berichtigung, Löschung und Widerspruch bezüglich Ihrer personenbezogenen Daten.</p>
        <h3>5. Cookies</h3>
        <p>Diese Website verwendet keine Tracking-Cookies. Technisch notwendige Cookies können verwendet werden.</p>
        <h3>6. Kontakt</h3>
        <p>Bei Fragen zur Datenschutzerklärung kontaktieren Sie uns unter: daniel@plistlabs.at</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      showImpressumModal: false,
      showDatenschutzModal: false,
      services: [
        {
          id: 1,
          icon: '📄',
          title: 'AI-Beleg-Assistent',
          description: 'Automatische Belegverarbeitung und DATEV-Integration. E-Mail rein, Beleg erkannt, Daten extrahiert.',
          roi: '860€ Ersparnis/Monat'
        },
        {
          id: 2,
          icon: '📞',
          title: 'KI-Telefonassistent',
          description: 'Intelligente Mandanten-Hotline, die Standardfragen beantwortet und Termine vereinbart.',
          roi: '740€ Ersparnis/Monat'
        },
        {
          id: 3,
          icon: '💬',
          title: 'Mandanten-FAQ-Bot',
          description: 'Automatische E-Mail-Antworten für wiederkehrende Fragen. 24/7 verfügbar und zuverlässig.',
          roi: '704€ Ersparnis/Monat'
        },
        {
          id: 4,
          icon: '👥',
          title: 'Mandanten-Onboarding',
          description: 'Automatisierte Onboarding-Prozesse mit digitalen Formularen und automatischen Checklisten.'
        },
        {
          id: 5,
          icon: '⏳',
          title: 'Fristenmanagement',
          description: 'Automatische Überwachung und Erinnerungen für wichtige Fristen und Rückfragen.'
        },
        {
          id: 6,
          icon: '⚡',
          title: 'Prozessoptimierung',
          description: 'Maßgeschneiderte Workflow-Automatisierung für Ihre spezifischen Anforderungen.'
        }
      ],
      roiExamples: [
        {
          id: 1,
          savings: '860€',
          title: 'AI-Beleg-Assistent',
          description: 'Monatliche Ersparnis durch automatische Belegverarbeitung. Break-even nach 4 Monaten.'
        },
        {
          id: 2,
          savings: '740€',
          title: 'KI-Telefonassistent',
          description: 'Monatliche Ersparnis durch Automatisierung von Standardanrufen. Break-even nach 4-5 Monaten.'
        },
        {
          id: 3,
          savings: '704€',
          title: 'Mandanten-FAQ-Bot',
          description: 'Monatliche Ersparnis durch automatische E-Mail-Antworten. Break-even nach 4 Monaten.'
        }
      ]
    }
  },
  methods: {
    showImpressum(e) {
      e.preventDefault();
      this.showImpressumModal = true;
    },
    showDatenschutz(e) {
      e.preventDefault();
      this.showDatenschutzModal = true;
    }
  }
}
</script>

<style scoped>
/* Alle Styles sind im index.html definiert */
</style>

