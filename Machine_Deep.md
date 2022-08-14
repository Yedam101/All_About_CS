  # 머신러닝과 딥러닝의 주요 개념들 정리
  <br/>
  <br/>
  
  ## 머신러닝 

  주어진 데이터에서 x와 y의 관계를 w와 b를 이용하여 식을 세우는 일을 가설이라고 한다. 문제에 대한 규칙을 가장 잘 표현하는 w와 b를 찾는 것이 중요하다. 머신 러닝은 w와 b를 찾기 위해서 실제값과 가설로부터 얻은 예측값의 오차를 계산하는 식을 세우고, 이 식의 값을 최소화하는 최적의 w와 b를 찾아낸다.
  <br/>
  <br/>

  ### - 비용 함수(Cost function)
   <br/>
  실제값과 예측값에 대한 오차에 대한 식을 목적 함수(Objective function) 또는 비용 함수(Cost function) 또는 손실 함수(Loss function) 라고 한다. 함수의 값을 최소화하거나, 최대화하거나 하는 목적을 가진 함수를 목적 함수(Objective function), 값을 최소화하려고 하면 이를 비용 함수(Cost function) 또는 손실 함수(Loss function)라고 한다.
  <br/>
  <br/>

  ### - 옵티마이저(Optimizer)
 <br/>
  선형 회귀를 포함한 수많은 머신 러닝, 딥 러닝의 학습은 결국 비용 함수를 최소화하는 매개 변수인 w와 b을 찾기 위한 작업을 수행한다. 이때 사용되는 알고리즘을 옵티마이저(Optimizer) 또는 최적화 알고리즘이라고 부른다.

  그리고 이 옵티마이저를 통해 적절한 w와 b를 찾아내는 과정을 머신 러닝에서 훈련(training) 또는 학습(learning)이라고 부른다. 
  <br/>
  <br/>

  ### -  ex) 선형 회귀
  - 선형회귀의 비용 함수(Cost function) : 평균 제곱 오차(MSE)
  - 선형회귀의 옵티마이저(Optimizer) : 경사하강법(Gradient Descent)
  <br/>
  <br/>

  ### -  기계학습 전 데이터의 분리 

  머신 러닝을 위한 데이터를 준비했다면 기계를 학습하기 전 해당 데이터를 훈련용(Training), 검증용(Validation), 테스트용(Testing) 이렇게 세 가지로 분리하는 것이 일반적이다.  
  - 훈련 데이터는 머신 러닝 모델을 학습하는 용도이다. 테스트 데이터는 학습한 머신 러닝 모델의 성능을 평가하기 위한 용도이다.  
  - 검증용 데이터는 모델의 성능을 평가하기 위한 용도가 아니라 모델의 성능을 조정하기 위한 용도이다. 더 정확히는 모델이 훈련 데이터에 과적합(overfitting)이 되고 있는지 판단하거나 하이퍼파라미터의 조정을 위한 용도이다.    
  - 훈련용 데이터로 훈련을 모두 시킨 모델은 검증용 데이터를 사용하여 정확도를 검증하며 하이퍼파라미터를 튜닝(tuning) 한다. 검증용 데이터에 대해서 높은 정확도를 얻도록 하이퍼파라미터의 값을 바꿔보는 것이다.
  <br/>
  <br/>

  ### -  하이퍼파라미터와 파라미터(매개변수)
   <br/>
  - 하이퍼파라미터(초매개변수) : 모델의 성능에 영향을 주는 사람이 값을 지정하는 변수. 경사 하강법에서의 학습률(learning rate)이나, 딥 러닝에서 뉴런의 수나 층의 수와 같은 것들이 대표적인 하이퍼파라미터이다.  

  - 매개변수 : 가중치와 편향. 학습을 하는 동안 값이 계속해서 변하는 수. 가중치와 편향과 같은 매개변수는 사용자가 결정해주는 값이 아니라 모델이 학습하는 과정에서 얻어지는 값이다.
  <br/>
  <br/>

  ### -  분류(Classification)와 회귀(Regression)
   <br/>

  1) 이진 분류 문제(Binary Classification)
  이진 분류는 주어진 입력에 대해서 두 개의 선택지 중 하나의 답을 선택해야 하는 것. 종합 시험 성적표를 보고 최종적으로 합격, 불합격인지 판단하는 문제, 메일을 보고나서 정상 메일, 스팸 메일인지를 판단하는 문제 등이 이에 속한다.

  2) 다중 클래스 분류(Multi-class Classification)
  다중 클래스 분류는 주어진 입력에 대해서 세 개 이상의 선택지 중에서 답을 선택해야 하는 것. 예를 들어 서점 직원이 일을 하는데 과학, 영어, IT, 학습지, 만화라는 레이블이 붙어있는 5개의 책장이 있다고 하고 새 책이 입고되면, 이 책은 다섯 개의 책장 중에서 분야에 맞는 적절한 책장에 책을 넣어야 한다. 이 경우는 현실에서의 다중 클래스 분류 문제라고 할 수 있다.

  3) 회귀 문제(Regression)
  회귀 문제는 분류 문제처럼 둘 중 하나를 선택해야 한다거나, 책이 입고되었을 때 5개의 책장 중 하나의 책장을 골라야하는 경우처럼 정답이 몇 개의 정해진 선택지 중에서 정해져 있는 경우가 아니라 어떠한 연속적인 값의 범위 내에서 예측값이 나오는 경우를 말한다.  
  예를 들어서= 역과의 거리, 인구 밀도, 방의 개수 등을 입력하면 부동산 가격을 예측하는 머신 러닝 모델이 있다고 하면 머신 러닝 모델이 부동산 가격을 7억 8,456만 3,450원으로 예측하는 경우도 있을 것이고, 8억 1257만 300원으로 예측하는 경우도 있을 수 있다. 즉, 특정 값의 범위 내에서는 어떤 숫자도 나올 수 있다. 기존의 분류 문제와 같이 분리된(비연속적인) 답이 결과가 아니라 연속된 값을 결과로 가지는 이러한 문제를 회귀 문제라고 부른다. 회귀 문제의 예시로 시계열 데이터(Time Series Data)를 이용한 주가 예측, 생산량 예측, 지수 예측 등이 있다.
  <br/>
  <br/>

  ### -  원-핫 인코딩(One-Hot Encoding)  
 <br/>
  컴퓨터는 문자보다는 숫자를 더 잘 처리한다. 이를 위해 자연어 처리에서는 문자를 숫자로 바꾸는 여러가지 기법들이 있다. 원-핫 인코딩은 그 기법들 중에서 단어를 표현하는 가장 기본적인 표현 방법이다.   
  원-핫 인코딩은 단어 집합의 크기를 벡터의 차원으로 하고, 표현하고 싶은 단어의 인덱스에 1의 값을 부여하고, 다른 인덱스에는 0을 부여하는 단어의 벡터 표현 방식이다. 이렇게 표현된 벡터를 원-핫 벡터(One-Hot vector)라고 한다.
  <br/>
  <br/>

  ### -  소프트맥스 회귀(Softmax Regression)
 <br/>
  이진 분류가 두 개의 선택지 중 하나를 고르는 문제라면, 다중 클래스 분류는 세 개 이상의 선택지 중 하나를 고르는 문제이다. 로지스틱 회귀를 통해 2개의 선택지 중에서 1개를 고르는 이진 분류(Binary Classification)문제를 푼다면 3개 이상의 선택지 중에서 1개를 고르는 다중 클래스 분류 문제는 소프트맥스 회귀를 통해 풀 수 있다.    

 <br/>
  소프트맥스 함수는 선택해야 하는 선택지의 총 개수를 k라고 할 때, k차원의 벡터를 입력받아 각 클래스에 대한 확률을 추정한다.   
  다수의 클래스를 분류하는 문제에서는 이진 분류처럼 2개의 숫자 레이블이 아니라 클래스의 개수만큼 숫자 레이블이 필요하다. 이때 생각해볼 수 있는 레이블링 방법은 분류해야 할 클래스 전체에 정수 인코딩을 하는 것이다. 예를 들어서 분류해야 할 레이블이 {red, green, blue}와 같이 3개라면 각각 0, 1, 2로 레이블한다. 또는 분류해야 할 클래스가 4개고 인덱스를 숫자 1부터 시작하고 싶다면 {baby, child, adolescent, adult}라면 1, 2, 3, 4로 레이블을 해볼 수 있다. 
  
  <br/>
  그런데 일반적인 다중 클래스 분류 문제에서 레이블링 방법으로는 위와 같은 정수 인코딩이 아니라 원-핫 인코딩을 사용하는 것이 보다 클래스의 성질을 잘 표현하였다고 할 수 있다. 그 이유는 정수 인코딩과 달리 원-핫 인코딩은 분류 문제 모든 클래스 간의 관계를 균등하게 분배하기 때문이다. 물론 각 클래스가 순서의 의미를 갖고 있어 회귀를 통해 분류 문제를 풀 수 있는 경우는 정수 인코딩의 순서 정보가 도움이 된다.
  <br/>
  <br/>
   <br/>

  ### -  혼동 행렬(Confusion Matrix)
   <br/>

  머신 러닝에서는 맞춘 문제수를 전체 문제수로 나눈 값을 정확도(Accuracy)라고 한다. 하지만 정확도는 맞춘 결과와 틀린 결과에 대한 세부적인 내용을 알려주지는 않는다. 이를 위해서 사용하는 것이 혼동 행렬(Confusion Matrix)이다. 
   <br/>
  | -   | 예측 참   | 예측 거짓 |
  |:--------|:--------:|--------:|
  | 실제 참   | TP | FN       |
  | 실제 거짓     | FP   | TN      |
   <br/>
  * True Positive(TP) : 실제 True인 정답을 True라고 예측 (정답)
  * False Positive(FP) : 실제 False인 정답을 True라고 예측 (오답)
  * False Negative(FN) : 실제 True인 정답을 False라고 예측 (오답)
  * True Negative(TN) : 실제 False인 정답을 False라고 예측 (정답)
  <br/>
  <br/>

  ### -  훈련 데이터의 오차와 테스트 데이터의 오차는 손실이라고도 부른다.
  <br/>
  <br/>

  ### -  과적합 방지를 고려한 일반적인 딥 러닝 모델의 학습 과정

  1. 주어진 데이터를 훈련 데이터, 검증 데이터, 테스트 데이터로 나눈다. 가령, 6:2:2 비율로 나눌 수 있다.
  2. 훈련 데이터로 모델을 학습한다. (에포크 +1)
  3. 검증 데이터로 모델을 평가하여 검증 데이터에 대한 정확도와 오차(loss)를 계산한다.
  4. 검증 데이터의 오차가 증가하였다면 과적합 징후이므로 학습 종료 후 Step 5로 이동, 아니라면 Step 2.로 재이동한다.
  5. 모델의 학습이 종료되었으니 테스트 데이터로 모델을 평가한다.
  <br/>
  <br/>
    

  ### -  훈련(training) 또는 학습(learning)
   <br/>
  머신 러닝은 데이터가 주어지면, 기계가 스스로 데이터로부터 규칙성을 찾는 것에 집중한다. 이렇게 주어진 데이터로부터 규칙성을 찾는 과정을 훈련(training) 또는 학습(learning)이라고 한다.
  <br/>
  <br/>
  
  ### -  훈련(training) 또는 학습(learning)
   <br/>
  머신 러닝은 데이터가 주어지면, 기계가 스스로 데이터로부터 규칙성을 찾는 것에 집중한다. 이렇게 주어진 데이터로부터 규칙성을 찾는 과정을 훈련(training) 또는 학습(learning)이라고 한다.
  <br/>
  <br/>
  
  ### -  훈련(training) 또는 학습(learning)
   <br/>
  머신 러닝은 데이터가 주어지면, 기계가 스스로 데이터로부터 규칙성을 찾는 것에 집중한다. 이렇게 주어진 데이터로부터 규칙성을 찾는 과정을 훈련(training) 또는 학습(learning)이라고 한다.
  <br/>
  <br/>
  
  ### -  훈련(training) 또는 학습(learning)
   <br/>
  머신 러닝은 데이터가 주어지면, 기계가 스스로 데이터로부터 규칙성을 찾는 것에 집중한다. 이렇게 주어진 데이터로부터 규칙성을 찾는 과정을 훈련(training) 또는 학습(learning)이라고 한다.
  <br/>
  <br/>

  
  ### -  훈련(training) 또는 학습(learning)
   <br/>
  머신 러닝은 데이터가 주어지면, 기계가 스스로 데이터로부터 규칙성을 찾는 것에 집중한다. 이렇게 주어진 데이터로부터 규칙성을 찾는 과정을 훈련(training) 또는 학습(learning)이라고 한다.
  <br/>
  <br/>