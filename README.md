# E-Ballot Concept
Author: ***

A single-file, Firebase-backed voting portal system built for CSK (Club/Student organization use). Includes a voter-facing portal and a SuperAdmin panel for managing candidates, sessions, and live results.

---

## Features

- **Live voting** with real-time Firebase Realtime Database sync
- **Candidate management** — add, remove, and set logos per candidate
- **Session management** — archive sessions, view past results
- **Admin panel** — password-protected with lock/unlock, audit log, live leaderboard
- **Export options** — CSV, JSON, TXT, Print/PDF
- **Vote success modal** — custom logo + 3-second auto-close timer
- **Offline queue** — votes are buffered locally and flushed when Firebase reconnects
- **Idle screen** — configurable portal logo and subtitle

---

## Files

| File | Description |
|------|-------------|
| `CSK-VOTING-SYSTEM.html` | Voter-facing kiosk portal |

Both files are self-contained single-file apps with all CSS and JS inline.

---

## Setup

1. Create a Firebase project at [console.firebase.google.com](https://console.firebase.google.com)
2. Enable **Realtime Database**
3. Open `CSK-VOTING-SYSTEM.html` in a browser (or serve via any static host)
4. In the **Settings** tab of the Admin panel, configure:
   - Admin username & password
   - Portal logo URL (shown on idle screen)
   - Vote success logo URL (shown in the post-vote modal)
   - Session subtitle
   - Secondary Firebase config (optional, for SuperAdmin sync)

---

## Usage

### Voter Portal
- Displays candidate cards; voter taps a card, confirms, and sees the success modal
- Success modal auto-closes after **3 seconds**
- Portal auto-returns to idle screen after inactivity

### Admin Panel
Access by triple-tapping the portal screen or navigating to the admin overlay.

| Tab | Function |
|-----|----------|
| Results | Live vote counts and percentages |
| Candidates | Add/remove candidates, set logos |
| Audit | Full vote log with search |
| Sessions | Archive current session, view past sessions |
| Settings | Credentials, logos, Firebase config |

---

## Security Note

This project uses client-side credential checking for the admin panel. For production use, consider adding Firebase Authentication and Realtime Database security rules to restrict write access.

---

## License

See [LICENSE](./LICENSE) for terms. This project is **source-available but not open source**. Usage requires explicit permission from the repository owner.
