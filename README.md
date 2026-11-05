# ANDON – Limhjul 3 och 4

Mobilanpassad testapp för operatörer och ansvarig. Fyra knappar: Material, Ställ, Kvalitet, Hjälp. Kvittens/nekande, kommentarer och tidslogg.

## Publicering med Render
1. Logga in på https://dashboard.render.com och välj New > Blueprint.
2. Koppla GitHub-repositoryt Mahlander/andon-app.
3. Ange en egen stark MANAGER_PIN som miljövariabel.
4. Publicera. Render skapar HTTPS-adressen.
5. För pushnotiser: generera VAPID-nycklar med `npx web-push generate-vapid-keys` och lägg VAPID_PUBLIC_KEY, VAPID_PRIVATE_KEY och VAPID_EMAIL i Render som miljövariabler. Lägg aldrig hemliga nycklar i GitHub.

## Begränsningar
Detta är en prototyp, inte ett säkerhetskritiskt larmsystem. På gratis Render kan servern somna och data gå förlorade vid omstart. För skarp drift behövs databas, säker inloggning, backup och övervakning. Operatörens vy är inte autentiserad. Push fungerar först efter serverkonfiguration och användarens tillstånd.