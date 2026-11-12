---
# the default layout is 'page'
icon: fas fa-info-circle
order: 4
---

### Architecture & Engineering Directives

> **"Data integrity is non-negotiable. Resilience is an architectural choice."**

안녕하세요, 백엔드 아키텍트 **Boris**입니다.

**The Arc Archive**는 엔터프라이즈 환경에서 마주하는 대용량 분산 시스템, 금융 및 원장(Ledger) 수준의 데이터 정합성 보장, 그리고 장애 복원력(Resilience)을 갖춘 아키텍처를 연구하고 기록하는 기술 아카이브입니다.

---

### Core Focus Areas

1. **무결성 및 멱등성 (Data Integrity & Idempotency)**
   - 금융/원장 시스템 수준의 트랜잭션 정합성 (Distributed Transactions, SAGA Pattern, 2PC)
   - 분산 환경에서의 멱등성 가드(Idempotency Key & Table Pattern) 및 중복 이벤트 격리

2. **경량 및 표준 우선 (Zero Overhead & Lean Tech)**
   - 불필요한 추상화와 오버엔지니어링을 배제한 클린 아키텍처 및 헥사고날 아키텍처
   - Java 21+ Virtual Threads, Record, Pattern Matching 등 런타임 표준 극대화
   - Spring Boot 및 폐쇄망 친화적 경량 스택

3. **고성능 데이터베이스 및 스토리지 엔지니어링**
   - 대용량 데이터베이스 커버링 인덱스, 복합 인덱스 순서 최적화
   - N+1 쿼리 엄격 차단 및 No-Offset 기반 대규모 페이징 아키텍처
   - Redis 인메모리 캐싱 및 분산 락(Redlock / Lua Script) 설계

---

### Contact & Profiles

- **GitHub**: [github.com/boris-arc-dev](https://github.com/boris-arc-dev)
- **Email**: [boris.arcdev@gmail.com](mailto:boris.arcdev@gmail.com)

