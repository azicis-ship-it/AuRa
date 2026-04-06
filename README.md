# ◈ AURA CHECK

> "what's your aura today?"

Una web app para teens que lee tu "aura" diaria mediante un quiz de 5 preguntas. Diseñada para ser viral, adictiva, y monetizable.

---

## 🚀 DEPLOY EN 5 MINUTOS (Vercel - Gratis)

### Opción A: Desde GitHub (recomendado)

1. **Crea un repo en GitHub** y sube esta carpeta
2. **Ve a [vercel.com](https://vercel.com)** → Sign up con GitHub
3. **Click "New Project"** → Importa tu repo
4. **Click "Deploy"** → Listo. Te da una URL tipo `aura-check.vercel.app`

### Opción B: Desde terminal

```bash
npm i -g vercel
cd aura-check
vercel
```

Sigue las instrucciones. En 2 minutos tienes URL pública.

### Dominio personalizado (opcional)

Compra un dominio en Namecheap (~$10/año). Ejemplo: `auracheck.app`
En Vercel → Settings → Domains → Agrega tu dominio.

---

## 💰 CÓMO MONETIZAR

### 1. Links de Afiliado (Ingreso principal)

En `app/page.js`, busca `matchLinks` en cada aura. Reemplaza los `"#"` con tus links de afiliado:

```js
matchLinks: [
  "https://www.amazon.com/dp/XXXXX?tag=TU-AFFILIATE-ID",
  "https://www.shein.com/xxx?ref=TU-ID",
  ...
],
```

**Programas de afiliados recomendados para teens:**
- **Amazon Associates** → Todo tipo de productos (4-10% comisión)
- **SHEIN Affiliate** → Moda accesible (10-20% comisión)
- **AliExpress Affiliate** → Accesorios baratos (8-12%)
- **Depop/Vinted** → Reventa (busca programas de referidos)
- **CJ Affiliate / ShareASale** → Marcas como Alo Yoga, etc.

**Tip:** Pon productos reales que cuesten $10-40. Es el rango donde los teens compran sin pedir permiso.

### 2. Suscripción PRO ($2.99/semana)

Para implementar pagos reales:
- **Stripe** (más profesional) o **RevenueCat** (si haces app nativa)
- El botón PRO ya está en el UI. Solo conecta el payment flow.

Features PRO que puedes agregar:
- Compatibilidad de auras entre amigos
- Historial de auras con gráfico
- Auras exclusivas PRO
- Forecast semanal personalizado

### 3. Contenido patrocinado

Cuando tengas +10k usuarios:
- Marcas de skincare, joyería, y accesorios pagan por ser "aura match"
- Cobra $200-500 por producto destacado
- Los teens no lo ven como publicidad, lo ven como parte del resultado

---

## 📱 HACERLA INSTALABLE (PWA)

La app ya tiene `manifest.json`. Los usuarios pueden:
- **iOS**: Safari → Compartir → "Agregar a pantalla de inicio"
- **Android**: Chrome muestra banner automático de "Instalar"

Se ve y funciona como app nativa. Sin pasar por App Store.

---

## 📣 ESTRATEGIA DE DISTRIBUCIÓN

### TikTok (canal principal)
1. Graba tu resultado de aura → "no way I got Void 🌀"
2. Link in bio a la web
3. Pide a 5-10 teens que hagan lo mismo
4. El formato de "share aura card" genera imagen lista para stories

### Instagram
- El botón "share aura" genera imagen 1080x1920 perfecta para stories
- Usa hashtags: #auracheck #whatsmyaura #auratiktok

### Growth Hack
- La mecánica de "coleccionar 5 auras" los trae de vuelta cada día
- La racha (streak) genera FOMO si pierden un día
- La "6ta aura secreta" genera misterio y conversación

---

## 🔧 DESARROLLO LOCAL

```bash
npm install
npm run dev
```

Abre `http://localhost:3000`

---

## 📁 ESTRUCTURA

```
aura-check/
├── app/
│   ├── layout.js      ← Metadata, fonts, PWA config
│   ├── page.js         ← Toda la app (quiz, resultados, vault, share)
│   └── globals.css     ← Estilos globales y animaciones
├── public/
│   └── manifest.json   ← PWA manifest
├── next.config.js
├── package.json
└── README.md
```

---

## 🎯 PRÓXIMOS PASOS

1. [ ] Subir a GitHub + Deploy en Vercel
2. [ ] Registrarte en Amazon Associates / SHEIN Affiliate
3. [ ] Reemplazar los `matchLinks` con tus links de afiliado
4. [ ] Agregar iconos reales (icon-192.png, icon-512.png) en /public
5. [ ] Crear cuenta TikTok para @auracheck
6. [ ] Publicar primer video mostrando tu aura
7. [ ] Cuando tengas tracción: implementar Stripe para PRO

---

*Built with Next.js 15 + React. Zero dependencies extra.*
