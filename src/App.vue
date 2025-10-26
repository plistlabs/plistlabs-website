<template>
  <div id="app">
    <!-- Header -->
    <header>
      <div class="header-content">
        <a href="#" class="logo">Plistlabs</a>
        <button class="menu-toggle" @click="toggleMenu">☰</button>
        <nav :class="{ active: menuOpen }">
          <a href="#services" @click="closeMenu">Services</a>
          <a href="#about" @click="closeMenu">Über uns</a>
          <a href="#contact" @click="closeMenu">Kontakt</a>
          <a href="/agb.html" @click="closeMenu">AGB</a>
        </nav>
      </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="hero">
      <div class="container">
        <div class="hero-content">
          <div>
            <h1>KI statt Klickarbeit - die <span class="highlight">smarte Kanzlei von morgen</span></h1>
            <p>Wir entwickeln maßgeschneiderte KI-Lösungen, die wiederkehrende Routineaufgaben in Ihrer Kanzlei automatisieren – damit sich Ihr Team auf Beratung statt Dateneingabe konzentriert.</p>
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
            <p>Zeitersparnis pro Monat durch Automatisierung</p>
          </div>
          <div class="result-card">
            <div class="result-number">80%</div>
            <p>Weniger Fehler bei automatisierten Prozessen</p>
          </div>
          <div class="result-card">
            <div class="result-number">24/7</div>
            <p>Verfügbarkeit für Ihre Mandanten</p>
          </div>
          <div class="result-card">
            <div class="result-number">4 Wo</div>
            <p>Durchschnittliche Implementierungszeit</p>
          </div>
        </div>

        <!-- Das Ergebnis Box -->
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
            <h3>Steuerkanzlei Müller & Partner - Wien</h3>
            <p><strong>Das Problem:</strong> Die Kanzlei mit 8 Mitarbeitern verbrachte täglich 3-4 Stunden mit Terminvergaben am Telefon. Mandanten warteten oft mehrere Tage auf Rückrufe, was zu Unzufriedenheit führte.</p>
            
            <p><strong>Die Lösung:</strong> Implementierung des KI-Telefonassistenten von Plistlabs. Der Assistent beantwortet Standardfragen, vereinbart Termine und leitet komplexe Anfragen an das Team weiter.</p>
            
            <p><strong>Das Ergebnis:</strong></p>
            <ul class="case-results">
              <li>✓ 6 Stunden pro Woche Zeitersparnis</li>
              <li>✓ 95% der Termine werden sofort vereinbart</li>
              <li>✓ Mandantenzufriedenheit um 40% gestiegen</li>
              <li>✓ Kein einziger Termin wird mehr übersehen</li>
            </ul>
            
            <p><strong>Zitat des Gründers:</strong> "Mit Plistlabs haben wir endlich Zeit für echte Beratung. Der Telefonassistent hat unseren Alltag revolutioniert."</p>
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
            <p>Unsere Lösung analysiert Ihre bestehenden Routineprozesse – z.B. E-Mail-Anfragen, Belegverarbeitung oder Mandantenkommunikation – und ersetzt manuelle Schritte durch intelligente Workflows. Wir verbinden Ihre bestehenden Systeme (DATEV, Outlook, Cloud, etc.) mit KI-gestützten Modulen.</p>
          </div>

          <div class="faq-item">
            <h4>Müssen wir unsere bestehende Software wechseln?</h4>
            <p>Nein. Wir integrieren uns in Ihr bestehendes System. Unsere KI-Lösungen arbeiten ergänzend zu Ihrer aktuellen Software, z.B. DATEV, Agenda oder Eigenlösungen.</p>
          </div>

          <div class="faq-item">
            <h4>Wie sicher sind unsere Daten?</h4>
            <p>Datenschutz ist oberste Priorität. Alle Prozesse laufen DSGVO-konform, Ihre Daten bleiben in der EU. Wir verwenden ausschließlich verschlüsselte Verbindungen und – auf Wunsch – Ihre eigene Infrastruktur (z.B. lokaler Server oder Cloud Ihrer Wahl).</p>
          </div>

          <div class="faq-item">
            <h4>Wie lange dauert die Implementierung?</h4>
            <p>In der Regel zwischen 2 und 4 Wochen, abhängig vom Prozessumfang. Wir starten mit einem kostenlosen Analysegespräch, definieren Ihre wichtigsten Automatisierungen und setzen diese schrittweise um.</p>
          </div>

          <div class="faq-item">
            <h4>Was kostet das?</h4>
            <p>Wir bieten modulare Preismodelle an – abhängig von Prozessumfang und Automatisierungsgrad. Es gibt keine versteckten Gebühren oder Lizenzverträge. Nach der kostenlosen Beratung erhalten Sie ein klares, nachvollziehbares Angebot.</p>
          </div>

          <div class="faq-item">
            <h4>Wer betreut uns nach der Einrichtung?</h4>
            <p>Sie haben einen festen Ansprechpartner, der Ihr System kennt und jederzeit erreichbar ist. Wir übernehmen auf Wunsch auch die laufende Wartung und Anpassung, wenn sich Ihre Kanzleiprozesse ändern.</p>
          </div>

          <div class="faq-item">
            <h4>Funktioniert das auch mit kleineren Kanzleien (1–5 Mitarbeiter)?</h4>
            <p>Ja, besonders dort. Kleine Kanzleien profitieren am stärksten, weil Routineaufgaben oft direkt auf die Inhaber oder Sachbearbeiter fallen. Unsere Lösungen sind skalierbar, egal ob Ein-Personen-Kanzlei oder großes Team.</p>
          </div>

          <div class="faq-item">
            <h4>Was passiert, wenn sich unsere Prozesse ändern?</h4>
            <p>Kein Problem – unsere Systeme sind modular aufgebaut. Wenn sich Abläufe ändern, können wir Automatisierungen in wenigen Stunden anpassen, ohne dass alles neu aufgebaut werden muss.</p>
          </div>

          <div class="faq-item">
            <h4>Können Sie uns Beispiele zeigen?</h4>
            <p>Ja. Im Erstgespräch zeigen wir konkrete Szenarien, z.B. automatische Erfassung eingehender Belege, KI-Assistent für Mandantenkommunikation, Reminder-System für Fristen und Rückfragen.</p>
          </div>

          <div class="faq-item">
            <h4>Wie viel Zeit kann man realistisch sparen?</h4>
            <p>Erfahrungsgemäß 30–80%, je nach Automatisierungsgrad. Besonders stark ist der Effekt bei repetitiven Aufgaben (z.B. E-Mail-Antworten, Fristenüberwachung, Belegsortierung).</p>
          </div>

          <div class="faq-item">
            <h4>Welche technischen Voraussetzungen gibt es?</h4>
            <p>Nur Internetzugang und Zugriff auf Ihre vorhandenen Tools (z.B. E-Mail, Cloud, Buchhaltungssoftware). Den Rest richten wir gemeinsam Schritt für Schritt ein.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- About Section -->
    <section class="about" id="about">
      <div class="container">
        <div class="about-content">
          <div class="about-image">
            <img src="/daniel.jpg" alt="Daniel Plistiev - Gründer & KI-Experte">
          </div>
          <div class="about-text">
            <h2>Über <span class="highlight">Plistlabs</span></h2>
            <p>Ich bin Daniel Plistiev, Gründer von Plistlabs. Mit mehreren Jahren Erfahrung in der Prozessoptimierung und Automatisierung habe ich erkannt, dass viele Kanzleien täglich Stunden mit Routineaufgaben verschwenden.</p>
            
            <p><strong>Meine Mission:</strong> Steuerberatungen durch intelligente Automatisierung entlasten und ihnen ermöglichen, sich auf das zu konzentrieren, was wirklich zählt – die Beratung ihrer Mandanten.</p>
            
            <p>Mit Plistlabs biete ich maßgeschneiderte KI-Lösungen, die nicht nur Zeit sparen, sondern auch die Qualität der Arbeit verbessern. Ich arbeite direkt mit meinen Kunden zusammen, um Lösungen zu schaffen, die wirklich funktionieren.</p>
            
            <p class="name">Daniel Plistiev<br><strong>Gründer & KI-Experte</strong></p>
          </div>
        </div>
      </div>
    </section>

    <!-- Contact Section -->
    <section class="contact" id="contact">
      <div class="container">
        <h2 class="section-title">Kontaktieren Sie <span class="highlight">uns</span></h2>
        <div class="contact-wrapper">
          <div class="contact-info">
            <h3>Kontaktdaten</h3>
            <p><strong>E-Mail:</strong> <a href="mailto:info@plistlabs.at">info@plistlabs.at</a></p>
            <p><strong>Telefon:</strong> <a href="tel:+436991888542">+43 699 1888 5442</a></p>
            <p><strong>Adresse:</strong> Schweidlgasse 24, 1020 Wien, Österreich</p>
          </div>
          
          <form class="contact-form" @submit.prevent="submitForm">
            <div class="form-group">
              <label for="name">Name</label>
              <input type="text" id="name" v-model="form.name" required>
            </div>
            <div class="form-group">
              <label for="email">E-Mail</label>
              <input type="email" id="email" v-model="form.email" required>
            </div>
            <div class="form-group">
              <label for="company">Kanzlei / Unternehmen</label>
              <input type="text" id="company" v-model="form.company" required>
            </div>
            <div class="form-group">
              <label for="phone">Telefon</label>
              <input type="tel" id="phone" v-model="form.phone">
            </div>
            <div class="form-group">
              <label for="message">Nachricht</label>
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
            <p><a href="mailto:info@plistlabs.at">info@plistlabs.at</a></p>
            <p><a href="tel:+436991888542">+43 699 1888 5442</a></p>
          </div>
          <div class="footer-section">
            <h4>Rechtliches</h4>
            <a href="#" @click="showImpressum">Impressum</a>
            <a href="#" @click="showDatenschutz">Datenschutzerklärung</a>
            <a href="/agb.html">AGB</a>
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

    <!-- Cookie Banner -->
    <div v-if="!cookieConsent" class="cookie-banner">
      <p>Wir verwenden Cookies, um Ihre Erfahrung zu verbessern. Mit der Nutzung dieser Website stimmen Sie zu.</p>
      <div class="cookie-buttons">
        <button class="cookie-accept" @click="acceptCookies">Akzeptieren</button>
        <button class="cookie-reject" @click="rejectCookies">Ablehnen</button>
      </div>
    </div>

    <!-- Impressum Modal -->
    <div v-if="showImpressumModal" class="impressum-content active">
      <div class="modal-content">
        <button class="modal-close" @click="showImpressumModal = false">&times;</button>
        <h2>Impressum</h2>
        <p><strong>Unternehmensname:</strong> Plistlabs</p>
        <p><strong>Rechtsform:</strong> Einzelunternehmen</p>
        <p><strong>Inhaber:</strong> Daniel Plistiev</p>
        <p><strong>Adresse:</strong> Schweidlgasse 24, 1020 Wien, Österreich</p>
        <p><strong>Telefon:</strong> +43 699 1888 5442</p>
        <p><strong>E-Mail:</strong> info@plistlabs.at</p>
        <p><strong>UID-Nummer:</strong> ATU72102912</p>
        <p><strong>Geschäftstätigkeit:</strong> Prozessautomatisierung und KI-Lösungen für Steuerberatungen und mittelständische Unternehmen</p>
        <h3>Haftungsausschluss</h3>
        <p>Trotz sorgfältiger Kontrolle übernehmen wir keine Haftung für die Inhalte externer Links. Für den Inhalt der verlinkten Seiten sind ausschließlich deren Betreiber verantwortlich.</p>
        <h3>Urheberrecht</h3>
        <p>Die Inhalte und Werke auf diesen Seiten sind urheberrechtlich geschützt. Die Vervielfältigung, Bearbeitung, Verbreitung und jede Art der Verwertung außerhalb der Grenzen des Urheberrechtes bedürfen der schriftlichen Zustimmung des Autors oder Erstellers.</p>
      </div>
    </div>

    <!-- Datenschutzerklärung Modal -->
    <div v-if="showDatenschutzModal" class="datenschutz-content active">
      <div class="modal-content">
        <button class="modal-close" @click="showDatenschutzModal = false">&times;</button>
        <h2>Datenschutzerklärung</h2>
        <h3>1. Verantwortliche Stelle</h3>
        <p>Verantwortlich für die Datenverarbeitung ist: Daniel Plistiev, Schweidlgasse 24, 1020 Wien, Österreich</p>
        
        <h3>2. Erhobene Daten</h3>
        <p>Wir erheben folgende Daten über unser Kontaktformular: Name, E-Mail-Adresse, Unternehmensname, Telefonnummer und Nachrichtentext.</p>
        
        <h3>3. Verwendung der Daten</h3>
        <p>Die Daten werden ausschließlich zur Beantwortung Ihrer Anfrage verwendet. Eine Weitergabe an Dritte erfolgt nicht.</p>
        
        <h3>4. Speicherung und Sicherheit</h3>
        <p>Ihre Daten werden verschlüsselt übertragen und sicher gespeichert. Wir verwenden nur DSGVO-konforme Dienste.</p>
        
        <h3>5. Ihre Rechte</h3>
        <p>Sie haben das Recht, Ihre Daten zu sehen, zu korrigieren oder zu löschen. Kontaktieren Sie uns unter info@plistlabs.at</p>
        
        <h3>6. Cookies</h3>
        <p>Wir verwenden Cookies nur mit Ihrer Zustimmung. Sie können diese jederzeit ablehnen.</p>
        
        <h3>7. Externe Dienste</h3>
        <p>Das Kontaktformular wird über Formspree.io verarbeitet, das DSGVO-konform ist. Ihre Daten werden nicht an Dritte weitergegeben.</p>
        
        <h3>8. Kontakt und Beschwerden</h3>
        <p>Bei Fragen kontaktieren Sie uns: info@plistlabs.at. Sie können sich auch an die österreichische Datenschutzbehörde wenden.</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      menuOpen: false,
      cookieConsent: localStorage.getItem('plistlabs-cookie-consent') !== null,
      showImpressumModal: false,
      showDatenschutzModal: false,
      form: {
        name: '',
        email: '',
        company: '',
        phone: '',
        message: ''
      },
      formMessage: '',
      formMessageType: ''
    }
  },
  methods: {
    toggleMenu() {
      this.menuOpen = !this.menuOpen;
    },
    closeMenu() {
      this.menuOpen = false;
    },
    scrollToContact() {
      const contactSection = document.getElementById('contact');
      if (contactSection) {
        contactSection.scrollIntoView({ behavior: 'smooth' });
      }
    },
    scrollToServices() {
      const servicesSection = document.getElementById('services');
      if (servicesSection) {
        servicesSection.scrollIntoView({ behavior: 'smooth' });
      }
    },
    acceptCookies() {
      localStorage.setItem('plistlabs-cookie-consent', 'accepted');
      this.cookieConsent = true;
    },
    rejectCookies() {
      localStorage.setItem('plistlabs-cookie-consent', 'rejected');
      this.cookieConsent = true;
    },
    showImpressum(e) {
      e.preventDefault();
      this.showImpressumModal = true;
    },
    showDatenschutz(e) {
      e.preventDefault();
      this.showDatenschutzModal = true;
    },
    async submitForm() {
      const cookieConsent = localStorage.getItem('plistlabs-cookie-consent');
      if (cookieConsent === 'rejected') {
        this.formMessage = 'Bitte akzeptieren Sie die Cookie-Richtlinie, um das Formular zu senden.';
        this.formMessageType = 'error';
        return;
      }

      try {
        const response = await fetch('https://formspree.io/f/xldorvea', {
          method: 'POST',
          headers: {
            'Content-Type': 'application/json',
          },
          body: JSON.stringify(this.form)
        });

        if (response.ok) {
          this.formMessage = 'Vielen Dank! Ihre Nachricht wurde erfolgreich versendet. Wir melden uns in Kürze bei Ihnen.';
          this.formMessageType = 'success';
          this.form = { name: '', email: '', company: '', phone: '', message: '' };
          setTimeout(() => {
            this.formMessage = '';
          }, 5000);
        } else {
          this.formMessage = 'Es gab einen Fehler beim Versenden. Bitte versuchen Sie es später erneut.';
          this.formMessageType = 'error';
        }
      } catch (error) {
        this.formMessage = 'Es gab einen Fehler beim Versenden. Bitte versuchen Sie es später erneut.';
        this.formMessageType = 'error';
      }
    }
  }
}
</script>

