# Research Radar — 최근 논문 표시 버전

기존 데이터베이스·AI 연구 레이더에 주제별 최근 논문 목록을 추가한 버전입니다.

## 기존 사이트 업그레이드

GitHub 저장소에서 아래 두 파일만 새 파일로 교체하고 commit합니다.

```text
index.html
data/research_topics.json
```

GitHub Pages가 `main / (root)`에서 배포 중이라면 commit 후 자동으로 사이트가 갱신됩니다.

## 추가된 기능

- 주제 카드에서 최근 관련 논문 수와 최신 학회 표시
- 자세히 보기에서 논문 제목, 학회, 공개 시점, 요약 표시
- 각 논문이 해당 연구 주제와 왜 관련 있는지 별도 설명
- 논문 제목·학회·요약도 홈페이지 검색 대상에 포함
- 현재 13개 주제에 최근 논문 38편 연결

## 매월 업데이트 요청 문구

ChatGPT의 월간 연구 레이더가 도착하면 다음처럼 요청합니다.

```text
이번 달 Research Radar를 기존 홈페이지 형식의 research_topics.json으로 만들어줘.
각 주제마다 최근 관련 논문 2~4편을 포함하고,
논문 제목·학회/연도·한국어 요약·왜 관련 있는지·원문 URL을 넣어줘.
```

받은 파일을 다음 위치에 덮어쓰고 commit합니다.

```text
data/research_topics.json
```

## 논문 데이터 형식

각 주제의 `papers` 배열은 다음 구조입니다.

```json
{
  "title": "논문 제목",
  "venue": "SIGMOD 2026",
  "date": "2026-06",
  "type": "Research Paper",
  "summary": "한국어 핵심 요약",
  "relevance": "이 연구 주제에서 읽을 가치가 있는 이유",
  "url": "https://..."
}
```
