# ₿ 프로젝트 소개
LSTM 신경망을 이용한 비트코인 시세 예측

# 💹 실제가격과 예측가격
![image](https://github.com/Brazen-Story/big-data-final-prj/assets/88796297/c14a14e4-311d-4eb1-9f1b-d5f7f3f0280e)

# 💸 오늘의 종가
비트코인 시세에 대한 오늘의 종가를 구할 수 있는 코드입니다.
```
# 최신 'window_len' 일의 데이터 추출 및 모델 입력 데이터 준비
latest_data = hist[-window_len:]
latest_data_normalized = normalise_zero_base(latest_data) if zero_base else latest_data
latest_data_reshaped = latest_data_normalized.values.reshape((1, window_len, len(hist.columns)))

# LSTM 모델을 사용하여 예측 실행
predicted_change = model.predict(latest_data_reshaped)
predicted_price = (predicted_change + 1) * latest_data['close'].iloc[-1]
```
