# U4S8 — Rodriguez Sepulveda Jose Manuel

## Demo en vivo (producción)
https://u4s8-rodriguez-sepulveda-jose-manuel.onrender.com

## Qué hace este proyecto
Este proyecto es una aplicación web desarrollada con Django que permite gestionar una vitrina de servicios.

La aplicación permite a los usuarios consultar los servicios disponibles y, mediante autenticación, gestionar sus propios registros. El proyecto integra una base de datos MySQL y cuenta con funcionalidades de autenticación, sesiones, operaciones CRUD, búsqueda y paginación.

El proyecto fue desarrollado y mejorado progresivamente durante las cuatro unidades del curso, pasando de una estructura web estática a una aplicación dinámica desplegada en producción.

## Stack técnico
Django + MySQL (Aiven) + Tailwind CSS + Render

## Cómo se prueba el aislamiento por usuario
Se implementaron las funciones de registro, inicio y cierre de sesión utilizando django.contrib.auth. Cada usuario puede consultar, crear, editar y eliminar únicamente sus propios servicios.

Prueba de aislamiento
Se registraron dos cuentas de prueba: usuario_a y usuario_b, y se crearon dos servicios con cada una. Al iniciar sesión con usuario_b, solo se mostraron sus propios servicios, sin acceder a los de usuario_a.

También se intentó editar y eliminar un servicio de usuario_a escribiendo directamente su ID en la URL mientras estaba iniciada la sesión de usuario_b. En ambos casos, el sistema respondió con un error 404, lo que confirmó la restricción de acceso por propietario.

## Historial de unidades
- Unidad 1: portafolio estático con HTML5 + Tailwind
- Unidad 2: modelo Servicio migrado a MySQL, deploy dinámico en Render
- Unidad 3: CRUD completo con ModelForms + autenticación y sesiones
- Unidad 4: paginación, búsqueda, UI review y defensa final