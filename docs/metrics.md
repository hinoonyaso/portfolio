# Metrics & Logs

## Shoepernoma Metrics
### Definitions
- 정의: Path tracking oscillation(흔들림) = cross-track error(RMS)
- 정의: Replan time = compute_path_to_pose 요청~응답 평균(rosout timestamp)
- 수집: rosout + bag replay
- 집계: 10회 평균/표준편차

### Baseline vs Tuned
- Baseline: `config/teb/teb_profile_default.yaml` @ commit <hash>
- Tuned: `config/teb/teb_profile_narrow.yaml` @ commit <hash>

### Results Table
| Metric | Baseline | Tuned | Delta |
| --- | --- | --- | --- |
| Path tracking oscillation (RMS) | TBD | TBD | TBD |
| Replan time (avg) | TBD | TBD | TBD |
| Stop accuracy (cm) | TBD | TBD | TBD |

### Top5 Tuning Params (TEB)
| Param | Change | Effect |
| --- | --- | --- |
| max_vel_x | TBD | 속도 상한 안정화 |
| acc_lim_x | TBD | 가속 제어 안정화 |
| weight_optimaltime | TBD | 시간 최적화 가중 |
| min_obstacle_dist | TBD | 안전 거리 확보 |
| weight_obstacle | TBD | 장애물 회피 강화 |

### Evidence
- rosout 캡처: (링크/파일명)
- bag 파일/재생 방법: (링크/파일명)
- 파라미터 diff: (링크/파일명)
- TF 트리 이미지: (링크/파일명)
- 핵심 프레임 표: map/odom/base_link/laser/imu

### Reproduce
1. ros2 launch roscar_nav bringup.launch.py
2. rosbag play <bag_path> --clock
3. python tools/eval_cte.py --bag <bag_path>
4. python tools/eval_replan.py --log <rosout_log>
5. outputs/*.csv → plots/*.png

### TF Frame Table
| Frame | Parent | Source | Note |
| --- | --- | --- | --- |
| map | — | SLAM | global |
| odom | map | nav2 | local drift |
| base_link | odom | wheel/imu | robot body |
| laser | base_link | static tf | LiDAR |
| camera_link | base_link | static tf | RGB-D |

## COOLRO Metrics
### Definitions
- 정의: UART 오류율 = 오류 패킷/전체 패킷 비율
- 정의: 거리 편차 = 목표거리 대비 오차 평균/표준편차
- 수집: UART 로그 + 거리 추정 로그
- 집계: 8회 평균/표준편차

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
- UART 프로토콜 스펙:\n  - baud: 115200 / frame: STX | cmd | payload | CRC16 | ETX\n  - timeout: 30ms / retry: 3 / ack: OK/ERR\n  - error handling: CRC fail → resend, timeout → safe stop

## Pill Guy Metrics
### Definitions
- 정의: 인증 성공률 = 매칭 성공/전체 요청 비율
- 정의: 로그 누락률 = 누락 로그/전체 투약 기록 비율
- 수집: 인증 로그 + 투약 로그
- 집계: 사용자 5명 × 30회 평균

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
- 정의: 오검출률 = 기준 포즈 대비 오분류 비율
- 정의: 지연 = 프레임 입력~피드백 출력 평균
- 수집: UI 로그 + 프레임 타임스탬프
- 집계: 5회 평균

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
- 프로파일링 요약: (링크/파일명)
