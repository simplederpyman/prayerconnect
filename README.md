# PrayerConnect

PrayerConnect is een gratis, mobielvriendelijk gebedsplatform voor kerken.

## Live app

- GitHub Pages: https://simplederpyman.github.io/prayerconnect/
- Repo: https://github.com/simplederpyman/prayerconnect
- Supabase project: https://supabase.com/dashboard/project/iatehwjwhmhvcujroxka

## Wat hier nu live draait

Deze repository bevat een **bruikbare statische GitHub Pages app** die direct met Supabase praat vanuit de browser.

Functionaliteit:
- Registreren van leider + kerk
- Inloggen
- Publieke gebedsmuur per kerk via hash-route
- Publiek verzoek indienen
- Dashboard voor leiders
- Goedkeuren van openbare verzoeken
- Markeren als beantwoord
- Nieuw verzoek toevoegen vanuit dashboard

## Stack

- Pure static HTML/CSS/JS voor GitHub Pages compatibiliteit
- Supabase JS client via CDN
- Supabase database + auth + RLS

## Routes

Hash-routes omdat GitHub Pages geen server-side routing heeft:
- `#/`
- `#/login`
- `#/register`
- `#/kerk/[slug]/gebedsmuur`
- `#/kerk/[slug]/delen`
- `#/dashboard`
- `#/dashboard/verzoeken`
- `#/dashboard/nieuw`

## Supabase

Project ref: `iatehwjwhmhvcujroxka`

Schema staat in `supabase/schema.sql` en is toegepast op het project.

## Opmerking

Voor GitHub Pages is gekozen voor een pure static app in plaats van de oorspronkelijke Vite-buildflow, zodat de site zonder extra CI of secrets echt bruikbaar live kan staan.
