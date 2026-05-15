# SWARN — FastAPI + PydanticAI

Pipeline multi-agente secuencial (M0–M6) con orquestación tipada, contratos validables y soporte multi-modelo.

## Stack

- FastAPI — API REST + WebSocket
- PydanticAI — Agentes con outputs estructurados y tools tipadas
- Typer — CLI
- JSON — Persistencia de estado (compatible con .swarm_template/)

## Arquitectura

M0 (Bootstrapper) → M1 (TDP) → M2 (BSP) → M3 (Arch) → M4 (QA) → M5 (Code) → M6 (DevOps)

## Endpoints API

| Metodo | Ruta | Descripcion |
|--------|------|-------------|
| POST | /swarm/init | Inicializa proyecto |
| GET | /swarm/state | Estado actual |
| POST | /swarm/transition | Transiciona al siguiente agente |
| POST | /swarm/agents/{id}/run | Ejecuta un agente |
| POST | /swarm/validate | Aprueba/rechaza paso (HITL) |
| GET | /swarm/history | Historial de transiciones |
| GET | /swarm/artifacts | Artefactos generados |
| WS | /swarm/ws | Tiempo real |
