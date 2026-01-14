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

## Pill Guy Metrics
### Definitions
- 인증 성공률: 매칭 성공/전체 요청 비율
- 로그 누락률: 누락 로그/전체 투약 기록 비율

### Baseline vs After
- Baseline: 재전송/캐싱 적용 전
- After: 재전송/캐싱 적용 후

### Results Table
| Metric | Baseline | After | Delta |
| --- | --- | --- | --- |
| Auth success rate | TBD | TBD | TBD |
| Log missing rate | TBD | TBD | TBD |

### Evidence
- 통신 로그 캡처: (링크/파일명)

## Fitness AI Trainer Metrics
### Definitions
- 오검출률: 기준 포즈 대비 오분류 비율
- 지연: 프레임 입력~피드백 출력 평균

### Baseline vs After
- Baseline: 최적화 전
- After: 프레임 스킵/경량화 적용 후

### Results Table
| Metric | Baseline | After | Delta |
| --- | --- | --- | --- |
| Mis-detection rate | TBD | TBD | TBD |
| Feedback latency | TBD | TBD | TBD |

### Evidence
- 로그 캡처/그래프: (링크/파일명)
