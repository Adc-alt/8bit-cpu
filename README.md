# Crear README.md con la estructura solicitada por el usuario

readme_content = """
# 🧠 8bit-CPU from Scratch
**Inspirado en el ordenador de Ben Eater – construido desde cero con aprendizaje y errores incluidos.**

---

## 📋 Tabla de Contenidos

1. [Motivación](#motivación)  
2. [Fases del Proyecto](#fases-del-proyecto)  
3. [Errores y Decisiones](#errores-y-decisiones)  
4. [Capítulos Técnicos](#capítulos-técnicos)  
5. [Qué aprendí](#qué-aprendí)  
6. [Cómo ejecutarlo / usarlo](#cómo-ejecutarlo--usarlo)

---

## 💡 Motivación

Este proyecto nace de mi interés por entender cómo funciona un ordenador a bajo nivel. En lugar de solo ver vídeos, decidí replicarlo desde cero, con mis propias pruebas, errores, mejoras y documentación.

---

## 🔨 Fases del Proyecto

1. **Diseño y planificación.**  
2. **Construcción física (placa/breadboard).**  
3. **Programación de la EEPROM.**  
4. **Creación del microcódigo.**  
5. **Añadir nuevas instrucciones.**  
6. **Debugging y mejora.**

---

## 🐞 Errores y Decisiones

Durante el proceso me encontré con varios errores que me ayudaron a entender mejor el funcionamiento interno. Aquí algunos ejemplos:

- ❌ Dirección mal cableada en el bus → solución: reorganizar pines.  
- 🔁 Instrucción que no hacía halt correctamente → revisión del microcódigo.  
- 💡 Decisión: cambiar el orden de ejecución de instrucciones para facilitar el debugging.

---

## 🧩 Capítulos Técnicos

### 1️⃣ EEPROM

Explicación de cómo programé la EEPROM, qué tabla de verdad usé, y cómo depuré errores en la escritura.

### 2️⃣ Microcode

Creación del microcódigo, estructura del ciclo de instrucción, uso de flags y fases del ciclo de fetch-decode-execute.

### 3️⃣ Instrucciones nuevas

Añadí instrucciones como `NOP`, `INC`, o `JNZ`. Aquí explico cómo las diseñé y qué efectos tienen.

*(Puedes añadir aquí capturas, gifs, esquemas, etc.)*

---

## 🎓 Qué aprendí

- Cómo se comunica un bus de datos.  
- El rol de los registros y la ALU.  
- Diseño de instrucciones y control mediante microcódigo.  
- Lo valioso del **debugging** como proceso de aprendizaje.

---

## ▶️ Cómo ejecutarlo / usarlo

(Si es físico, pon fotos o vídeos; si es en simulador como Logisim, puedes poner cómo abrirlo y correrlo)

---
"""

# Guardar archivo
readme_path = "/mnt/data/README.md"
with open(readme_path, "w", encoding="utf-8") as f:
    f.write(readme_content)

readme_path
