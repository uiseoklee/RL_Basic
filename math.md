# 용어 정리

### **알고리즘: Q-learning**

초기화:

Q(s, a|W) ← 미분 가능한 함수

W ← 함수의 가중치를 임의의 값으로 초기화

각 에피소드에 대해 반복:

s를 초기화

에피소드의 각 스텝에 대해 반복:

s에서 행동 정책을 이용해 행동 a를 선택(예: Gibbs 소프트맥스 함수)

행동 a를 취한 후 보상 r과 다음 상태 s’를 관측

s’에서 타깃 정책으로 행동 a’를 선택

$$
w \gets w + \alpha[r + \gamma \max_{a'}Q(s', a'|w) - Q(s,a|w)]{ \partial Q(s,a|w)\over \partial w}
$$

s가 마지막 상태라면 종료