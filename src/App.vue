<template>
  <div id="app">
    <!-- Header -->
    <header>
      <div class="container">
        <div class="header-content">
          <a href="#" class="logo">plistlabs</a>
          <nav>
            <a href="#problems">Probleme</a>
            <a href="#solutions">Lösungen</a>
            <a href="#benefits">Vorteile</a>
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
            <h1>Das <span class="highlight">AI Ready</span> Kanzleibüro wird Realität</h1>
            <p>Wir entwickeln maßgeschneiderte KI-Mitarbeiter, die Ihre täglichen Aufgaben automatisieren und Ihre bestehenden Tools intelligent vernetzen – ohne komplizierte Systemwechsel.</p>
            <div class="hero-buttons">
              <button class="btn-primary">Unverbindliche Beratung</button>
              <button class="btn-secondary">Mehr erfahren</button>
            </div>
          </div>
          <div class="hero-image">
            🤖 KI-Automatisierung für Kanzleien
          </div>
        </div>
      </div>
    </section>

    <!-- Problems Section -->
    <section class="problems" id="problems">
      <div class="container">
        <h2 class="section-title">Ohne KI-Agenten <span class="highlight">verlieren Sie täglich Kunden</span></h2>
        <div class="problems-grid">
          <div class="problem-card" v-for="problem in problems" :key="problem.id">
            <h3>
              <div class="problem-icon">{{ problem.icon }}</div>
              {{ problem.title }}
            </h3>
            <p>{{ problem.description }}</p>
            <div class="problem-impact">{{ problem.impact }}</div>
          </div>
        </div>
      </div>
    </section>

    <!-- Solutions Section -->
    <section class="solutions" id="solutions">
      <div class="container">
        <h2 class="section-title">Zeit für eine <span class="highlight">Veränderung?</span></h2>
        <div class="solutions-grid">
          <div class="solution-card" v-for="solution in solutions" :key="solution.id">
            <div class="solution-icon">{{ solution.icon }}</div>
            <h3>{{ solution.title }}</h3>
            <p>{{ solution.description }}</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Benefits Section -->
    <section class="benefits" id="benefits">
      <div class="container">
        <h2 class="section-title">Das sagen unsere <span class="highlight">Kunden</span></h2>
        <div class="benefits-grid">
          <div class="benefit-item" v-for="benefit in benefits" :key="benefit.id">
            <div class="benefit-number">{{ benefit.number }}</div>
            <div class="benefit-content">
              <h4>{{ benefit.title }}</h4>
              <p>{{ benefit.description }}</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- CTA Section -->
    <section class="cta" id="contact">
      <div class="container">
        <h2>Bereit für KI-Automatisierung?</h2>
        <p>Lassen Sie uns gemeinsam Ihre Chancen entdecken</p>
        <button class="btn-primary">Kostenlose Potenzialanalyse buchen</button>
      </div>
    </section>

    <!-- Footer -->
    <footer>
      <div class="container">
        <p>&copy; 2025 plistlabs. Alle Rechte vorbehalten.</p>
        <p>KI-Automatisierung für Kanzleien</p>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      problems: [
        {
          id: 1,
          icon: '📱',
          title: 'Inkonsistente Social Media Präsenz',
          description: 'Unregelmäßige Posts, verpasste Posting-Zeiten und unprofessionelle Inhalte kosten wertvolle Leads',
          impact: 'Der Schaden: Bis zu 40% weniger Online-Sichtbarkeit'
        },
        {
          id: 2,
          icon: '📞',
          title: 'Verpasste Anrufe & schlechte Qualifizierung',
          description: 'Anrufe gehen verloren, Interessenten werden schlecht qualifiziert oder müssen zu lange warten',
          impact: 'Der Schaden: 30% der Leads gehen durch verpasste Calls verloren'
        },
        {
          id: 3,
          icon: '💬',
          title: 'Langsame WhatsApp-Kommunikation',
          description: 'Stundenlange Antwortzeitenführen zu frustrierten Kunden und verlorenen Deals',
          impact: 'Der Schaden: 67% der Kunden erwarten Antwort binnen 1 Stunde'
        },
        {
          id: 4,
          icon: '⏰',
          title: 'Zeitverschwendung bei Routineaufgaben',
          description: 'Manuelle Prozesse und administrative Tätigkeiten verschlingen wertvolle Zeit',
          impact: 'Der Schaden: 60% der Arbeitszeit für Routine statt Kunden'
        }
      ],
      solutions: [
        {
          id: 1,
          icon: '🤖',
          title: 'AI-Beleg-Assistent',
          description: 'Automatische Belegverarbeitung und DATEV-Integration. E-Mail rein, Beleg erkannt, Daten extrahiert.'
        },
        {
          id: 2,
          icon: '📞',
          title: 'KI-Telefonassistent',
          description: 'Intelligente Mandanten-Hotline, die Standardfragen beantwortet und Termine vereinbart.'
        },
        {
          id: 3,
          icon: '💬',
          title: 'Mandanten-FAQ-Bot',
          description: 'Automatische E-Mail-Antworten für wiederkehrende Fragen. 24/7 verfügbar und zuverlässig.'
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
      benefits: [
        {
          id: 1,
          number: '40h',
          title: 'Zeitersparnis pro Monat',
          description: 'Weniger Routineaufgaben, mehr Zeit für strategische Beratung'
        },
        {
          id: 2,
          number: '860€',
          title: 'Kostenersparnis monatlich',
          description: 'Durchschnittliche Einsparungen durch Automatisierung'
        },
        {
          id: 3,
          number: '24/7',
          title: 'Verfügbarkeit',
          description: 'KI-Agenten arbeiten rund um die Uhr ohne Pause'
        },
        {
          id: 4,
          number: '4',
          title: 'Monate Break-even',
          description: 'ROI-Amortisation durchschnittlich nach 4 Monaten'
        }
      ]
    }
  }
}
</script>

<style scoped>
/* Alle Styles sind im index.html definiert */
</style>

