

# Sécurité

Contact : [security@cal.com](mailto:security@cal.com)

Basé sur [https://supabase.com/.well-known/security.txt](https://supabase.com/.well-known/security.txt)

Chez Cal.com, nous considérons la sécurité de nos systèmes comme une priorité absolue. Cependant, peu importe les efforts que nous mettons dans la sécurité du système, des vulnérabilités peuvent toujours être présentes.

Si vous découvrez une vulnérabilité, nous aimerions en être informés afin de pouvoir prendre des mesures pour y remédier le plus rapidement possible. Nous vous demandons de nous aider à mieux protéger nos clients et nos systèmes.

## Vulnérabilités hors de portée

- Clickjacking sur des pages sans actions sensibles.
- CSRF non authentifié/déconnexion/connexion.
- Attaques nécessitant une interception man-in-the-middle (MITM) ou un accès physique à l'appareil d'un utilisateur.
- Toute activité pouvant entraîner une interruption de notre service (DoS).
- Usurpation de contenu et problèmes d'injection de texte sans montrer de vecteur d'attaque / sans pouvoir modifier HTML/CSS.
- Usurpation d'email.
- Absence de DNSSEC, CAA, en-têtes CSP.
- Absence de flag Secure ou HTTP uniquement sur des cookies non sensibles.
- Liens morts.

## Veuillez faire ce qui suit

- Envoyez vos découvertes par e-mail à [security@cal.com](mailto:security@cal.com).
- Ne lancez pas de scanners automatisés sur notre infrastructure ou notre tableau de bord. Si vous souhaitez le faire, contactez-nous et nous mettrons en place un environnement de test pour vous.
- Ne tirez pas profit de la vulnérabilité ou du problème que vous avez découvert, par exemple en téléchargeant plus de données que nécessaire pour démontrer la vulnérabilité ou en supprimant ou modifiant les données d'autres personnes.
- Ne révélez pas le problème à d'autres avant qu'il ne soit résolu.
- N'utilisez pas d'attaques sur la sécurité physique, d'ingénierie sociale, de déni de service distribué, de spam ou d'applications de tiers.
- Fournissez suffisamment d'informations pour reproduire le problème, afin que nous puissions le résoudre aussi rapidement que possible. Habituellement, l'adresse IP ou l'URL du système affecté et une description de la vulnérabilité suffisent, mais des vulnérabilités complexes peuvent nécessiter des explications supplémentaires.

## Ce que nous promettons

- Nous répondrons à votre rapport dans les 3 jours ouvrables avec notre évaluation du rapport et une date de résolution prévue.
- Si vous avez suivi les instructions ci-dessus, nous ne prendrons aucune mesure juridique à votre encontre en ce qui concerne le rapport.
- Nous traiterons votre rapport avec une stricte confidentialité et ne transmettrons pas vos informations personnelles à des tiers sans votre autorisation.
- Nous vous tiendrons informé des progrès vers la résolution du problème.
- Dans les informations publiques concernant le problème signalé, nous mentionnerons votre nom en tant que découvreur du problème (sauf si vous souhaitez le contraire).
- Nous nous efforçons de résoudre tous les problèmes aussi rapidement que possible, et nous aimerions jouer un rôle actif dans la publication finale du problème une fois résolu.

---