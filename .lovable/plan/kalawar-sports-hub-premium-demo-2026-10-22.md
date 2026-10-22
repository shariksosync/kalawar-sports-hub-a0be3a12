# Kalawar Sports Hub - Premium Demo

A polished demo portal using mock data only (no database). Data is kept in the browser so registrations, uploads, likes and follows persist during a demo session. No "demo role" switchers or testing tools anywhere - every user goes through real-looking login and registration pages.

## Visual direction

Dark, premium sports look: deep charcoal background, warm gold accent, bold condensed display headings (Bebas Neue style) with a clean body font, glassy cards, large action photography (generated images), subtle motion.

## Pages

**Home (/)**

- Sticky navbar: Home, Kalawar, GYM & Fitness, Sports Academy, Media, plus Login / account menu.
- Carousel directly under navbar, 5 slides, auto-play with arrows and dots:
  1. Welcome slide: headline + text on the left, 4 normal-sized boxes in a 2x2 grid on the right (Kalawar, GYM & Fitness, Sports Academy, Media).
  2. Kalawar championships highlight
  3. Featured gyms
  4. Sports academies spotlight
  5. Media community / trending creators
- Below: stats strip, featured partners, latest media, call-to-action to join as partner, footer.

**Kalawar** - your existing Kalawar project ("Kalawar_main_website_6_aug") is used exactly as it is, not recreated or modified. It runs on its own system, which cannot run inside this app, so it stays a separate website (hosted as it is today). The Kalawar box and navbar link open it, just like they do now.

**GYM & Fitness (/gyms)** - searchable/filterable list of registered gyms (city, facilities, price), gym detail page, "Join as a Partner" button.

- /gyms/register - multi-step registration form (owner, gym details, plans, facilities).
- /gyms/login - dedicated gym login.
- Gym admin panel: Dashboard (KPIs, revenue chart), Members, Membership Plans, Subscriptions (active/expiring/expired, renewals), Employees/Trainers, Attendance, Sales & Revenue reports (by month/plan, export CSV), Expenses, Gym Profile & Settings.

**Sports Academy (/academies)** - list of academies (sport, city, age groups), detail page, "Join as a Partner".

- /academies/register and /academies/login.
- Academy admin panel: Dashboard, Students, Batches & Schedules, Coaches/Staff, Fee Collection & Payments, Attendance, Events & Tournaments, Performance/Progress reports, Revenue reports, Profile & Settings.

**Media (/media)** - Instagram-style feed and explore grid of videos and images, creator profiles, stream videos.

- Guests can browse, stream and view profiles; any action (upload, like, subscribe, follow, follow request, comment) opens a "Please register / log in first" prompt.
- Signed-in users: upload video/image, like, comment, subscribe, follow, send follow requests (accept/decline, mutual followers), notifications, own profile with followers/following.
- /media/register and /media/login.

## Shared login

One account system across the app. A single login page with tabs for Media, GYM & Fitness, Sports Academy, and Kalawar members (player, coach, referee, club, state association, district association). Any account type can use Media; gym and academy accounts also get their admin panel. Pre-made sample accounts exist so the demo looks populated (shown as a small "sample credentials" note only on login pages).

## Technical details

- TanStack routes per page; admin panels under a protected layout per partner type.
- Mock data modules (gyms, academies, members, posts, users) + a client-side store persisted to localStorage; uploads stored as local preview URLs.
- shadcn components, recharts for reports, design tokens in styles.css, generated hero/slide images.
- Unique page titles/descriptions for every route.

## Open item

- The web address where your Kalawar project is running, so the Kalawar link points to it (a placeholder is used until you share it).
- Kalawar members sign in to Media with sample Kalawar-role accounts here; true single sign-on with the Kalawar site is not possible because it is a separate system.