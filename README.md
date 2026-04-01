# PrayerConnect

PrayerConnect is een gratis, mobielvriendelijk gebedsplatform voor kerken. Deze deploy gebruikt een GitHub Pages frontend met Supabase voor auth, database en row-level security.

## Live

- App: https://simplederpyman.github.io/prayerconnect/
- Repo: https://github.com/simplederpyman/prayerconnect
- Supabase project: `iatehwjwhmhvcujroxka`

## Wat zit erin

- publieke gebedsmuur per kerk
- login en registratie voor leiders
- automatisch herstellen/aanmaken van kerk + admin membership bij dashboard toegang
- leidersdashboard met verzoeken, snelle stats en events
- openbare inzendingen met goedkeuringsflow

## Belangrijke routes

- `#/`
- `#/login`
- `#/register`
- `#/dashboard`
- `#/dashboard/verzoeken`
- `#/dashboard/nieuw`
- `#/dashboard/team`
- `#/dashboard/instellingen`
- `#/kerk/:slug/gebedsmuur`
- `#/kerk/:slug/delen`

## Supabase

Het schema staat in `supabase/schema.sql`.

Belangrijk:
- multi-tenant per kerk via `church_id`
- publieke gebedsmuur zonder login
- leidersdashboard met auth en RLS
- publieke leesrechten alleen voor goedgekeurde openbare verzoeken

## Volgende stap

- eventbeheer uitbreiden
- echte teamweergave koppelen
- mock onderdelen verder vervangen door live data
