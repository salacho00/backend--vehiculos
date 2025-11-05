#  Proyecto Vehículos - Back - Main

## 🧩 Requisitos previos

Antes de ejecutar el proyecto, asegúrate de tener lo siguiente instalado:

- **Visual Studio Code**  
- **JDK (Java Development Kit)**  
- **Java versión 21**  
- **Postman**  

### 🔧 Extensiones necesarias
Debes instalar las extensiones necesarias en Visual Studio Code para poder ejecutar y probar el proyecto correctamente.  
<!-- Aquí puedes añadir una imagen de las extensiones instaladas -->
<img width="459" height="228" alt="Captura de pantalla 2025-11-05 163853" src="https://github.com/user-attachments/assets/0c69a310-61a1-4de7-bc74-7f80fd15ba77" />

---

## 🚀 Ejecución del proyecto

1. Abre **Visual Studio Code**.  
2. Usa el atajo **Ctrl + O** para abrir la carpeta del proyecto:  
   **vehículos-back-main**  
3. Ve al ícono de **Spring Boot** en la barra lateral.  
4. Da clic en el botón de **ejecución** (marcado con la segunda flecha en la guía).  
<!-- Inserta aquí una imagen de la interfaz de Spring Boot y el botón de ejecución -->
<img width="487" height="507" alt="Captura de pantalla 2025-11-04 160256" src="https://github.com/user-attachments/assets/1de0173b-8e03-4e0f-a220-ec4a7f89c8e9" />


Si todo funciona correctamente, deberías ver un mensaje indicando que la aplicación está corriendo en el **puerto 8080**.  
<!-- Inserta aquí una imagen del log de ejecución mostrando el puerto 8080 -->
<img width="1452" height="230" alt="Captura de pantalla 2025-10-23 094415" src="https://github.com/user-attachments/assets/7340fdbb-7a40-4c9a-996a-7e554af001b2" />

---


## 🧪 Pruebas con Postman

Una vez la aplicación esté corriendo, abre **Postman** para probar los diferentes endpoints del proyecto.

En la parte superior de Postman, selecciona el **tipo de método (POST, GET, PUT o DELETE)** y coloca la **URL correspondiente** con el puerto `8080`.
<img width="1885" height="801" alt="Captura de pantalla 2025-11-04 165301" src="https://github.com/user-attachments/assets/2aa7c3df-ad79-475e-8c07-e46836dd682a" />

---

## 🛠️ Métodos CRUD

### ➕ Crear vehículo
**URL:** **http://localhost:8080/api/vehiculos**  
**Método:** **POST**

Este método permite registrar un nuevo vehículo.  
Como el vehículo contiene una imagen, debes ir al apartado **Body → form-data** en Postman y añadir los siguientes campos:

- **vehiculo** → tipo *Text*  -> y despues pones los datos del vehiculo -> content-type: application/json
- **imagen** → tipo *File*   -> y despues eliges una imagen
<img width="1385" height="427" alt="Captura de pantalla 2025-11-05 160310" src="https://github.com/user-attachments/assets/5eecadc9-f918-431a-ba5e-54e798fb23d1" />

<!-- Inserta aquí una imagen de cómo debe verse el formulario en Postman -->

Finalmente, presiona **Send** para enviar la petición.

---

### 🔍 Buscar todos los vehículos
**URL:** **http://localhost:8080/api/vehiculos**  
**Método:** **GET**
<img width="1408" height="572" alt="Captura de pantalla 2025-11-05 160556" src="https://github.com/user-attachments/assets/fc774a9e-5ad1-4a9f-b1b5-6f72e68d6e19" />

Este método devuelve la lista completa de vehículos registrados.  
No requiere parámetros adicionales.

---

### 🔎 Buscar vehículo por ID
**URL:** **http://localhost:8080/api/vehiculos/{vehiculo_id}**  
**Método:** **GET**

