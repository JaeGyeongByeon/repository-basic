# 5주차/개념

## State Variables

---
![Untitled](https://github.com/JaeGyeongByeon/repository-basic/assets/144103220/9996bccc-689c-4268-a208-68722672322b)



1. 복잡한 문제는 여러명이서 분업을 통해 문제를 해결하는 경우가 종종 있음
2. 이 때 문제를 여러개로 쪼개어 체계를 갖추고 싶을 때
3. 의미있는 시스템에 정의를 하고 이 중심으로 문제를 푸는것이 핵심

## State Variables의 예제1.

---
![Untitled 1](https://github.com/JaeGyeongByeon/repository-basic/assets/144103220/19443e10-15f4-4e0c-bead-af02a9a04d61)





1. 스프링이 있는 mass damper system은 미분이 2번 들어가는 2차 방정식꼴로 나타난다. 
2. 라플라스 트랜스폼의 해가 2개가 나오는데 이는 State가 2개인 것을 의미한다.(x1,x2)
3. x2를 설정할 때는 x1의 미분값으로 x2를 설정한다. 

![Untitled 2](https://github.com/JaeGyeongByeon/repository-basic/assets/144103220/f3340a20-f6ef-4e5e-9647-7b2138ae4831)


1. 정리전의 라플라스트랜스폼은 2차이지만, 2개의 연립방정식으로 나눠서 생각할 수 있게 된다.
2. 이는 행렬을 이용하여 1차미분방정식과 같은 형식으로 해를 구할 수 있다.

## State Variables의 예제2.

---
![Untitled 3](https://github.com/JaeGyeongByeon/repository-basic/assets/144103220/6c7cf68d-ba41-4215-8c75-1b89ce4b8f58)


1. x1과 x2를 전압과 전류로 정한 이유 그냥. 단지 두 식이 항등식이 되는 것만 피하면 뭐든 좋다.
2. 이를 KCL과 KVL을 이용해서 회로를 해석하면 커페시터가 포함된 항, 인덕터와 커페시터가 포함된 항으로 구분할 수 있다.
![Untitled 4](https://github.com/JaeGyeongByeon/repository-basic/assets/144103220/8ca9039e-f25c-4fc6-80fb-66ae60305f08)


1. 이렇게 식을 세우면 1차 미분방정식이 2개가 나오는 형태를 만들어낼 수 있다.

![Untitled 5](https://github.com/JaeGyeongByeon/repository-basic/assets/144103220/9acfb844-cbbb-4fb1-abc1-dbe6a5df8478)

## State Space Equation

---

![Untitled 6](https://github.com/JaeGyeongByeon/repository-basic/assets/144103220/a4afabe3-1490-4616-ae70-25544f86dd4e)

1. 식을 정리하면, 적분 밖의 값과 적분 안의 값으로 구분 할 수 있다. 
2. 왼쪽값은 시작 전 초기값이다.

![Untitled 7](https://github.com/JaeGyeongByeon/repository-basic/assets/144103220/55324a90-46fb-4f14-901a-a3dfc4685785)

1. 일반적으로 다차 미분방정식으로 수식이 정리가된다.
2. 즉, 스테이트는 벡터의 형식으로 정리가 된다.

![Untitled 8](https://github.com/JaeGyeongByeon/repository-basic/assets/144103220/7dcce038-5075-4314-b1c7-ddae9b20a84f)

1. 행렬로 수식을 바꾸면, 1차 미분방정식이 2개였던 것을 하나의 행렬 1차 미분 방정식으로 바꿀 수 있다.
2. 이렇게 행렬의 형식으로 바꾸면 좋은 점은 
a. 스테이트에 의미가 부여가 되기 때문에 수식에서 그 의미를 파악하기 쉬워진다.
b. 컴퓨터에게 일을 시킬 때 좀 더 편하게 시킬 수 있다.
c. 즉 분업을 할 때 세분화하여 일을 시킬 수 있다.

![Untitled 9](https://github.com/JaeGyeongByeon/repository-basic/assets/144103220/ad11c6d3-df26-4295-a265-0cb37806f081)

1. 행렬로 표현하였기 때문에 행렬식 연산이 가능하다. 
2. 트랜스폼을 해주는 함수 파이(t)를 state transition matrix라고 한다.

## State Space Equation

---
![Untitled 10](https://github.com/JaeGyeongByeon/repository-basic/assets/144103220/e8100ebd-2f79-4709-9d8c-97141cb354d6)


1. 이 문제의 경우 4차 미분 방정식을 세워야한다. 
2. 그러면 이를 해석하기 매우 힘들다. 그러므로 1차 행렬 미분 방정식으로 만들어서 쉽게 문제를 해결 할 수 있도록 한다.

![Untitled 11](https://github.com/JaeGyeongByeon/repository-basic/assets/144103220/3c85157a-116d-4095-9726-094fd9e292a9)

1. 이는 1차 행렬 미분 방정식으로 만들 수 있다. 
![Untitled 12](https://github.com/JaeGyeongByeon/repository-basic/assets/144103220/80bb9b03-1844-42f8-8c7a-534d93b67b4f)


1. 이를 matlab으로 해석할 수 있다.
