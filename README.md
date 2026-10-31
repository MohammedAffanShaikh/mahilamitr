# MAHILAMITR

**Unified Community Safety & Resilience Platform** — responsive prototype for the SEVA Innovation Challenge.

This demonstration connects community resources, alert status, institutional workflow, local evidence records, low-connectivity simulation and aggregate insights. All records and metrics are simulated. The application does not contact police, ERSS 112, hospitals, government systems or external responders, and it does not guarantee assistance.

## Run locally

Requirements: Node.js 20+ and npm.

```sh
npm install
npm run dev
```

Vite prints the local URL. To make a production bundle:

```sh
npm run build
npm run preview
```

## Demo flow

1. Open **SAFEGRID** and browse the example Pune help points, filters and route visualization. Location access is only requested after selecting **My location**.
2. Open **MAHILAMITR LINK** and select **Hold to simulate SOS**. This creates a local sample incident; delivery and responder states are explicitly simulated.
3. Change the role selector to **Responder** or **Institution** and open **INSTITUTION SHIELD**. Acknowledge the alert and mark it resolved to progress its response timeline.
4. Add a document or note in **TRUSTVAULT**. Files are hashed with browser SHA-256 and kept only in the current session; this is not secure or encrypted storage.
5. Open **CIVIC INSIGHT** to review sample aggregate charts and the demo trend summary.
6. Open **COMMUNITY RELAY**, simulate offline mode, queue a sample check-in, and restore connectivity to demonstrate local synchronization.

## Roles and safety boundaries

The role selector changes demonstration access and content. It is **not authentication or production authorization**. Do not put sensitive data in this prototype. Analytics contain sample data only and omit identities. Maps show illustrative local listings; routes are not guaranteed safe. A cryptographic hash can detect a file change but does not establish authenticity, truth or legal admissibility. If immediate assistance is needed, contact official emergency services.

## Technology

React, TypeScript, Vite, Tailwind CSS, Lucide React, React Router, Recharts and Leaflet with OpenStreetMap tiles. The map plots illustrative Pune-area sample points over public OSM tiles. Map tiles require internet access; all other demonstration workflows run from local browser state without API credentials. Data and state are local to the browser session.

## Optional backend

No backend credentials are needed for this demo. `.env.example` documents optional future Supabase integration settings. Never expose service-role secrets in a frontend bundle. A production deployment would need a secured backend, reviewed role/consent policies, data retention controls and authorized integrations before handling real safety information.

## Netlify

The included `netlify.toml` builds with `npm run build`, publishes `dist`, and rewrites client routes to `index.html`.
