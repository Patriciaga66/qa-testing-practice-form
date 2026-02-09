# 📋 Análisis de DEMOQA

## Información General
- **URL:** (https://demoqa.com automation-practice-form)
- **Tipo de aplicación:** Formulario
- **Fecha de análisis:** 09/02/2026
- **Analista:** Patricia Gonzalez

## Objetivo de la Aplicación
Recolecta en un aformulario informacion de el usuario como: nombre completo, datos de comunicacion y preferencias.

## Elementos Identificados

### 1. Campos de Entrada
| Campo | Tipo | Validación Observada | ¿Obligatorio? |
|-------|------|---------------------|---------------|
|First Name | Text Input | Alfanumerico| si
|Last Name |Text Input |Alfanunerico |si |
|Email | Email Input|Formato Validacion Email| si|
|Mobile |Number Input|10 Digitos Numericos| si|

### 2. Elementos de Selección
| Elemento | Tipo | Opciones Disponibles | Obligatorio|
|----------|------|---------------------|--------------|
|Gender|Radio|Male, Female, Other| si|
|Hobbies |Checkbox | Sports, Reading, Music|no|
|Date of Birth|Date| Calendario|no|
|Subjects| Multiseleccion autocomplete| Lista de materias|no|

### 3. Campos de Texto Opcionales 
| Campo | Tipo | Validación | Obligatorio |
|-------|------|------------|-------------|
|Current Address|text input |ninguna |no|



### 4. Campos Dependientes
| Campo | Tipo | Dependencia | Obligatorio |
|-------|------|-------------|-------------|
|State|Dropdown|independiente|no|
|City|Dropdown|depende de la seleccion de State|no|



### 5. Otros Elementos
- **Picture: Upload de imagen (opcional)
- **Submit: Botón de envío del formulario

## Flujo de Usuario Observado

1. [Paso 1: Usuario hace X]
2. [Paso 2: Sistema responde con Y]
3. [Paso 3: ...]
4. [...]

## Validaciones Identificadas

### ✅ Validaciones que funcionan:
- [Validación 1 que observaste]
- [Validación 2]
- [...]

### ⚠️ Posibles bugs o áreas de mejora:
- [Algo que no funciona bien o podría mejorar]
- [...]

## Casos de Prueba Sugeridos

Basado en este análisis, se deberían crear casos para:
- [ ] [Tipo de prueba 1 - ej: Campos obligatorios]
- [ ] [Tipo de prueba 2 - ej: Validación de formato]
- [ ] [Tipo de prueba 3 - ej: Flujo completo exitoso]
- [ ] [...]

## Observaciones Adicionales
[Cualquier cosa importante que notaste sobre la aplicación]

## Conclusiones
[Tu opinión sobre qué tan bien está construida la aplicación y qué necesita testing]