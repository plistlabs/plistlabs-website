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
            <a href="#contact">Kontakt</a>
            <a href="#contact" class="btn-contact">Anfrage</a>
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
              <button class="btn-primary" @click="scrollToContact">Kostenlose Beratung</button>
              <button class="btn-secondary">Mehr erfahren</button>
            </div>
          </div>
          <div class="hero-image">
            <img src="/ki_hero.jpg" alt="KI-Automatisierung für Steuerberatungen" style="width: 100%; height: 100%; object-fit: cover; border-radius: 12px;">
          </div>
        </div>
      </div>
    </section>

    <!-- Problem Section -->
    <section class="problems">
      <div class="container">
        <h2 class="section-title">Das Problem: <span class="highlight">Zeitverschwendung durch Routineaufgaben</span></h2>
        <div class="benefits-grid">
          <div class="benefit-card" v-for="problem in problems" :key="problem.id">
            <h4>{{ problem.title }}</h4>
            <p>{{ problem.description }}</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Services Section -->
    <section class="services" id="services">
      <div class="container">
        <h2 class="section-title">Unsere <span class="highlight">Services</span></h2>
        <p style="text-align: center; color: #6b7280; margin-bottom: 50px; font-size: 16px; max-width: 700px; margin-left: auto; margin-right: auto;">
          Jeder Service ist speziell für die Anforderungen von Steuerberatungen entwickelt und lässt sich nahtlos in bestehende Systeme wie DATEV integrieren.
        </p>
        <div class="services-grid">
          <div class="service-card" v-for="service in services" :key="service.id">
            <div class="service-icon">{{ service.icon }}</div>
            <h3>{{ service.title }}</h3>
            <p>{{ service.description }}</p>
            <div style="margin-top: 20px; padding-top: 20px; border-top: 1px solid #e5e7eb;">
              <p style="font-weight: bold; color: #1f2937; margin-bottom: 10px;">Wie profitieren Sie davon:</p>
              <ul style="color: #6b7280; font-size: 14px; line-height: 1.8;">
                <li v-for="benefit in service.benefits" :key="benefit" style="margin-bottom: 8px;">✓ {{ benefit }}</li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Benefits Section -->
    <section class="benefits" style="background-color: #ffffff; padding: 80px 0;">
      <div class="container">
        <h2 class="section-title">Warum <span class="highlight">plistlabs?</span></h2>
        <div class="benefits-grid">
          <div class="benefit-card" v-for="benefit in whyUs" :key="benefit.id">
            <h4>{{ benefit.title }}</h4>
            <p>{{ benefit.description }}</p>
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

    <!-- Results Section -->
    <section class="results" style="background-color: #f9fafb; padding: 80px 0;">
      <div class="container">
        <h2 class="section-title">Das bringt <span class="highlight">Automatisierung</span></h2>
        <div class="benefits-grid">
          <div class="benefit-card" v-for="result in results" :key="result.id">
            <h4>{{ result.title }}</h4>
            <p>{{ result.description }}</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Contact Section -->
    <section class="contact" id="contact">
      <div class="container">
        <h2 class="section-title">Lassen Sie uns <span class="highlight">gemeinsam starten</span></h2>
        <p style="text-align: center; color: #6b7280; margin-bottom: 40px; font-size: 16px; max-width: 700px; margin-left: auto; margin-right: auto;">
          Füllen Sie das Formular aus und wir melden uns innerhalb von 24 Stunden bei Ihnen. Kostenlos und unverbindlich.
        </p>
        
        <div class="contact-form">
          <form @submit.prevent="submitForm">
            <div class="form-group">
              <label for="name">Name *</label>
              <input 
                type="text" 
                id="name" 
                v-model="form.name" 
                required 
                placeholder="Ihr Name"
              >
            </div>

            <div class="form-group">
              <label for="email">E-Mail *</label>
              <input 
                type="email" 
                id="email" 
                v-model="form.email" 
                required 
                placeholder="ihre@email.at"
              >
            </div>

            <div class="form-group">
              <label for="company">Kanzlei/Unternehmen *</label>
              <input 
                type="text" 
                id="company" 
                v-model="form.company" 
                required 
                placeholder="Name Ihrer Kanzlei"
              >
            </div>

            <div class="form-group">
              <label for="phone">Telefon</label>
              <input 
                type="tel" 
                id="phone" 
                v-model="form.phone" 
                placeholder="+43 1 234 56789"
              >
            </div>

            <div class="form-group">
              <label for="message">Nachricht *</label>
              <textarea 
                id="message" 
                v-model="form.message" 
                required 
                placeholder="Erzählen Sie uns von Ihren Herausforderungen..."
              ></textarea>
            </div>

            <button 
              type="submit" 
              class="form-submit"
              :disabled="isSubmitting"
            >
              {{ isSubmitting ? 'Wird gesendet...' : 'Anfrage senden' }}
            </button>

            <div v-if="formMessage" :class="['form-message', formMessageType]">
              {{ formMessage }}
            </div>
          </form>
        </div>
      </div>
    </section>

    <!-- CTA Section -->
    <section class="cta">
      <div class="container">
        <h2>Bereit für Automatisierung?</h2>
        <p>Lassen Sie uns gemeinsam Ihre Chancen entdecken</p>
        <button class="btn-primary" @click="scrollToContact">Kostenlose Potenzialanalyse buchen</button>
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
            <a href="mailto:info@plistlabs.at">info@plistlabs.at</a>
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
          <strong>E-Mail:</strong> info@plistlabs.at
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
        <p>Bei Fragen zur Datenschutzerklärung kontaktieren Sie uns unter: info@plistlabs.at</p>
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
      isSubmitting: false,
      formMessage: '',
      formMessageType: '',
      form: {
        name: '',
        email: '',
        company: '',
        phone: '',
        message: ''
      },
      problems: [
        {
          id: 1,
          title: '📧 E-Mails und Anrufe binden Ressourcen',
          description: 'Ihr Team beantwortet täglich die gleichen Fragen. Das kostet Zeit und Energie, die besser in Beratung investiert wäre.'
        },
        {
          id: 2,
          title: '📄 Belegverarbeitung ist zeitintensiv',
          description: 'Manuelle Eingabe von Belegen in DATEV kostet Stunden pro Woche. Fehler sind vorprogrammiert.'
        },
        {
          id: 3,
          title: '⏳ Fristen fallen durch die Maschen',
          description: 'Ohne automatische Überwachung gehen wichtige Fristen und Rückfragen verloren.'
        },
        {
          id: 4,
          title: '👥 Mandanten-Onboarding ist manuell',
          description: 'Neue Mandanten müssen manuell erfasst werden. Checklisten und Prozesse sind nicht standardisiert.'
        }
      ],
      services: [
        {
          id: 1,
          icon: '📄',
          title: 'AI-Beleg-Assistent',
          description: 'Automatische Belegverarbeitung mit DATEV-Integration. E-Mails werden gescannt, Belege erkannt und Daten automatisch extrahiert.',
          benefits: [
            'Zeitersparnis von 6-8 Stunden pro Woche',
            'Weniger Fehler bei der Dateneingabe',
            'Nahtlose DATEV-Integration',
            'Sofortige Verfügbarkeit der Daten'
          ]
        },
        {
          id: 2,
          icon: '📞',
          title: 'KI-Telefonassistent',
          description: 'Intelligente Mandanten-Hotline, die Standardfragen beantwortet, Termine vereinbart und Informationen bereitstellt.',
          benefits: [
            'Verfügbarkeit 24/7 für Mandanten',
            'Automatische Terminvergabe',
            'Reduzierte Anrufmenge für Ihr Team',
            'Höhere Mandantenzufriedenheit'
          ]
        },
        {
          id: 3,
          icon: '💬',
          title: 'Mandanten-FAQ-Bot',
          description: 'Automatische E-Mail-Antworten für häufig gestellte Fragen. Intelligente Weiterleitung komplexer Anfragen an Ihr Team.',
          benefits: [
            'Sofortige Antworten auf Standardfragen',
            'Weniger E-Mails für Ihr Team',
            'Bessere Mandantenerfahrung',
            'Zeitersparnis von 4-6 Stunden pro Woche'
          ]
        },
        {
          id: 4,
          icon: '👥',
          title: 'Mandanten-Onboarding',
          description: 'Automatisierte Onboarding-Prozesse mit digitalen Formularen, automatischen Checklisten und Erinnerungen.',
          benefits: [
            'Standardisierte Prozesse',
            'Digitale Dokumentensammlung',
            'Automatische Checklisten',
            'Keine vergessenen Schritte mehr'
          ]
        },
        {
          id: 5,
          icon: '⏳',
          title: 'Fristenmanagement',
          description: 'Automatische Überwachung von Fristen mit intelligenten Erinnerungen und Eskalationen.',
          benefits: [
            'Keine verpassten Fristen mehr',
            'Automatische Erinnerungen',
            'Übersichtliches Dashboard',
            'Compliance und Sicherheit'
          ]
        },
        {
          id: 6,
          icon: '⚡',
          title: 'Prozessoptimierung',
          description: 'Maßgeschneiderte Workflow-Automatisierung für Ihre spezifischen Anforderungen und Systeme.',
          benefits: [
            'Individuelle Lösungen',
            'Integration bestehender Systeme',
            'Kontinuierliche Optimierung',
            'Skalierbar mit Ihrem Wachstum'
          ]
        }
      ],
      whyUs: [
        {
          id: 1,
          title: '🎯 Spezialisiert auf Steuerberatungen',
          description: 'Wir verstehen die Anforderungen von Kanzleien. Unsere Lösungen sind speziell für Ihre Branche entwickelt.'
        },
        {
          id: 2,
          title: '🔗 DATEV-Integration',
          description: 'Alle unsere Services integrieren nahtlos mit DATEV. Keine komplizierten Systemwechsel erforderlich.'
        },
        {
          id: 3,
          title: '⚡ Schnelle Implementierung',
          description: 'Die meisten Lösungen sind innerhalb von 1-2 Wochen einsatzbereit. Sie profitieren schnell von den Ergebnissen.'
        },
        {
          id: 4,
          title: '🤝 Persönliche Betreuung',
          description: 'Sie bekommen einen festen Ansprechpartner. Wir unterstützen Sie bei jedem Schritt.'
        }
      ],
      results: [
        {
          id: 1,
          title: '⏱️ Zeitersparnis',
          description: 'Ihr Team gewinnt täglich mehrere Stunden zurück, die für hochwertige Beratung genutzt werden können.'
        },
        {
          id: 2,
          title: '😊 Höhere Mandantenzufriedenheit',
          description: 'Schnellere Antworten, bessere Erreichbarkeit und professionellere Abläufe führen zu zufriedeneren Mandanten.'
        },
        {
          id: 3,
          title: '💼 Mitarbeiterzufriedenheit',
          description: 'Weniger Routineaufgaben bedeuten motiviertere Mitarbeiter und bessere Retention.'
        },
        {
          id: 4,
          title: '📈 Skalierbarkeit',
          description: 'Wachsen Sie ohne proportionale Steigerung der Kosten. Automatisierung ermöglicht Skalierung.'
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
    },
    scrollToContact() {
      const contactSection = document.getElementById('contact');
      if (contactSection) {
        contactSection.scrollIntoView({ behavior: 'smooth' });
      }
    },
    async submitForm() {
      this.isSubmitting = true;
      this.formMessage = '';

      try {
        // Sende die E-Mail über einen einfachen Service
        const response = await fetch('https://formspree.io/f/xyzabc', {
          method: 'POST',
          headers: {
            'Content-Type': 'application/json'
          },
          body: JSON.stringify({
            name: this.form.name,
            email: this.form.email,
            company: this.form.company,
            phone: this.form.phone,
            message: this.form.message,
            _subject: `Neue Anfrage von ${this.form.name} - plistlabs`
          })
        });

        if (response.ok) {
          this.formMessage = '✓ Vielen Dank! Wir melden uns innerhalb von 24 Stunden bei Ihnen.';
          this.formMessageType = 'success';
          // Reset form
          this.form = {
            name: '',
            email: '',
            company: '',
            phone: '',
            message: ''
          };
        } else {
          this.formMessage = '✗ Es gab einen Fehler. Bitte versuchen Sie es später erneut.';
          this.formMessageType = 'error';
        }
      } catch (error) {
        this.formMessage = '✗ Es gab einen Fehler. Bitte versuchen Sie es später erneut.';
        this.formMessageType = 'error';
      } finally {
        this.isSubmitting = false;
        // Nachricht nach 5 Sekunden ausblenden
        setTimeout(() => {
          this.formMessage = '';
        }, 5000);
      }
    }
  }
}
</script>

<style scoped>
/* Alle Styles sind im index.html definiert */
</style>

