# Metrics & Logs

## Shoepernoma Metrics
- Path tracking oscillation(흔들림): cross-track error(RMS) 기준
- Replan time: compute_path_to_pose 요청~응답 평균 지연(rosout timestamp)
- Baseline: Nav2 기본 파라미터 / After: teb_tuning_profile 적용 후
- rosout 로그 및 bag replay 기반 수치 요약을 텍스트로 정리

## COOLRO Metrics
- UART 오류율/추종 지연 로그 요약을 텍스트로 정리
