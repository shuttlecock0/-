# 지도학습 VS 비지도학습



## 지도학습

-  **정답이 주어진 상태에서 학습하는 알고리즘**

  -  많은 고양이와 기린의 사진을 주고 각 사진이 고양이인지 기린인지 하나하나 정답을 알려준 후 어떤 사진을 주었을 때 고양이인지 기린인지 알아맞힐 수 있도록 하는 것 

-  **지도학습의 목적은 분류(classification)와 회귀생성(regression)** 

  - 분류: 어떤 데이터를 적절한 유한개의 클래스로 분류 
  - 회귀생성: 데이터의 특징을 기반으로 연속적인 값을 예측하는 것 

  <img src = "https://post-phinf.pstatic.net/MjAxODA4MDJfMjc1/MDAxNTMzMTg1NTQwMDcw.rDJmkQSchSqyhifIOpV5EJg5DeDx71XYgWXW07JUE3Ig.vDvL6PDJixUx5livk3llUwKeBUgSrT3l1TgCNRCuXxIg.JPEG/2%EC%A7%80%EB%8F%84%ED%95%99%EC%8A%B5.jpg?type=w1200">

## 비지도학습

- **정답이 주어져 있지 않은 데이터의 특성을 학습하여 스스로 패턴을 파악 **

  -  대표적인 비지도학습: 군집화(clustering) 
    -  하나하나 정답을 주지 않더라도 데이터의 특성을 파악하여 비슷한 사진끼리 분류하는 것을 군집화 
  -   **비지도학습 GAN**
    - 원 데이터가 가지고 있는 확률분포를 추정하도록 하고, 인공신경망이 그 분포를 만들어 낼 수 있도록 한다는 점에서 단순한 군집화 기반의 비지도학습과 차이가 있음

  <img src = "https://post-phinf.pstatic.net/MjAxODA4MDJfODUg/MDAxNTMzMTg1NTYyNDQ4.MICqwzMvZwjUoWy1F7nI6hzmYmQ52cHE9cdsdTYfDsog.5jJNBCxVGCuhMPlig_woMyWd0M7Ac91IrVc5rRGUR1Eg.JPEG/3%EB%B9%84%EC%A7%80%EB%8F%84%ED%95%99%EC%8A%B5.jpg?type=w1200">

