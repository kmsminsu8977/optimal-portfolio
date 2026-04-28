# Optimal Portfolio

최적 포트폴리오 프로젝트의 기본 연구 구조와 재현 가능한 baseline 산출물을 담은 저장소입니다.

**핵심 연구 질문**

> 제약조건이 있는 long-only 포트폴리오에서 Sharpe ratio가 가장 높은 가중치 조합은 무엇인가?

## 저장소 구조

```text
optimal-portfolio/
├── src/                         # baseline 계산 로직과 실행 엔트리포인트
├── data/sample/                 # 합성 샘플 입력 데이터
├── docs/                        # 방법론과 해석 기준
├── notebooks/                   # 실행 흐름을 보여주는 최소 노트북
├── outputs/tables/              # 재현 가능한 결과 CSV
├── presentation/                # 발표/보고서 초안
└── references/                  # 재작성 개념 노트와 참고문헌 메모
```

## 빠른 시작

```bash
python -m src.run_baseline
```

실행 결과는 `outputs/tables/baseline_results.csv`에 저장됩니다.

## 구현 범위

- 월별 합성 수익률에서 기대수익률과 공분산을 추정한다.
- 10% 단위 grid search로 long-only, full-investment 제약을 만족하는 가중치를 찾는다.
- 최적화 절차를 설명하는 기준 구현이다.

## 주요 파일

- `src/optimal_portfolio_baseline.py`: 표본 수익률에서 평균-분산 기준의 단순 최적 가중치를 찾는다.
- `data/sample/asset_return_panel.csv`: baseline 실행용 합성 입력값
- `docs/methodology.md`: 계산 절차, 입력/출력 정의, 해석상 주의점
- `outputs/tables/baseline_results.csv`: 현재 baseline 산출물

## 다음 확장 방향

- 실제 공개 데이터 또는 별도 수집 데이터 연결
- notebook 기반 탐색 분석 추가
- 차트와 표를 포함한 최종 보고서 작성
- 모델 검증, 민감도 분석, 비용/리스크 가정 보강
