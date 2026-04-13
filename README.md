<div align="center">

# KNAP (Known Nearby Access Points)

Sniffer pasivo de radiofrecuencia especializado en identificar redes WiFi conocidas por dispositivos cercanos mediante la captura de peticiones de sonda (Probe Requests).

<br>

<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" />
<img src="https://img.shields.io/badge/Scapy-FFD200?style=for-the-badge&logo=python&logoColor=black" alt="Scapy" />
<img src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black" alt="Linux" />

</div>

---

### ✦ Descripción

KNAP detecta en tiempo real los ESSID (nombres de red) que los dispositivos móviles y equipos cercanos están buscando para conectarse automáticamente. Esta técnica permite enumerar a qué redes confiaría un objetivo potencial para realizar ataques de punto de acceso falso o reconocimiento de ubicación.

### ✦ Características

*   **Captura en Tiempo Real**: Visualización inmediata de dispositivos (MAC) y las redes por las que consultan.
*   **Identificación de Fabricantes**: Integración opcional de base de datos OUI para mostrar el fabricante del dispositivo detectado.
*   **Registro Automático**: Almacenamiento de hallazgos en un archivo `essids.txt` sin duplicados.
*   **Detección de Interfaz**: Verificación automática del modo monitor en la interfaz de red seleccionada.

### ✦ Instalación y Uso

1.  Clone el repositorio:
    ```bash
    git clone https://github.com/samilososami/knap.git
    cd knap
    pip3 install -r requirements.txt
    ```
2.  Ejecute la herramienta especificando su interfaz en modo monitor:
    ```bash
    python3 knap.py -i <interfaz>
    ```

Para mostrar fabricantes:
```bash
python3 knap.py -i <interfaz> -oui oui.txt
```

---

> [!CAUTION]
> Esta herramienta requiere que la interfaz de red soporte modo monitor. El uso de esta técnica debe limitarse a fines éticos y bajo consentimiento previo.