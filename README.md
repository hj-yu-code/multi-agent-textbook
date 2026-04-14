# Multi-Agent Orchestration: Theory and Practice

**멀티에이전트 오케스트레이션: 이론과 실전**

> AI 코딩 에이전트의 멀티에이전트 오케스트레이션에 관한 포괄적인 한국어 교재

**저자:** 유혜정

---

## Overview

이 교재는 단일 LLM 에이전트의 한계를 넘어, 여러 에이전트가 협업하여 복잡한 소프트웨어 엔지니어링 작업을 수행하는 시스템의 **설계, 구현, 운영**을 다룹니다.

- **35+ 멀티에이전트 패턴**을 6개 범주로 체계적으로 분류
- **6개 실전 도구** (OMC, ECC, Superpowers, gstack, GSD, Gas Town)를 깊이 있게 분석
- **모든 단원에 실행 가능한 Python 코드** 예시 포함
- **29개 SVG 다이어그램**으로 시각적 이해 지원
- **25개 학술/산업 출처** (날짜 포함)로 학술적 엄밀성 확보

---

## Table of Contents

| # | 단원 | 내용 |
|---|------|------|
| 00 | [목차](00_목차.md) | 교재 소개, 대상 독자, 학습 경로 |
| 01 | [서론](01_서론.md) | 멀티에이전트 시스템의 동기, 배경, Anthropic 연구 결과 |
| 02 | [기본 패턴](02_기본_패턴.md) | Augmented LLM, Prompt Chaining, Routing, Parallelization, Orchestrator-Workers, Evaluator-Optimizer |
| 03 | [오케스트레이션 패턴](03_오케스트레이션_패턴.md) | Blackboard, Multi-Agent Debate, Reflexion, Planner-Executor, Handoff, Magentic-One |
| 04 | [작업 분해 패턴](04_작업_분해_패턴.md) | THREAD, Scatter-Gather, Market-Based Allocation, Fan-In 병목 해소 |
| 05 | [모델 라우팅 패턴](05_모델_라우팅_패턴.md) | FrugalGPT, Semantic/Cost-Aware/Shadow Routing, 프로덕션 5레이어 |
| 06 | [품질 보증 패턴](06_품질_보증_패턴.md) | Evaluator-Optimizer, LLM-as-Judge, MoA, Six Sigma Agent |
| 07 | [오류 처리 및 안전](07_오류_처리_및_안전.md) | Circuit Breaker, Guardian Agent, Pub-Sub, A2A, Shadow/Canary 배포 |
| 08 | [실전 도구 분석](08_실전_도구_분석.md) | OMC, ECC, Superpowers, gstack, GSD, Gas Town 비교 분석 |
| 09 | [에이전트 구현 가이드](09_에이전트_구현_가이드.md) | Agent/Skill/Hook 정의, 모델 티어 배정, CLAUDE.md 설계, 실전 구현 예시 |
| 10 | [프로덕션 배포](10_프로덕션_배포.md) | C 컴파일러 사례, 토큰 예산, 벤치마크, 모니터링, 인간-에이전트 협업 |
| 11 | [부록](11_부록.md) | 용어 사전, 출처 목록, 다이어그램 목록, 도구 설치 빠른 참조 |

---

## Key Numbers

| 항목 | 수치 |
|------|------|
| 총 분량 | **6,389줄** (12개 단원) |
| 패턴 수 | **35+** (6개 범주) |
| SVG 다이어그램 | **29개** |
| 실전 도구 분석 | **6개** |
| 학술/산업 출처 | **25개** |
| 코드 예시 | **50+** (Python, JavaScript, YAML, JSON, Bash) |

---

## Diagrams

29개의 SVG 다이어그램이 `diagrams/` 폴더에 포함되어 있습니다.

### Pattern Diagrams (15)

| 다이어그램 | 유형 | 단원 |
|-----------|------|------|
| 단일 에이전트 vs 멀티에이전트 비교 | Component | 01 |
| 워크플로우-에이전트 연속체 | Component | 01 |
| 기본 패턴 선택 의사결정 트리 | Activity | 02 |
| 오케스트레이션 패턴 비교 | Component | 03 |
| 계획-실행 분리 전체 흐름 | Activity | 03 |
| 핸드오프 vs 오케스트레이터-워커 비교 | Component | 03 |
| 작업 분해 패턴 비교 | Component | 04 |
| Fan-In 병목 해소 패턴 | Component | 04 |
| 모델 라우팅 패턴 비교 | Component | 05 |
| FrugalGPT 캐스케이딩 흐름 | Activity | 05 |
| 프로덕션 라우팅 5레이어 스택 | Component | 05 |
| 품질 보증 패턴 비교 | Component | 06 |
| Six Sigma 합의 투표 프로세스 | Activity | 06 |
| 서킷 브레이커 상태 전이 | Statechart | 07 |
| 레인보우 배포 시간축 | Activity | 07 |

### Tool Architecture Diagrams (8)

| 다이어그램 | 유형 | 단원 |
|-----------|------|------|
| OMC Team 모드 5단계 파이프라인 | Activity | 08 |
| OMC 3티어 모델 라우팅 | Component | 08 |
| ECC 개발 워크플로우 | Activity | 08 |
| AgentShield 적대적 파이프라인 | Component | 08 |
| Superpowers 워크플로우 | Activity | 08 |
| gstack 6가지 역할 시스템 | Component | 08 |
| GSD 스펙 기반 개발 파이프라인 | Activity | 08 |
| Gas Town Mayor 패턴 아키텍처 | Component | 08 |

