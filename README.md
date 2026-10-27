# 03-orchestration

[LLM Zoomcamp 2026 — Module 3: AI Orchestration with Kestra](https://github.com/DataTalksClub/llm-zoomcamp/tree/main/03-orchestration) 실습 저장소입니다. 공식 예제를 바탕으로 현재 사용 가능한 모델 설정을 적용했습니다.

- `docker-compose.yml`: Kestra와 PostgreSQL 실행 설정
- `flows/`: RAG, agent, multi-agent 예제 6개
- `.env.example`: 필요한 환경변수 이름과 형식

`.env.example`을 참고해 로컬 `.env`에 암호와 API 키를 설정한 뒤 실행합니다. `GEMINI_API_KEY`는 일반 키이고, flow용 `SECRET_*` 값은 각 API 키를 Base64로 인코딩한 값입니다. `.env`는 Git에서 제외됩니다.

```bash
docker compose up -d
```

현재 생성 모델은 `gemini-3.5-flash-lite`, 3번 flow는 `gpt-6-luna`, 임베딩 모델은 `gemini-embedding-001`을 사용합니다. Flow 등록과 실습 순서는 위 공식 자료를 참고하세요.
