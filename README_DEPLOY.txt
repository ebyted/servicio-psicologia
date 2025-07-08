# Instrucciones para subir y servir la página en tu VPS (puerto 8021)

1. **Sube todos los archivos de la carpeta a tu VPS**
   - Incluye: `index.html`, `propuesta1.html`, `propuesta2.html`, `propuesta3.html`, `server.js`, `package.json`

2. **Instala Node.js en tu VPS** (si no lo tienes):
   ```sh
   sudo apt update
   sudo apt install nodejs npm -y
   ```

3. **Instala las dependencias**:
   ```sh
   npm install
   ```

4. **Inicia el servidor en el puerto 8021**:
   ```sh
   node server.js
   ```
   o
   ```sh
   npm start
   ```

5. **Abre tu navegador y accede a:**
   
   `http://TU_IP_DEL_VPS:8021`

---

**Nota:**
- Si quieres que el servidor siga corriendo después de cerrar la terminal, usa `pm2` o `nohup`:
  ```sh
  npm install -g pm2
  pm2 start server.js
  ```
- Asegúrate de que el puerto 8021 esté abierto en el firewall de tu VPS.
