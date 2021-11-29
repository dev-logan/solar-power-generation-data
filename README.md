## Dataset
This data has been gathered at two solar power plants in India over a 34 day period. It has two pairs of files - each pair has one power generation dataset and one sensor readings dataset. The power generation datasets are gathered at the inverter level - each inverter has multiple lines of solar panels attached to it. The sensor data is gathered at a plant level - single array of sensors optimally placed at the plant.

## Summary of Findings
* 매일 각 인버터의 총 발전량의 변화를 그래프로 그려서 어떤 인버터 그룹에 문제가 생겼는지 확인할 수 있었다.
* 하지만 2 발전소의 경우 각 인버터의 발전량이 제각각이기 때문에 그래프 상에서 어떤 인버터 그룹에 문제가 생겼는지 특정 짓기 힘들었다.
* 따라서 매일 각 인버터의 발전량과 최대 발전량을 내는 인버터를 비교하고 비율을 계산하여, 임의의 기준에 따라 어떤 인버터 그룹에 문제가 생겼는지 규정할 수 있었다.
* 발전량을 예측하기 위해서 10일과 5일 동안의 발전량으로 부터 다음 날의 발전량을 예측하는 모델을 만들었으나 한계가 있었다.
* 따라서 날씨 데이터를 이용하여 발전량 예측을 진행했다.
* 'AMBIENT_TEMPERATURE', 'IRRADIATION’로 부터 multi linear regression 모델을 통해 ‘AC_POWER’ 즉 발전량을 예측할 수 있었다.
