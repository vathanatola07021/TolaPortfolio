# Developer Portfolio — Django & Google Stitch UI

A high-performance, cinematic 3D developer portfolio built with **Python Django** and styled with the Google Stitch design (**Website Typography Selector: Final Screen — Syne + Plus Jakarta Sans + Cosmic Float Particles + 3D Tilt Cards**).

---

## 🌟 Key Features

1. **Google Stitch UI Implementation & 3D Spatial Engine**:
   - **Interactive 3D WebGL Spatial Simulator**: Integrated Three.js spatial viewport featuring a procedural bioluminescent mesh with undulating physics tentacles, 480 depth-blended particles, drag-to-rotate interaction, scroll zoom, and live telemetry HUD (FPS, Vertices, Drawcalls). Includes controls to toggle wireframe lattice, particle cloud, specular shader glow, and perspective reset.
   - **Interactive 3D Tilt Cards**: Bento grid project cards with instantaneous cursor tracking and snappy spring-back physics (`cubic-bezier(0.175, 0.885, 0.32, 1.275)`).
   - **Proximity-Aware Magnetic Snap**: High-tension magnetic pull on buttons, pills, mark, and navigation links.
   - **Navigation Capsule Particle Sparks**: Dual-layer canvas with glowing neon wakes and lingering zero-G floaty cosmic drift particles (`#navAuraCanvas`).
   - **Three.js 3D Background**: Real-time WebGL interactive cosmic node network on a Fibonacci sphere with parallax mouse response and scroll depth.
   - **Typography**: Expressive headline hierarchy in `Syne` (800 weight with tight negative letter-spacing) paired with `Plus Jakarta Sans` for body legibility and `JetBrains Mono` for telemetry and code.

2. **Django Backend Architecture**:
   - **`Profile` Model**: Editable name, roles, typewriter animation phrases, bio quote, descriptions, badges, and social links.
   - **`Project` Model**: Bento grid projects with column span (`w4`, `w2`, `w3`), tags, live links, GitHub URLs, terminal output commands, and technology chips.
   - **`SkillCategory` & `Skill` Models**: Categorized tech stack (Cloud & Ops, Backend & Data, Graphics & Frontend).
   - **`EducationFact` Model**: Key-value data table for degree, graduation date, GPA, honors, and certifications.
   - **`Article` Model**: Publications and tech blog posts with reading times and external URLs.
   - **`ContactMessage` Model**: Live instant messaging form with AJAX submission and backend inbox logging.
   - **Django Admin CMS**: Pre-configured admin panel at `/admin/` to manage all portfolio data dynamically.

---

## 🚀 How to Run

### Option 1: Quick Launch (Windows)
Double-click [`run.bat`](file:///c:/Users/LAI%20VATHANATOLA/Desktop/My%20Portfolio/run.bat) or run in terminal:
```powershell
.\run.bat
```

### Option 2: Command Line
```powershell
& "C:\Users\LAI VATHANATOLA\anaconda3\python.exe" manage.py runserver 127.0.0.1:8000
```

Open your browser at:
- **Portfolio Website**: [http://127.0.0.1:8000/](http://127.0.0.1:8000/)
- **Admin Panel**: [http://127.0.0.1:8000/admin/](http://127.0.0.1:8000/admin/)

---

## 🔐 Admin Credentials

A superuser account is pre-configured for local editing:
- **Username**: `admin`
- **Password**: `admin123`

---

## 📁 Project Structure

```
My Portfolio/
├── config/
│   ├── settings.py          # Django settings (apps, templates, static/media)
│   ├── urls.py              # Root URL router
│   └── wsgi.py
├── portfolio/
│   ├── admin.py             # Django admin panel configuration
│   ├── models.py            # Database models (Profile, Project, Skill, etc.)
│   ├── views.py             # Index page & AJAX contact handler
│   ├── urls.py              # App URLs
│   ├── tests.py             # Unit test suite
│   └── management/commands/
│       └── seed_portfolio.py # Database seeder from Stitch design
├── static/
│   ├── css/
│   │   └── portfolio.css    # Full Stitch design CSS (Glassmorphism, 3D tilt, Glows)
│   └── js/
│       ├── portfolio.js     # Physics, magnetic snaps, particles, typewriter, AJAX
│       └── three-scene.js   # Three.js 3D cosmic network background
├── templates/
│   ├── base.html            # Base layout with Three.js canvas & nav capsule
│   └── portfolio/
│       └── index.html       # Portfolio landing page
├── manage.py
├── run.bat
└── db.sqlite3
```
