# Análisis de Seguridad de Red Local

Este proyecto documenta un análisis de seguridad de la red local utilizando herramientas como Nmap. El objetivo es identificar los dispositivos conectados a la red y realizar un escaneo de puertos para evaluar los servicios activos en el router del ISP y otros dispositivos IoT.

## Tabla de Contenidos
1. [Introducción](#introducción)
2. [Objetivos](#objetivos)
3. [Herramientas Utilizadas](#herramientas-utilizadas)
4. [Metodología](#metodología)
5. [Resultados](#resultados)
6. [Análisis de Resultados](#análisis-de-resultados)
7. [Conclusiones](#conclusiones)
8. [Referencias](#referencias)

## Introducción
La seguridad en redes locales es fundamental, especialmente en entornos donde se utilizan dispositivos inteligentes. Con el creciente número de dispositivos IoT en el hogar, es crucial asegurarse de que estén correctamente configurados y no presenten vulnerabilidades que puedan ser explotadas por atacantes. Este proyecto se centra en aprender y aplicar técnicas de escaneo de redes para identificar vulnerabilidades potenciales.

## Objetivos
- **Identificar dispositivos conectados**: Detectar todos los dispositivos que están activos en la red local.
- **Escanear puertos abiertos**: Evaluar la superficie de ataque del router y otros dispositivos mediante el escaneo de puertos.
- **Documentar servicios activos**: Analizar los servicios que están expuestos al mundo exterior y su potencial de riesgo.

## Herramientas Utilizadas
- **Nmap**: Una herramienta de código abierto para escaneo de redes y auditoría de seguridad.
- **Kali Linux**: Un sistema operativo basado en Debian, especialmente diseñado para pruebas de penetración y auditorías de seguridad.

## Metodología
1. **Identificación de la red**: Se utilizó el comando `ifconfig` para identificar la dirección IP del router y la configuración de la red.
2. **Escaneo de dispositivos**: Se ejecutó Nmap para detectar dispositivos conectados utilizando el siguiente comando:
   ```bash
   sudo nmap -sn 192.168.1.0/24

    Escaneo de puertos: Se escanearon los puertos abiertos del router con el siguiente comando:

    bash

    sudo nmap 192.168.1.1

## Resultados

    Dispositivos detectados:
        Router: Huawei (192.168.1.1)
        Foco inteligente: GE Lighting (192.168.1.52)
        Dispositivo Amazon: Amazon Technologies (192.168.1.54)

    Puertos abiertos en el router:
        53/tcp: open (domain)
        80/tcp: open (http)

## Análisis de Resultados

El escaneo reveló dos puertos abiertos en el router, lo cual indica que hay servicios activos que pueden ser accesibles desde la red externa. Es importante evaluar la configuración de estos servicios para mitigar riesgos. Por ejemplo, el puerto 80 es comúnmente utilizado para servidores web, por lo que es recomendable asegurarse de que no haya vulnerabilidades conocidas.
## Conclusiones

El escaneo de la red local ha permitido identificar los dispositivos conectados y los puertos abiertos en el router. Esta información es valiosa para mejorar la seguridad de la red y tomar medidas adecuadas para proteger los dispositivos conectados. Se recomienda realizar auditorías de seguridad periódicas y mantener el firmware de los dispositivos actualizado.
## Referencias

    Nmap Official Documentation
    Kali Linux Official Documentation

## Notas Finales

Este proyecto es parte de un esfuerzo más amplio para aprender sobre ciberseguridad y cómo proteger mejor las redes domésticas. Se anima a otros a realizar análisis similares y compartir sus hallazgos.
