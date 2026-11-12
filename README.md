# Sobre el proyecto de-mantenimiento-de-sensores-y-repuestos:
Aplicación de consola en Python para un centro técnico de sensores ambientales. Permite abrir órdenes de trabajo (OT), registrar servicios, repuestos y pruebas de calibración, luego cerrar y facturar las órdenes. Todos los movimientos se guardan en archivos CSV/TXT para conservar los datos y genera reportes de facturación y de inventario.

# Configuracion inicial:
1. Installar Python.
2. Descargar el proyecto aquí adjunto (proyectofinal.py).
3. Preparar la base de datos local: ubica los archivos equipos.csv, servicios.csv, repuestos.csv, en la misma carpeta principal (que llamamos proyectofinal) que el script. También las carpetas ordenes_abiertas y ordenes_cerradas. 
# De todas formas para más facilidad, en la carpeta .zip ya vienen todos los archivos necesarios para correr el programa.

# Estructura de archivos:
1. El archivo equipos.csv es esencial para que el programa cargue los equipos disponibles y ocupados. Este archivo contiene equipo_id (EQ01, EQ02...), cliente, tipo (fijo/móvil), modelo, estado (disponible/ocupado).
2. El archivo servicios.csv contiene codigo (S01, S02...), descripcion, costo_fijo, costo_movil.
3. El archivo repuestos.csv contiene codigo(R01, R02...), descripcion, costo_compra, precio_venta, stock (cuántos disponibles).
4. Se necesitan también dos carpetas para ir registrando allí los .txt según las órdenes que se vayan trabajando y posteriormente cerrando:
4.1 ordenes_abiertas
  Registro delimitado por |: ORDEN, SERVICIO, REPUESTO, PRUEBA
  ORDEN|OT001|EQ01|2026-11-10|ABIERTA
  SERVICIO|S01|60000
  REPUESTO|R01|2|15000|8000
  PRUEBA|INICIAL|8.0
4.2 ordenes_cerradas
  ordenes_cerradas/  ·  columnas: Directorio de órdenes finalizadas; una orden cerrada conserva historial íntegro.
  (archivos OTxxxx.txt)