### Implementation Diagrams (6)

| 다이어그램 | 유형 | 단원 |
|-----------|------|------|
| 통신/안전/배포 패턴 | Component | 07 |
| 오류 처리 패턴 | Component | 07 |
| 3단계 스킬 로딩 프로세스 | Activity | 09 |
| Opus 코디네이터 종합 아키텍처 | Component | 09 |
| 병렬 에이전트 Docker 동기화 아키텍처 | Component | 10 |
| 인간-에이전트 협업 검증 프로세스 | Activity | 10 |

---

## Learning Paths

### 초급 (멀티에이전트 입문)

```
01 서론 → 02 기본 패턴 → 08 실전 도구 분석
```

### 중급 (패턴 심화)

```
01 → 02 → 03 오케스트레이션 → 04 작업 분해 → 05 모델 라우팅 → 06 품질 보증 → 07 오류 처리 → 08 실전 도구
```

### 고급 (구현 및 운영)

```
전 단원 순서대로 (01~11)
```

---

## References

이 교재는 다음 25개 출처를 기반으로 합니다:

### Anthropic 공식 자료

- [How We Built Our Multi-Agent Research System](https://www.anthropic.com/engineering/multi-agent-research-system) (2025)
- [Building Effective Agents](https://www.anthropic.com/research/building-effective-agents) (2024)
- [Building a C Compiler with Parallel Claudes](https://www.anthropic.com/engineering/building-c-compiler) (2026)

### 학술 논문 (11편)

arxiv 2510.01285 (Blackboard), 2305.14325 (Debate), 2512.20845 (MAR), 2503.09572 (Plan-and-Act), 2405.17402 (THREAD), 2601.22290 (Six Sigma), 2603.04445 (Routing Survey), 2505.24239 (Credibility), 2505.19234 (GUARDIAN), 2411.13768 (EDDOps), 2511.07784 (Debate Diversity)

### 산업 자료 (11편)

Azure AI Agent Patterns, Addy Osmani (Code Agent Orchestra), Maxim (Routing), Mixture-of-Agents, 30 Tips for Agent Teams, FrugalGPT (Portkey), Google A2A, Event-Driven AI Agents, Shadow Testing, AWS Scatter-Gather

---

## Quality Assurance

이 교재는 **Opus-Sonnet 교차 검토 3회전** 프로세스를 거쳤습니다:

| 단계 | 점수 | 줄 수 |
|------|------|-------|
| Opus 초안 | — | 3,325 |
| 1차 검토 (Opus) → 수정 (Sonnet) | 7.5 → 8.5 | 4,527 |
| 2차 검토 (Opus) → 수정 (Sonnet) | 8.5 → 9.2 | 5,552 |
| 3차 검토 (Opus) → 수정 (Sonnet) | 9.2 → **9.3** | 6,389 |
| 최종 검토 (Opus) | **9.3/10** | 6,389 |

**최종 판정: 출판 가능**

---

## License

This work is for educational purposes.

---

## Structure

```
multi_agent/
├── README.md                           ← 이 파일
├── 00_목차.md                          ← 교재 목차 및 학습 로드맵
├── 01_서론.md                          ← 멀티에이전트 시스템이란
├── 02_기본_패턴.md                     ← 에이전틱 빌딩 블록
├── 03_오케스트레이션_패턴.md           ← 에이전트 간 협업 구조
├── 04_작업_분해_패턴.md               ← 복잡한 작업 분할
├── 05_모델_라우팅_패턴.md             ← 비용과 품질의 균형
├── 06_품질_보증_패턴.md               ← 에이전트 출력 품질 관리
├── 07_오류_처리_및_안전.md            ← 신뢰성과 보안
├── 08_실전_도구_분석.md               ← 주요 Claude Code 도구 비교
├── 09_에이전트_구현_가이드.md         ← 에이전트를 직접 만들기
├── 10_프로덕션_배포.md                ← 실전 운영
├── 11_부록.md                          ← 용어 사전, 출처, 다이어그램 목록
└── diagrams/                           ← 29개 SVG 다이어그램
    ├── ch01_single_vs_multi_agent.svg
    ├── ch01_agent_vs_workflow_continuum.svg
    ├── ch02_pattern_decision_tree.svg
    ├── ch03_orchestration_patterns.svg
    ├── ch03_planner_executor_flow.svg
    ├── ch03_handoff_vs_orchestrator.svg
    ├── ch04_task_decomposition_patterns.svg
    ├── ch04_fan_in_patterns.svg
    ├── ch05_model_routing_patterns.svg
    ├── ch05_frugalgpt_cascading.svg
    ├── ch05_production_routing_layers.svg
    ├── ch06_quality_assurance_patterns.svg
    ├── ch06_six_sigma_consensus.svg
    ├── ch07_communication_safety_deployment.svg
    ├── ch07_error_handling_patterns.svg
    ├── ch07_circuit_breaker_statechart.svg
    ├── ch07_rainbow_deployment.svg
    ├── ch08_omc_team_pipeline.svg
    ├── ch08_omc_model_routing.svg
    ├── ch08_ecc_dev_workflow.svg
    ├── ch08_ecc_agentshield.svg
    ├── ch08_superpowers_workflow.svg
    ├── ch08_gstack_roles.svg
    ├── ch08_gsd_pipeline.svg
    ├── ch08_gastown_mayor.svg
    ├── ch09_skill_loading_process.svg
    ├── ch09_opus_coordinator_pattern.svg
    ├── ch10_parallel_agent_sync.svg
    └── ch10_human_agent_verification.svg
```
