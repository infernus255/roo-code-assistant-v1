# ROO-CODE-SWARM Template (Enterprise AI Agent Framework)

Este repositorio es un template arquitectónico para orquestar un enjambre de agentes de IA secuenciales (Sequential Multi-Agent Pipeline) bajo la estricta metodología de **Spec-Driven Development (SDD)** y **Harness Engineering**.

## 🧠 Filosofía Arquitectónica
Este framework parte de la premisa de que los LLMs son motores estocásticos (probabilísticos). Para generar software determinista, de calidad empresarial y libre de alucinaciones en hardware local/cloud, el enjambre se rige por:
1. **Cero Código sin Contrato:** Ningún agente programa (M5) sin un documento de negocio (BSP) y de arquitectura técnica (TDP) validados.
2. **Separation of Concerns (SoC) Agéntico:** Roles divididos (PM, BA, Arquitecto, QA, Developer, DevOps) que no se solapan.
3. **El Orquestador como Gatekeeper:** Un único punto de control que valida los *inputs/outputs* de cada fase antes de mover el grafo.

## 📁 Estructura del Framework
El sistema mantiene una separación inmutable entre el "motor" y el "resultado":
- `.swarm/`: Cerebro inmutable. Contiene especificaciones (`specs/`), contratos (`CONTRACTS.md`) y el motor de validación.
- `app_result/`: Espacio de trabajo dinámico. Aquí se generan el código, la arquitectura, los planes de prueba y la memoria del proyecto.

## 🚀 Workflows Soportados
- **Greenfield (Desde Cero):** Ideación -> Manifiesto -> Especificaciones -> Código -> Infraestructura.
- **Brownfield (Legacy):** Ingeniería Inversa desde repositorios existentes -> Documentación Automática -> Refactorización.