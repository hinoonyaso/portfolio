# Metrics & Logs

## Shoepernoma Metrics
### Definitions
- Path tracking oscillation(흔들림): cross-track error(RMS) 기준
- Replan time: compute_path_to_pose 요청~응답 평균 지연(rosout timestamp)

### Baseline vs Tuned
- Baseline: Nav2 기본 파라미터
- Tuned: teb_tuning_profile 적용 후

### Results Table
| Metric | Baseline | Tuned | Delta |
| --- | --- | --- | --- |
| Path tracking oscillation (RMS) | TBD | TBD | TBD |
| Replan time (avg) | TBD | TBD | TBD |
| Stop accuracy (cm) | TBD | TBD | TBD |

### Evidence
- rosout 캡처: (링크/파일명)
- bag 파일/재생 방법: (링크/파일명)
- 파라미터 diff: (링크/파일명)

## COOLRO Metrics
### Definitions
- UART 오류율: 오류 패킷/전체 패킷 비율
- 거리 편차: 목표거리 대비 오차의 평균/표준편차

### Baseline vs After
- Baseline: 필터링/CRC 적용 전
- After: 필터링/CRC 적용 후

### Results Table
| Metric | Baseline | After | Delta |
| --- | --- | --- | --- |
| UART error rate | TBD | TBD | TBD |
| Follow distance error (avg/std) | TBD | TBD | TBD |

### Evidence
- UART 로그 캡처: (링크/파일명)
