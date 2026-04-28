# 발표 초안

## 1. 문제 정의

제약조건이 있는 long-only 포트폴리오에서 Sharpe ratio가 가장 높은 가중치 조합은 무엇인가?

## 2. 데이터와 가정

- 합성 샘플 데이터: `data/sample/asset_return_panel.csv`
- 재현 가능한 baseline 실행을 우선 구성

## 3. 방법

표본 수익률에서 평균-분산 기준의 단순 최적 가중치를 찾는다.

## 4. 현재 산출물

- 실행 스크립트: `python -m src.run_baseline`
- 결과 표: `outputs/tables/baseline_results.csv`

## 5. 후속 작업

- 실제 데이터 연결
- 민감도 분석
- 차트/보고서 산출
- 프로젝트별 상세 검증
