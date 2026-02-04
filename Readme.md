# Entorno Java con Kali Linux y Apache NetBeans

Imagen Docker lista para usar en cursos de **Java**, con **OpenJDK**, **Maven**, **Gradle** y **Apache NetBeans**, accesible desde el navegador.

---

## Opción 1: Usar Docker Compose (recomendado)

Desde el directorio del proyecto:

```bash
docker-compose up -d
```

Luego abre en el navegador:

👉 http://localhost:3011

Todo tu trabajo se guarda automáticamente en la carpeta `config/`.

---

## Opción 2: Usar `docker run` (en windows usar PowerShell)

### Paso 1: Desde el directorio del proyecto, crear la carpeta `config`


#### Windows / Linux / macOS

```bash
mkdir config
```

---

### Paso 2: Ejecutar el contenedor

Ejecuta el comando **desde el mismo directorio donde está la carpeta `config`**.

```bash
docker run -d --name kali-javadev -p 3011:3000 -v "${PWD}/config:/config" augustosalazar/kali-netbeans-java:2
```

Luego abre en el navegador:

👉 http://localhost:3011

---

## ¿Dónde guardar mi trabajo?

Guarda **todo dentro del escritorio o carpetas visibles del sistema**.

Internamente, todo se almacena en la carpeta `config/` del host, por lo que **no se pierde nada aunque el contenedor se detenga o elimine**.

---

## Requisitos

- Docker instalado
- Navegador web moderno

No necesitas Java ni NetBeans instalados en tu computador.

