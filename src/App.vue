<template>
  <div id="app">
    <!-- AGB Page -->
    <div v-if="currentPage === 'agb'" class="agb-page">
      <header>
        <div class="header-content">
          <a href="#" @click="goHome" class="logo">Plistlabs</a>
          <button class="menu-toggle" @click="toggleMenu">☰</button>
          <nav :class="{ active: menuOpen }">
            <a href="#" @click="goHome">Startseite</a>
          </nav>
        </div>
      </header>
      <div class="container" style="padding-top: 40px; padding-bottom: 40px;">
        <h1>Allgemeine Geschäftsbedingungen (AGB)</h1>
        <h2>1. Geltungsbereich und Vertragsparteien</h2>
        <p>Diese Allgemeinen Geschäftsbedingungen (AGB) regeln die Geschäftsbeziehung zwischen Plistlabs und dem Kunden. Der Anbieter ist ein Einzelunternehmen mit Sitz in Wien, Österreich, und bietet KI-Automatisierungslösungen für Steuerberatungen an.</p>
        <h2>2. Leistungsumfang</h2>
        <p>Der Anbieter erbringt folgende Leistungen:</p>
        <ul>
          <li>Kostenlose Beratungsgespräche und Potenzialanalysen</li>
          <li>Entwicklung und Implementierung von KI-Automatisierungslösungen</li>
          <li>Integration in bestehende Systeme</li>
          <li>Schulung und Support nach Implementierung</li>
          <li>Wartung und Anpassung der Systeme</li>
        </ul>
        <h2>3. Preise und Zahlungsbedingungen</h2>
        <p>Die Preise für die Leistungen werden individuell in einem Angebot festgehalten. Rechnungen sind innerhalb von 14 Tagen nach Rechnungsdatum fällig.</p>
        <h2>4. Datenschutz und Sicherheit</h2>
        <p>Der Anbieter verpflichtet sich, alle Daten des Kunden DSGVO-konform zu behandeln. Alle Daten bleiben in der EU und werden mit verschlüsselten Verbindungen übertragen.</p>
        <h2>5. Haftung und Gewährleistung</h2>
        <p>Der Anbieter garantiert, dass die Leistungen fachgerecht erbracht werden. Die Haftung ist auf den Wert der erbrachten Leistungen begrenzt.</p>
        <h2>6. Vertragslaufzeit und Kündigung</h2>
        <p>Verträge für laufende Services können monatlich mit einer Frist von 30 Tagen gekündigt werden.</p>
        <h2>7. Geistiges Eigentum</h2>
        <p>Die von Plistlabs entwickelten Lösungen bleiben Eigentum des Anbieters. Der Kunde erhält ein Nutzungsrecht für die implementierten Lösungen.</p>
        <h2>8. Kontakt</h2>
        <p><strong>E-Mail:</strong> info@plistlabs.at<br><strong>Telefon:</strong> +43 699 1888 5442<br><strong>Adresse:</strong> Schweidlgasse 24, 1020 Wien, Österreich</p>
      </div>
    </div>

    <!-- Home Page -->
    <div v-else>
      <!-- Header -->
      <header>
        <div class="header-content">
          <a href="#" class="logo">Plistlabs</a>
          <button class="menu-toggle" @click="toggleMenu">☰</button>
          <nav :class="{ active: menuOpen }">
            <a href="#services" @click="closeMenu">Services</a>
            <a href="#about" @click="closeMenu">Über uns</a>
            <a href="#contact" @click="closeMenu">Kontakt</a>
            <a href="#" @click="showAGB">AGB</a>
          </nav>
        </div>
      </header>

      <!-- Hero Section -->
      <section class="hero" id="hero">
        <div class="container">
          <div class="hero-content">
            <div>
              <h1>KI statt Klickarbeit - die <span class="highlight">smarte Kanzlei von morgen</span></h1>
              <p>Wir entwickeln maßgeschneiderte KI-Lösungen, die wiederkehrende Routineaufgaben in Ihrer Steuerkanzlei automatisieren – damit sich Ihr Team auf Beratung statt Dateneingabe konzentriert.</p>
              <div class="hero-buttons">
                <button class="btn-primary" @click="scrollToContact">Unverbindliche Beratung</button>
                <button class="btn-secondary" @click="scrollToServices">Mehr erfahren</button>
              </div>
            </div>
            <div class="hero-image">
              <img src="/ki_hero.jpg" alt="KI-Automatisierung für Steuerberatungen">
            </div>
          </div>
        </div>
      </section>

      <!-- Problems Section -->
      <section class="problems" id="problems">
        <div class="container">
          <h2 class="section-title">Die Probleme, die wir lösen</h2>
          <div class="problems-grid">
            <div class="problem-card">
              <div class="problem-icon">📧</div>
              <h3>Zeitfressende Routineaufgaben</h3>
              <p>Ihre Mitarbeiter verbringen täglich Stunden mit Dateneingabe, E-Mail-Verwaltung und Belegverarbeitung statt mit echter Beratung.</p>
            </div>
            <div class="problem-card">
              <div class="problem-icon">⚠️</div>
              <h3>Fehlerquote bei manuellen Prozessen</h3>
              <p>Manuelle Eingaben führen zu Fehlern, die später aufwendig korrigiert werden müssen – Zeit und Geld kosten.</p>
            </div>
            <div class="problem-card">
              <div class="problem-icon">📞</div>
              <h3>Mandanten warten auf Antworten</h3>
              <p>Standardfragen werden nicht sofort beantwortet, weil Ihr Team mit Routineaufgaben beschäftigt ist. Mandanten sind frustriert.</p>
            </div>
            <div class="problem-card">
              <div class="problem-icon">⏰</div>
              <h3>Fristenmanagement ist manuell</h3>
              <p>Wichtige Termine und Fristen werden übersehen, weil es kein automatisiertes System gibt – Compliance-Risiken entstehen.</p>
            </div>
          </div>
        </div>
      </section>

      <!-- Services Section -->
      <section class="services" id="services">
        <div class="container">
          <h2 class="section-title">Unsere <span class="highlight">Services</span></h2>
          <div class="services-grid">
            <div class="service-card">
              <div class="service-icon">📄</div>
              <h3>AI-Beleg-Assistent</h3>
              <p>Automatische Belegverarbeitung. E-Mails werden gescannt, Belege erkannt und Daten automatisch extrahiert.</p>
              <div class="service-benefits">
                <div>✓ Zeitersparnis von 6-8 Stunden pro Woche</div>
                <div>✓ Weniger Fehler bei der Dateneingabe</div>
                <div>✓ Sofortige Verfügbarkeit der Daten</div>
              </div>
            </div>
            <div class="service-card">
              <div class="service-icon">☎️</div>
              <h3>KI-Telefonassistent</h3>
              <p>Intelligente Mandanten-Hotline, die Standardfragen beantwortet, Termine vereinbart und Informationen bereitstellt.</p>
              <div class="service-benefits">
                <div>✓ Verfügbarkeit 24/7 für Mandanten</div>
                <div>✓ Automatische Terminvergabe</div>
                <div>✓ Reduzierte Anrufmenge für Ihr Team</div>
              </div>
            </div>
            <div class="service-card">
              <div class="service-icon">💬</div>
              <h3>Mandanten-FAQ-Bot</h3>
              <p>Automatische E-Mail-Antworten für häufig gestellte Fragen. Intelligente Weiterleitung komplexer Anfragen an Ihr Team.</p>
              <div class="service-benefits">
                <div>✓ Sofortige Antworten auf Standardfragen</div>
                <div>✓ Weniger E-Mails für Ihr Team</div>
                <div>✓ Bessere Mandantenerfahrung</div>
              </div>
            </div>
            <div class="service-card">
              <div class="service-icon">👥</div>
              <h3>Mandanten-Onboarding</h3>
              <p>Automatisierte Onboarding-Prozesse mit digitalen Formularen, automatischen Checklisten und Erinnerungen.</p>
              <div class="service-benefits">
                <div>✓ Standardisierte Prozesse</div>
                <div>✓ Digitale Dokumentensammlung</div>
                <div>✓ Automatische Checklisten</div>
              </div>
            </div>
            <div class="service-card">
              <div class="service-icon">📅</div>
              <h3>Fristenmanagement</h3>
              <p>Automatische Überwachung von Fristen mit intelligenten Erinnerungen und Eskalationen.</p>
              <div class="service-benefits">
                <div>✓ Keine verpassten Fristen mehr</div>
                <div>✓ Automatische Erinnerungen</div>
                <div>✓ Übersichtliches Dashboard</div>
              </div>
            </div>
            <div class="service-card">
              <div class="service-icon">⚡</div>
              <h3>Prozessoptimierung</h3>
              <p>Maßgeschneiderte Workflow-Automatisierung für Ihre spezifischen Anforderungen und Systeme.</p>
              <div class="service-benefits">
                <div>✓ Individuelle Lösungen</div>
                <div>✓ Integration bestehender Systeme</div>
                <div>✓ Kontinuierliche Optimierung</div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- Results Section -->
      <section class="results">
        <div class="container">
          <h2 class="section-title">Das bringt <span class="highlight">Automatisierung</span></h2>
          <div class="results-grid">
            <div class="result-card">
              <div class="result-number">40h</div>
              <p>Zeitersparnis pro Monat</p>
            </div>
            <div class="result-card">
              <div class="result-number">80%</div>
              <p>Weniger Fehler</p>
            </div>
            <div class="result-card">
              <div class="result-number">24/7</div>
              <p>Verfügbarkeit</p>
            </div>
            <div class="result-card">
              <div class="result-number">4 Wo</div>
              <p>Implementierung</p>
            </div>
          </div>
          <div class="result-box">
            <h3>Das Ergebnis:</h3>
            <p>Bis zu 80 % weniger Aufwand bei Routinearbeiten in der Kanzlei. Mehr Zeit für Mandantenberatung, Jahresabschlüsse und strategische Themen. Ihre KI-Assistenten übernehmen den Rest – zuverlässig, präzise und rund um die Uhr.</p>
          </div>
        </div>
      </section>

      <!-- Why Us Section -->
      <section class="why-us">
        <div class="container">
          <h2 class="section-title">Warum <span class="highlight">Plistlabs?</span></h2>
          <div class="why-us-grid">
            <div class="why-card">
              <h3>Innovation & Nähe</h3>
              <p>Wir sind ein junges Team mit einem klaren Ziel: Kanzleien digital entlasten, ohne sie mit Technik zu überfordern. Bei uns sprechen Sie nicht mit Verkäufern, sondern direkt mit den Entwicklern.</p>
            </div>
            <div class="why-card">
              <h3>Partnerschaft statt Anbieter</h3>
              <p>Wir entwickeln jede Lösung gemeinsam mit unseren Kunden – praxisnah, schlank und individuell. Kein „One fits all", sondern ein System, das wirklich in Ihrer Kanzlei funktioniert.</p>
            </div>
            <div class="why-card">
              <h3>Datenschutz & Sicherheit</h3>
              <p>Datenschutz ist oberste Priorität. Alle Prozesse laufen DSGVO-konform, Ihre Daten bleiben in der EU und wir verwenden ausschließlich verschlüsselte Verbindungen.</p>
            </div>
            <div class="why-card">
              <h3>Schnelle Implementierung</h3>
              <p>In der Regel zwischen 2 und 4 Wochen. Wir starten mit einem kostenlosen Analysegespräch, definieren Ihre wichtigsten Automatisierungen und setzen diese schrittweise um.</p>
            </div>
          </div>
        </div>
      </section>

      <!-- Case Study Section -->
      <section class="case-study">
        <div class="container">
          <h2 class="section-title">Fallstudie: <span class="highlight">Praxis in Aktion</span></h2>
          <div class="case-study-content">
            <div class="case-study-text">
              <h3>Steuerkanzlei HWS - Dettingen</h3>
              <p><strong>Das Problem:</strong> Die Kanzlei mit 6 Mitarbeitern verbrachte täglich 3-4 Stunden mit Terminvergaben am Telefon. Mandanten warteten oft mehrere Tage auf Rückrufe.</p>
              <p><strong>Die Lösung:</strong> Implementierung des KI-Telefonassistenten von Plistlabs.</p>
              <p><strong>Das Ergebnis:</strong></p>
              <ul class="case-results">
                <li>✓ 6 Stunden pro Woche Zeitersparnis</li>
                <li>✓ 95% der Termine werden sofort vereinbart</li>
                <li>✓ Mandantenzufriedenheit um 40% gestiegen</li>
                <li>✓ Kein einziger Termin wird mehr übersehen</li>
              </ul>
            </div>
          </div>
        </div>
      </section>

      <!-- FAQ Section -->
      <section class="faq">
        <div class="container">
          <h2 class="section-title">Häufig gestellte <span class="highlight">Fragen</span></h2>
          <div class="faq-grid">
            <div class="faq-item">
              <h4>Wie funktioniert Ihre KI-Automatisierung konkret?</h4>
              <p>Wir analysieren Ihre Prozesse, identifizieren Automatisierungspotenziale und setzen diese schrittweise um. Alles läuft DSGVO-konform und sicher.</p>
            </div>
            <div class="faq-item">
              <h4>Wie lange dauert die Implementierung?</h4>
              <p>Durchschnittlich einige Wochen. Wir starten mit einer kostenlosen Analyse und setzen dann Schritt für Schritt um.</p>
            </div>
            <div class="faq-item">
              <h4>Funktioniert das mit unseren bestehenden Systemen?</h4>
              <p>Ja! Wir integrieren mit DATEV, Outlook, Cloud-Lösungen und vielen anderen Systemen. Individuelle Lösungen sind möglich.</p>
            </div>
            <div class="faq-item">
              <h4>Wie sicher sind meine Daten?</h4>
              <p>Höchste Priorität! DSGVO-konform, Daten bleiben in der EU. Keine Kompromisse beim Datenschutz.</p>
            </div>
            <div class="faq-item">
              <h4>Können wir das vorher testen?</h4>
              <p>Ja! Wir bieten eine kostenlose Potenzialanalyse und können Pilotprojekte durchführen, bevor wir alles ausrollen.</p>
            </div>
            <div class="faq-item">
              <h4>Was kostet das?</h4>
              <p>Die Preise sind individuell und hängen vom Umfang ab. Wir machen transparente Angebote ohne versteckte Gebühren.</p>
            </div>
            <div class="faq-item">
              <h4>Wie läuft der Support nach der Implementierung?</h4>
              <p>Wir bieten umfassenden Support, Schulungen und kontinuierliche Optimierung. Sie sind nicht allein gelassen.</p>
            </div>
            <div class="faq-item">
              <h4>Können wir die Automatisierung später ändern?</h4>
              <p>Absolut! Änderungen sind schnell möglich. Kleine Anpassungen in Stunden, größere Änderungen mit zusätzlichen Kosten.</p>
            </div>
            <div class="faq-item">
              <h4>Brauchen wir technisches Know-how?</h4>
              <p>Nein! Wir kümmern uns um die Technik. Sie müssen nur wissen, welche Prozesse automatisiert werden sollen.</p>
            </div>
            <div class="faq-item">
              <h4>Wie viele Mitarbeiter braucht ihr für die Implementierung?</h4>
              <p>Minimal! Wir brauchen einen Ansprechpartner, der die Prozesse kennt. Der Rest läuft im Hintergrund.</p>
            </div>
            <div class="faq-item">
              <h4>Können wir die Lösung wieder beenden?</h4>
              <p>Ja, mit 30 Tagen Kündigungsfrist. Aber die meisten Kunden möchten nicht mehr zurück, wenn sie die Zeitersparnis sehen.</p>
            </div>
          </div>
        </div>
      </section>

      <!-- About Section -->
      <section class="about" id="about">
        <div class="container">
          <h2 class="section-title">Über <span class="highlight">Plistlabs</span></h2>
          <div class="about-content">
            <div class="about-image">
              <img src="/daniel.jpg" alt="Daniel Plistiev">
            </div>
            <div class="about-text">
              <h2>Über uns</h2>
              <p>Ich bin Daniel Plistiev, Gründer & KI-Experte bei Plistlabs. Mit mehreren Jahren Erfahrung in der Prozessoptimierung und Automatisierung habe ich erkannt, dass viele Kanzleien täglich Stunden mit Routineaufgaben verschwenden.</p>
              <p>Meine Mission: Steuerberatungen durch intelligente KI-Lösungen entlasten und ihnen ermöglichen, sich auf das zu konzentrieren, was wirklich zählt – die Beratung ihrer Mandanten.</p>
              <p>Bei Plistlabs biete ich nicht nur Technologie, sondern echte Partnerschaft. Wir verstehen die Herausforderungen von Kanzleien und entwickeln Lösungen, die wirklich funktionieren.</p>
              <p class="name">Daniel Plistiev<br>Gründer & KI-Experte<br>Plistlabs</p>
            </div>
          </div>
        </div>
      </section>

      <!-- Contact Section -->
      <section class="contact" id="contact">
        <div class="container">
          <h2 class="section-title">Kontaktieren Sie uns</h2>
          <div class="contact-wrapper">
            <div class="contact-info">
              <h3>Direkt erreichbar</h3>
              <p><strong>E-Mail:</strong><br><a href="mailto:info@plistlabs.at">info@plistlabs.at</a></p>
              <p><strong>Telefon:</strong><br><a href="tel:+436991888544">+43 699 1888 5442</a></p>
              <p><strong>Adresse:</strong><br>Schweidlgasse 24<br>1020 Wien<br>Österreich</p>
            </div>
            <form class="contact-form" @submit.prevent="submitForm">
              <div class="form-group">
                <label for="name">Name *</label>
                <input type="text" id="name" v-model="form.name" required>
              </div>
              <div class="form-group">
                <label for="email">E-Mail *</label>
                <input type="email" id="email" v-model="form.email" required>
              </div>
              <div class="form-group">
                <label for="company">Kanzlei / Unternehmen</label>
                <input type="text" id="company" v-model="form.company">
              </div>
              <div class="form-group">
                <label for="phone">Telefon</label>
                <input type="tel" id="phone" v-model="form.phone">
              </div>
              <div class="form-group">
                <label for="message">Nachricht *</label>
                <textarea id="message" v-model="form.message" required></textarea>
              </div>
              <button type="submit" class="form-submit">Nachricht senden</button>
              <div v-if="formMessage" :class="['form-message', formMessageType]">
                {{ formMessage }}
              </div>
            </form>
          </div>
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
              <a href="#contact">Kontakt</a>
            </div>
            <div class="footer-section">
              <h4>Kontakt</h4>
              <p>info@plistlabs.at</p>
              <p>+43 699 1888 5442</p>
              <p>Schweidlgasse 24<br>1020 Wien, Österreich</p>
            </div>
            <div class="footer-section">
              <h4>Rechtliches</h4>
              <a href="#" @click="showImpressum">Impressum</a>
              <a href="#" @click="showDatenschutz">Datenschutzerklärung</a>
              <a href="#" @click="showAGB">AGB</a>
            </div>
            <div class="footer-section">
              <h4>Folgen Sie uns</h4>
              <a href="https://www.linkedin.com/in/danielplistiev/" target="_blank">LinkedIn</a>
            </div>
          </div>
          <div class="footer-bottom">
            <p>&copy; 2025 Plistlabs. Alle Rechte vorbehalten.</p>
          </div>
        </div>
      </footer>

      <!-- Modals -->
      <div class="impressum-content" :class="{ active: showImpressumModal }" @click="showImpressumModal = false">
        <div class="modal-content" @click.stop>
          <button class="modal-close" @click="showImpressumModal = false">×</button>
          <h2>Impressum</h2>
          <h3>Unternehmensangaben</h3>
          <p><strong>Unternehmen:</strong> Plistlabs<br><strong>Rechtsform:</strong> Einzelunternehmen<br><strong>Inhaber:</strong> Daniel Plistiev</p>
          <h3>Kontaktinformationen</h3>
          <p><strong>Adresse:</strong> Schweidlgasse 24, 1020 Wien, Österreich<br><strong>E-Mail:</strong> info@plistlabs.at<br><strong>Telefon:</strong> +43 699 1888 5442</p>
          <h3>UID-Nummer</h3>
          <p><strong>UID:</strong> ATU72102912</p>
          <h3>Geschäftstätigkeit</h3>
          <p>Entwicklung und Implementierung von KI-Automatisierungslösungen für Steuerberatungen und mittelständische Unternehmen.</p>
        </div>
      </div>

      <div class="datenschutz-content" :class="{ active: showDatenschutzModal }" @click="showDatenschutzModal = false">
        <div class="modal-content" @click.stop>
          <button class="modal-close" @click="showDatenschutzModal = false">×</button>
          <h2>Datenschutzerklärung</h2>
          <h3>1. Verantwortliche Stelle</h3>
          <p>Plistlabs, Daniel Plistiev, Schweidlgasse 24, 1020 Wien, Österreich</p>
          <h3>2. Erhobene Daten</h3>
          <p>Wir erheben Daten, die Sie uns freiwillig mitteilen (Name, E-Mail, Telefon, Unternehmen, Nachricht).</p>
          <h3>3. Verwendung der Daten</h3>
          <p>Ihre Daten werden ausschließlich zur Beantwortung Ihrer Anfrage verwendet.</p>
          <h3>4. Speicherung und Sicherheit</h3>
          <p>Alle Daten werden verschlüsselt übertragen und sicher gespeichert. Wir geben Ihre Daten nicht an Dritte weiter.</p>
          <h3>5. Ihre Rechte</h3>
          <p>Sie haben das Recht, Ihre Daten einzusehen, zu berichtigen oder zu löschen. Kontaktieren Sie uns unter info@plistlabs.at</p>
          <h3>6. Cookies</h3>
          <p>Wir verwenden Cookies nur für Cookie-Consent-Verwaltung. Keine Tracking-Cookies ohne Ihre Zustimmung.</p>
          <h3>7. Externe Dienste</h3>
          <p>Wir nutzen Formspree.io für Kontaktformulare (DSGVO-konform) und LinkedIn für Social Media.</p>
        </div>
      </div>

      <!-- Cookie Banner -->
      <div class="cookie-banner" v-if="showCookieBanner">
        <p>Wir verwenden Cookies für ein besseres Nutzungserlebnis. Durch Klicken auf "Akzeptieren" stimmen Sie zu.</p>
        <div class="cookie-buttons">
          <button class="cookie-accept" @click="acceptCookies">Akzeptieren</button>
          <button class="cookie-reject" @click="rejectCookies">Ablehnen</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      currentPage: 'home',
      menuOpen: false,
      showImpressumModal: false,
      showDatenschutzModal: false,
      showCookieBanner: false,
      form: {
        name: '',
        email: '',
        company: '',
        phone: '',
        message: ''
      },
      formMessage: '',
      formMessageType: ''
    };
  },
  mounted() {
    this.showCookieBanner = !localStorage.getItem('cookieConsent');
  },
  methods: {
    toggleMenu() {
      this.menuOpen = !this.menuOpen;
    },
    closeMenu() {
      this.menuOpen = false;
    },
    scrollToServices() {
      this.closeMenu();
      setTimeout(() => {
        document.getElementById('services').scrollIntoView({ behavior: 'smooth' });
      }, 0);
    },
    scrollToContact() {
      this.closeMenu();
      setTimeout(() => {
        document.getElementById('contact').scrollIntoView({ behavior: 'smooth' });
      }, 0);
    },
    showImpressum() {
      this.showImpressumModal = true;
      this.closeMenu();
    },
    showDatenschutz() {
      this.showDatenschutzModal = true;
      this.closeMenu();
    },
    showAGB() {
      this.currentPage = 'agb';
      window.scrollTo(0, 0);
    },
    goHome() {
      this.currentPage = 'home';
      window.scrollTo(0, 0);
    },
    acceptCookies() {
      localStorage.setItem('cookieConsent', 'true');
      this.showCookieBanner = false;
    },
    rejectCookies() {
      localStorage.setItem('cookieConsent', 'false');
      this.showCookieBanner = false;
    },
    async submitForm() {
      if (!localStorage.getItem('cookieConsent')) {
        this.formMessage = 'Bitte akzeptieren Sie die Cookies, um das Formular zu senden.';
        this.formMessageType = 'error';
        return;
      }

      try {
        const response = await fetch('https://formspree.io/f/xldorvea', {
          method: 'POST',
          headers: {
            'Content-Type': 'application/json'
          },
          body: JSON.stringify(this.form)
        });

        if (response.ok) {
          this.formMessage = 'Vielen Dank! Wir melden uns in Kürze bei Ihnen.';
          this.formMessageType = 'success';
          this.form = { name: '', email: '', company: '', phone: '', message: '' };
          setTimeout(() => {
            this.formMessage = '';
          }, 5000);
        } else {
          this.formMessage = 'Fehler beim Senden. Bitte versuchen Sie es später erneut.';
          this.formMessageType = 'error';
        }
      } catch (error) {
        this.formMessage = 'Fehler beim Senden. Bitte versuchen Sie es später erneut.';
        this.formMessageType = 'error';
      }
    }
  }
};
</script>
