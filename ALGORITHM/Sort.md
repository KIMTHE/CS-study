# 정렬종류

### [stable sort](https://goodgid.github.io/Stable-Sort/)

### [bubble sort](https://gmlwjd9405.github.io/2018/05/06/algorithm-bubble-sort.html)

### [insertion sort](https://gmlwjd9405.github.io/2018/05/06/algorithm-insertion-sort.html)

- [shell sort](https://gmlwjd9405.github.io/2018/05/08/algorithm-shell-sort.html)

### [selection sort](https://gmlwjd9405.github.io/2018/05/06/algorithm-selection-sort.html)

### [merge sort](https://gmlwjd9405.github.io/2018/05/08/algorithm-merge-sort.html)

### [quick sort(손코딩)](https://gmlwjd9405.github.io/2018/05/10/algorithm-quick-sort.html)

- [improved quick sort](https://gusdnd852.tistory.com/124)

### [heap sort](https://gmlwjd9405.github.io/2018/05/10/algorithm-heap-sort.html)

### [counting sort](https://gyoogle.dev/blog/algorithm/Counting%20Sort.html)

### [radix sort](https://gyoogle.dev/blog/algorithm/Radix%20Sort.html)

## [자바/코틀린에서 sort 구현](https://ongveloper.tistory.com/385)

<img src="https://gmlwjd9405.github.io/images/algorithm-bubble-sort/sort-time-complexity.png" width="80%">

    - Quick Sort와 Merge Sort를 비교해 주세요.

    : stable 여부, 시간복잡도, 공간복잡도

    - Quick Sort에서 O(N^2)이 걸리는 예시를 들고, 이를 개선할 수 있는 방법에 대해 설명해 주세요.

    : 이미 정렬된 경우에 pivot 값이 최소나 최대로 지정되어 파티션이 나누어지지 않았을 때, 위의 링크 참고.

    - Stable Sort가 무엇이고, 어떤 정렬 알고리즘이 Stable 한지 설명해 주세요.

    : 위의 링크 참고.

    - Merge Sort를 재귀를 사용하지 않고 구현할 수 있을까요?

    : 처음부터 길이가 1인 배열들로 시작하여, 병합만 차례로 해나간다.

    - Radix Sort에 대해 설명해 주세요.

    : 위의 링크 참고.
 
    - Bubble, Selection, Insertion Sort의 속도를 비교해 주세요.

    : 위의 표 참고.

    - 값이 거의 정렬되어 있거나, 아예 정렬되어 있다면, 위 세 알고리즘의 성능 비교 결과는 달라질까요?

    : 삽입정렬만 best case.

    - 본인이 사용하고 있는 언어에선, 어떤 정렬 알고리즘을 사용하여 정렬 함수를 제공하고 있을까요?

    : 자바/코틀린은 위의 링크 참고. 파이썬은 tim sort

    - 정렬해야 하는 데이터는 50G 인데, 메모리가 4G라면, 어떤 방식으로 정렬을 진행할 수 있을까요?

    : 이 상황에서는 비교 횟수 보다 swap 등 데이터의 이동 회수가 훨씬 중요하게 여겨져 복사나 값 교환 작업이 알고리즘의 성능을 좌우하게 됩니다.

    1. (관계형 데이터베이스에서와 같은) 복합 레코드들을 key 값으로 정렬하듯이, 리스트 자체를 정렬하지 말고 인덱스를 만들어 그 인덱스로 정렬을 하는 방법이 있다. 인덱스는 전체 리스트보다 훨씬 작으므로 전체 물리 메모리에 못 들어갈 데이터들을 RAM 영역에서 정렬할 수 있으며 효과적으로 디스크 스와핑을 없앨 수 있다. 이 과정은 종종 "tag sort"라 불리기도 한다.

    2. 전체적인 성능 향상을 위해 두 알고리즘의 강점을 조합하는 것이다. 예를 들어 배열은 RAM 영역에 쉽게 포함될 수 있는 크기 단위로 나뉘어 질 수 있을 것이고 나뉘어진 분할 리스트들을 각기 퀵 소트나 힙 소트로 정렬한다. 그리고 정렬된 분할 리스트들을 머지 소트로 병합하는 것이다. 이렇게 하면 머지 소트만 하는 것보다 성능이 뛰어나며 퀵 소트만 하는 것 보다 작은 물리 메모리를 필요로 하게 된다.








