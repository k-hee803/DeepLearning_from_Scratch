# 1장. 헬로 파이썬

### 1.5 Numpy

1. 가져오기
    
     `import numpy as np`
    
2. 배열 생성
    
    `x = np.array([1.0, 2.0, 3.0])`
    
3. N차원 배열
    
    `A = np.array([1, 2], [3, 4])` 
    
4. 브로드캐스트(broadcast)
    - 형상이  다른  배열끼리도 계산이 가능하다
5. 원소 접근
    
    ```python
    X = np.array([[51, 55], [14, 19], [0, 4]])
    print(X[0]) # array([51, 55])
    print(X[0][1]) # 55
    
    X = X.flatten() # X를 1차원 배열로 변환(평탄화)
    print(X) # [51 55 14 19 0 4]
    print(X[np.array([0, 2, 4])]) # array([51, 14, 0])
    
    print(X > 15) # array([True True False True False False], dtype=bool)
    print(X[X>15]) # array([51, 55, 19]
    ```
    

### 1.6 Matplotlib

1. `import matplotlib.pyplot as plt`
2. 데이터 준비
    
    `x = np.arange(0, 6, 0.1)` `y = np.sin(x)`
    
3. 그래프 그리기
    
    `plt.plot(x,y)` `plt.show()`
    
4. 그래프 옵션(그래프 이름, 선스타일, 축 이름, 제목,  범례)
    
    `label='이름'` `linestyle="--"` `plt.xlabel(”x”)` `plt.title('제목')` `plt.legend()`
    
5. 이미지 표시
    
    ```python
    import matplotlib.pyplot as plt
    from matplotlib.image import imread
    
    img = imread('이미지 경로')
    
    plt.imshow(img)
    plt.show()
    ```