Permite buscar un vehículo específico por su ID.  
Si la respuesta es correcta, obtendrás un **código 200 (OK)**.
<img width="1378" height="528" alt="Captura de pantalla 2025-11-05 160858" src="https://github.com/user-attachments/assets/a3c86c35-ddae-4a9a-ac56-b1ba6615312a" />

<!-- Inserta aquí una imagen del resultado en Postman -->

---

### ✏️ Actualizar vehículo
**URL:** **http://localhost:8080/api/vehiculos/{vehiculo_id}**  
**Método:** **PUT**

Para actualizar un vehículo, sigue los mismos pasos que en **Crear vehículo**, pero con la URL que incluye el ID.  
Presiona **Send** para guardar los cambios.
<img width="1366" height="657" alt="Captura de pantalla 2025-11-05 161055" src="https://github.com/user-attachments/assets/e141db18-d461-405d-bf84-00b23d2e77a7" />

---

### ❌ Eliminar vehículo
**URL:** **http://localhost:8080/api/motos/{vehiculo_id}**  
**Método:** **DELETE**

Permite eliminar un vehículo existente por su ID.  
Si la operación fue exitosa, se mostrará una respuesta con **código 200 (OK)**.
<img width="1377" height="363" alt="Captura de pantalla 2025-11-05 162047" src="https://github.com/user-attachments/assets/f195059f-56ac-4497-957f-fb175fa9105a" />

<!-- Inserta aquí una imagen mostrando la eliminación exitosa -->



---
---

## 🏍️ GESTIÓN DE MOTOS

Para las motos, lo único que cambia es la **URL**: en vez de poner `vehiculos`, debes usar `motos`.

---

### ➕ Crear moto
**URL:** **http://localhost:8080/api/motos**  
**Método:** **POST**

Es muy similar al de vehículos, solo cambia la URL.  
<!-- 📸 Imagen del formulario form-data en Postman -->
<img width="1374" height="640" alt="Captura de pantalla 2025-11-05 165629" src="https://github.com/user-attachments/assets/17fec9e9-f13c-474c-a41e-3cd2aef4d293" />

---

### 🔍 Buscar todas las motos
**URL:** **http://localhost:8080/api/motos**  
**Método:** **GET**

Devuelve la lista de todas las motos registradas.  
<!-- 📸 Imagen mostrando el resultado en Postman -->
<img width="1362" height="587" alt="Captura de pantalla 2025-11-05 165743" src="https://github.com/user-attachments/assets/16e8feb5-5048-4353-9379-c6ffd9c847f2" />

---

### 🔎 Buscar moto por ID
**URL:** **http://localhost:8080/api/motos/{moto_id}**  
**Método:** **GET**

El parámetro se pasa por la URL como se muestra en la imagen.  
<!-- 📸 Imagen del ejemplo de búsqueda por ID -->
<img width="1380" height="512" alt="Captura de pantalla 2025-11-05 165946" src="https://github.com/user-attachments/assets/8f301fda-b9e0-419f-9555-c73726fc9bb7" />

---

### ✏️ Actualizar moto
**URL:** **http://localhost:8080/api/motos/{moto_id}**  
**Método:** **PUT**

Funciona igual que el método de crear moto, pero con **PUT**, por lo que actualiza los datos existentes.  
<!-- 📸 Imagen del ejemplo en Postman -->
<img width="1380" height="658" alt="Captura de pantalla 2025-11-05 170128" src="https://github.com/user-attachments/assets/8471ac19-8205-4e3a-9f1a-1c4202effef9" />

---

### ❌ Eliminar moto
**URL:** **http://localhost:8080/api/motos/{moto_id}**  
**Método:** **DELETE**

Permite eliminar una moto existente por su ID.  
<!-- 📸 Imagen mostrando la eliminación exitosa -->
<img width="1382" height="371" alt="Captura de pantalla 2025-11-05 170252" src="https://github.com/user-attachments/assets/3fa9baa7-4efb-4f21-b467-1bb9e39a2009" />

---

## ✅ Conclusión

Ya sabes cómo ejecutar y probar el proyecto **Vehículos - Back - Main** utilizando **Spring Boot** y **Postman**.  




