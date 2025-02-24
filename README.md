# Cifrado de Flujo con XOR

## Descripción

Este proyecto implementa un esquema básico de cifrado y descifrado utilizando la operación XOR con un keystream generado mediante un generador de números pseudoaleatorios (PRNG). Se exploran las implicaciones de reutilizar el keystream y su longitud en la seguridad del cifrado.

## Objetivos

- Comprender el concepto de un keystream y su importancia en los cifrados de flujo.
- Implementar un esquema básico de cifrado y descifrado utilizando XOR.
- Analizar las implicaciones de la reutilización del keystream y su longitud en la seguridad.

## Requisitos

- Python 3.x
- Jupyter Notebook (opcional, pero recomendado)

## Instalación

1. Clona el repositorio:
   ```bash
   git clone <URL_DEL_REPOSITORIO>
   ```
2. Navega al directorio del proyecto:
   ```bash
   cd <NOMBRE_DEL_REPOSITORIO>
   ```

## Uso

1. Abre el Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
2. Ejecuta el archivo `Stream_Cipher.ipynb` paso a paso para ver la generación del keystream, el cifrado y el descifrado de mensajes.

## Implementación

### 1. Generación de Keystream

La función genera un keystream pseudoaleatorio basado en:

- Un PRNG básico.
- Una clave (seed/nonce) para inicializar el PRNG.
- Un keystream con al menos la misma longitud que el mensaje a cifrar.

### 2. Cifrado

La función de cifrado toma un mensaje en texto plano y lo cifra utilizando la operación XOR con el keystream generado.

### 3. Descifrado

La función de descifrado toma el mensaje cifrado y lo descifra utilizando la misma operación XOR con el keystream. El resultado debe ser idéntico al mensaje original.

## Preguntas y Reflexiones

1. ¿Qué sucede cuando cambias la clave utilizada para generar el keystream?
2. ¿Qué riesgos de seguridad existen si reutilizas el mismo keystream para cifrar dos mensajes diferentes?
3. ¿Cómo afecta la longitud del keystream a la seguridad del cifrado?
4. ¿Qué consideraciones debes tener al generar un keystream en un entorno real?

## Pruebas

Se incluyen pruebas unitarias para validar el funcionamiento correcto del cifrado y descifrado. Para ejecutar las pruebas, usa:

```bash
pytest test_stream_cipher.py
```
