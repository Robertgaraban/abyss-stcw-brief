# Prompt — Calidad / SGC a Datos y Analítica

```md
Actúa como data architect y systems engineer para ABYSS.

Quiero diseñar cómo toda la documentación, trazabilidad y eventos de `Calidad / SGC` en ABYSS pasan a una capa de datos estructurada para ser analizados.

Contexto:
- ABYSS ya tiene módulo de `SGC / ISO`, procedimientos, auditorías, objetivos, riesgos, competencias, expedientes, checklist DGMM, encuestas, documentación firmada y reportes.
- Necesitamos convertir esa capa documental en una capa de datos útil para control, reporting y mejora continua.

Desarrolla:

1. Qué fuentes deben entrar en la capa analítica:
- procedimientos
- auditorías
- no conformidades
- acciones correctivas
- riesgos
- objetivos
- competencias
- expedientes
- documentación firmada
- encuestas de satisfacción
- trazabilidad académica relacionada

2. Modelo de datos analítico:
- tablas base
- hechos
- dimensiones
- claves
- versionado
- timestamps
- trazabilidad por tenant / curso / alumno / instructor / auditoría

3. Pipeline propuesto:
- ingestión
- normalización
- validación
- almacenamiento
- reporting
- alertas

4. Casos de análisis:
- preparación de auditoría
- cobertura documental
- riesgos abiertos
- cumplimiento por curso
- satisfacción por instructor / curso
- tiempos de cierre
- calidad operativa por sede / periodo

5. Controles:
- privacidad
- anonimización o seudonimización
- acceso por rol
- calidad del dato
- reconciliación con runtime transaccional

6. Documentación:
- diagrama de flujo de datos
- diccionario de datos
- indicadores prioritarios
- qué mostrar públicamente
- qué mantener privado

Formato:
- Objetivo
- Fuentes
- Modelo analítico
- Pipeline
- Casos de uso
- Controles
- Plan documental
- Prioridad recomendada
```
