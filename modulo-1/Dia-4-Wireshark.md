# Día 4: Análisis de Tráfico con Wireshark

## 🧠 Conceptos Clave
- Wireshark es un analizador de tráfico que actúa como un "inspector de aduanas" en la red.
- El Handshake TCP consta de 3 pasos: SYN (Hola) -> SYN-ACK (Hola de vuelta) -> ACK (Confirmo).
- El filtrado es vital para no ahogarse en datos. Sintaxis usada: `ip.addr == X.X.X.X` y `tcp.flags.syn == 1`.

## 🛠️ Práctica Realizada
1. Capturé tráfico en mi interfaz `eth0`.
2. Generé tráfico usando el comando `curl -I http://scanme.nmap.org`.
3. Filtré los paquetes y logré identificar el paquete **SYN** y el **SYN-ACK**.
4. Analicé una petición HTTP y comprobé que el texto viaja **sin cifrar**. ¡Entendí la importancia de HTTPS!

## 💡 Reflexión
Wireshark es una herramienta fundamental tanto para atacantes (para robar datos sin cifrar o entender servicios) como para defensores (para detectar tráfico malicioso).
<img width="878" height="654" alt="wireshark04" src="https://github.com/user-attachments/assets/9c912ac1-ac5e-40dd-8e1d-0cb78bb2d8d7" />
<img width="969" height="703" alt="wireshark03" src="https://github.com/user-attachments/assets/17ba747f-22cd-44ab-a9c5-8bb2f1b846f8" />
<img width="954" height="701" alt="wireshark02" src="https://github.com/user-attachments/assets/d81322cd-1f71-4849-9d75-342e1d70a572" />
<img width="964" height="714" alt="wireshark01" src="https://github.com/user-attachments/assets/21605767-5fcc-4e7a-98b7-f7d0a6abd4b4" />
