# 2023 01 02

### transformer time complexity

![image](https://user-images.githubusercontent.com/100833732/210191134-74a77ffe-d67e-42ef-b665-33bc0c581beb.png)

input의 차원 수의 제곱에 비례하는 rnn, cnn과 달리 attention 알고리즘은 input sequence 의 length의 제곱에 비례하는 구조를 갖는다.
이는 attention matrix를 만들 때 query와 key가 행렬곱 연산이 되기 때문이다. 

    transformer는 입력 길이 N에 대하여 O(N^2)의 복잡도를 가져 일정 길이 이상을 연산하기 힘들다.
    
BERT는 이로 인해 512라는 길이의 제한이 있기도 하며 이로 인해 sentence embmedding을 사용하기도 한다.
긴 입력을 받기 위해 Linformer, Longformer, reFormer, Big Bird 등의 모델이 나오고 있다. 

### Linear Transformer

softmax 함수가 어텐션의 필수 메커니즘이 아님을 아이디어로 각 시점의 토큰과 다른 토큰들과 유사도를 비교하고 유사도에 맞춰 가중합을 계산한다.
즉 다른 토큰과 비교하여 임의의 토큰이 얼마나 유사한지 측정한다.


출처 스탠포드 세미나 자료 : <https://nlp.stanford.edu/seminar/details/lkaiser.pdf>

