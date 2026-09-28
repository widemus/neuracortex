# Neuracortex

A university group project for a fictional organoid-intelligence company, built with React, Next.js and a MySQL-compatible database. Alongside the public company website, the application provides event management and booking flows for webinars and lab excursions.

[Demo](https://neuracortex.vercel.app/)

This is an academic prototype. Use fictional information when exploring it.

## Inspiration

The fictional company concept was inspired by [Cortical Labs](https://corticallabs.com/). Neuracortex was developed as an independent university group project and is not affiliated with Cortical Labs.

## Features

· Browse events and filter by event type or availability, with filter state stored in the URL.
· View event details, book a place, cancel a booking and join a waitlist when an event is full.
· Create an account and access attendee, organiser or administrator interfaces.
· Create and manage events through the organiser interface.
· Manage users and events through the administrator interface.
· Validate submitted data on the server, including event dates, capacity and duplicate bookings.

These workflows are described in the submitted project documentation. This is an academic implementation, and the authentication and authorisation limitations below still apply.

## My contribution — Anton Zahrai (`widemus`)

I worked on the frontend and coordinated the team's development. My contributions included:

· Building the React / Next.js interface, including interactive components, public pages, events, bookings and account screens.
· Creating the custom Tailwind CSS design system and responsive layouts.
· Reviewing teammates' changes and resolving Git merge conflicts.
· Contributing to server-side and database integration.
· Deploying the project with Vercel and TiDB and adjusting the database connection configuration.

This repository is my fork of the [original group repository](https://github.com/polina-batanova/Assignment3_GroupProject). The project documentation credits Polina Batanova with the database schema, event and booking APIs, and route-protection middleware; Yaroslav Razumovskyi with authentication and administration APIs, documentation and presentation preparation. My primary ownership was the frontend, with additional collaboration on integration and deployment.

## Continuing the project

I forked Neuracortex to continue developing it independently. I will be responsible for all future development and maintenance in this fork, including the improvements listed below. The original university application remains a collaborative project with the contributions credited above.

## Technology

· React and Next.js for the web application.
· JavaScript, HTML, CSS and Tailwind CSS for the interface.
· MySQL-compatible SQL through `mysql2` for database access.
· TiDB for the deployed database and Vercel for hosting.
· Git and GitHub for collaboration.

## Code guide

· `app/`: pages and server routes.
· `components/`: shared interface components.
· `lib/db.js`: database connection pool and TLS configuration.
· `lib/auth.js`: authentication/session helpers.
· `public/`: static assets.

## Development setup

The application needs a compatible Node.js installation, npm, and a MySQL-compatible database populated with the project's expected schema. The repository does not currently include a complete database bootstrap script, so installing dependencies alone is not sufficient to reproduce all features.

1. Clone the repository and install the locked dependencies:

   ```sh
   git clone https://github.com/widemus/neuracortex.git
   cd neuracortex
   npm ci
   ```

2. Configure a local `.env.local` with your own database connection string:

   ```dotenv
   DATABASE_URL=mysql://USERNAME:PASSWORD@HOST:PORT/DATABASE
   ```

   Use a database connection compatible with the TLS settings in `lib/db.js`. Do not commit real credentials.

3. Start the development server:

   ```sh
   npm run dev
   ```

4. Open `http://localhost:3000`.

Available additional commands are `npm run lint`, `npm run build` and `npm start`. These are the repository's configured commands, not a claim that they pass in every environment.

## Planned improvements

My priorities for the next stage of development, in order:

1. **Improve the mobile experience.** Add a dedicated mobile navigation menu so users do not have to rely on footer links, and improve layouts and usability on smaller screens.
2. **Add Google sign-in.** Allow users to register and sign in with their Google account.
3. **Implement a full redesign.** Bring the new design I have already planned for a long time into the application. This is the final planned stage because it requires substantial preparation and implementation work after the earlier improvements.
