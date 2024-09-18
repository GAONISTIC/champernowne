# Abstract

챔퍼나운 상수는 1933년에 David G. Champernowne이 소개하면서 세상에 알려졌다. 그는 10진법에서 $0.123456789101112...$로 주어진 그 상수가 정규수라는 것을 증명했다. 4년 뒤, Jurt Mahler는 챔퍼나운 상수와 비슷한 구조를 가진 상수들의 초월성을 증명함으로써 챔퍼나운 상수 또한 초월수임을 증명했다. 이 두가지 특성(정규수, 초월수) 외에도, 챔퍼나운 상수는 특이한 연분수 전개를 가지고 있다. 즉, 전개에는 유난히 큰 항들이 포함되어 있다.

이 논문의 기여는 챔퍼나운 상수와 그 특성들, 증명들과 증명들에 사용된 기법들에 대한 더 나은 이해를 제공하는 것이다.

정규성에 대한 개념은 챔퍼나운이 했던 방법으로, 그리고 $(\epsilon, k)-normality$의 개념을 사용하여 설명되고 증명될 것이다. 그 후에, 우리는 초월성의 개념을 소개하고, Kurt Mahler의 논증을 따라 챔퍼나운 상수가 초월수임을 증명할 것이다. 마지막으로, 우리는 연분수 전개 절차를 고려하여 챔퍼나운 상수를 전개할 것이다. 연분수 전개에 대한 일반적인 개념 몇개가 소개될 것이다. 이 개념들로, 우리는 Kurt Mahler의 논증에 사용된 분수와 챔퍼나운 상수의 연분수에서 나타나는 큰 항들의 관계를 보일 것이다.

# Introduction
이 논문에서는 챔퍼나운 상수를 고려할 것이다. 챔퍼나운 상수는 경제학자 David G. Champernowne의 이름을 따 명명된 것으로, 그는 1933년에 발표한 그의 논문에서 이 상수의 10진법에서의 정규성을 증명했다. Champernowne은 1912년부터 2000년까지 살았으며, 그러므로 그는 학부생 시절에 그 논문을 발표한 것이다. 정규성의 개념이 상수에 대해 증명하기에 간단하지 않기 때문에, 그가 그 나이에 정규성을 증명했다는 것은 매우 주목할 만하다. 그의 수학적 지식은 아마도 매우 광범위하지 않았을 것이며, 실제로 이 증명은 매우 직관적이고 기본적인 수학적 추론을 사용한다. 

Champernowne이 10진법에서 정규성을 증명한 상수, 즉 우리가 집중할 상수는 다음과 같이 주어진다.
$$ C_{10} = 0.12345678910111213 \ldots $$
형식적으로, 이 상수는 자연수를 이어붙이는 것으로 정의된다. 아래첨자는 우리가 상수를 만드는 데 고려해야 할 자연수의 기수(진법)을 나타낸다. 만약 2진법이라면, 이렇게 정의될 것이다. 
$$ C_2 = 0.11011100101110111\ldots $$
이 상수는 십진법에서 ($C_{10}$) $0.86224$ 정도이다. 이 논문에서는 $C_{10}$만 고려할 것이다. (십진법만)

Champernowne의 논문은 수학자들에게 이 상수와 같은 구조를 가진 상수들을 추가로 연구하도록 영감을 주었다. 이러한 연구는 예를 들어, 정규성 증명에 조합론적인 방법으로 이어졌으며, 이는 $(\epsilon, k)-normality$ 개념을 사용하여 특정 특성을 가진 상수들의 정규성을 증명하는 방법이다. 또한 챔퍼나운 상수에 대한 다른 특성(정규성 외)들도 증명되었다. Kurt Mahler는 챔퍼나운 상수가 초월수임을 증명했고, 이 상수는 주목할 만한 큰 항을 포함하는 연분수 전개를 가지고 있음이 밝혀졌다.

# Normality
1933년에 발표된 Champernowne의 논문은 10진법에서 몇몇 상수의 정규성을 증명하는 데 집중하고 있다. 따라서, 우리는 정규성 특성부터 시작할 것이다. 우선 정규성의 직관적 정의부터 살펴보자.

상수가 10진법에서 정규적(normal)이라는 것은, $0, 1, ..., 9$로 구성된 모든 같은 길이의 문자열이 동일한 빈도로 나타난다는 것을 의미한다. 실제로, 무한소수인 상수가 10진법에서 정규적이라는 것은, 예를 들어 숫자 1과 숫자 2가 동일한 빈도로 나타나고, 문자열 025와 문자열 999가 동일한 빈도로 나타나는 경우를 말한다.

## Definition 2.1.
A constant $x$ is said to be normal in base $g$ if, for every string $s$ consisting of $k$ digits of base $g$, we have
상수 $x$가 $g$진법에서 정규적이라고 할 때, 기수 $g$의 $k$자리로 구성된 모든 문자열 $s$에 대해 다음이 성립한다.
$$ \lim_{N \to \infty} \frac{v(x, N, s)}{N} = \frac{1}{g^k} \tag{1}$$
where $v(x, N, s)$ denotes the number of times string $s$ occurs in the first $N$ digits of constant $x$ considered in base $g$. [2, p.1]
여기서 $v(x, N, s)$는 $g$진법에서 상수 $x$의 처음 $N$자리(소수 첫째 자리부터 $N$번째 자리까지)에서 문자열 $s$가 나타나는 횟수를 나타낸다.

따라서, $N$이 무한으로 갈 때, 한자리수 $s$는 10% 확률로 나타날 것이다. 어떤 한자리수를 선택하던간에, 모든 확률이 똑같을 것이다. 유사하게, 이는 모든 $k$(자리수)에 대해 성립한다. $k$자리수의 문자열을 만든다면 $10^k$개의 서로 다른 경우가 있을 것이다. 상수 $x$의 처음 $N$자리에서 각 문자열의 빈도를 $N$으로 나누면, $N$이 무한대로 갈때 모든 $k$자리 문자열이 나타나는 확률은 $1/10^k$에 가까워질 것이다.

이제 우리는 정규성을 정의했고, 이것이 어떻게 증명되는지 살펴보자. 우리가 챔퍼나운 상수를 10진법에서 집중적으로 다루기 때문에, 이러한 증명에서는 10진법을 사용할 것이다. 다음 증명을 위해 몇 가지 표기법을 설정하겠다.


$c_i$ A sequence of digits consisting of all $10^i$ possible strings of $i$ digtis, ordered in the following way: $0...00, 0...01, ..., 9...98, 9...99$. These specific strings are called members of $c_i$. (Note that commas are used to emphasize the different strings, this is used throughout the paper.)

$c_i$ 모든 $10^i$개의 가능한 i자리 문자열로 구성된 숫자 수열: $0...00, 0...01, ..., 9...98, 9...99$. 이러한 특정한 문자열들은 $c_i$의 멤버라고 부른다. (Note. 문서 전체에서 문자열을 구분하기 위해 콤마를 사용함.)


$C^j$ A chain of sequences $c_i$ where every sequence $c_i$ is repeated $j$ times in the following way: $C^j = c_1...c_1c_2...c_2c_3...$ For example $C^1 = c1c2c3... = 0,1,...,9,00,01,...,99,000,001,...$

$C^j$ 각 시퀸스 $c_i$가 다음과 같은 방식으로 j번 반복되는 수열의 연쇄: $C^j = c_1...c_1c2...c2c3...$ 얘를 들어, $C^1 = c1c2c3... = 0,1,...,9,00,01,...,99,000,001,...$


$C$ An ordered sequence of the natural numbers. This sequence is given by: $C = 1,2,...,9,10,11,...,99,100,101,...$

$C$ 자연수의 정렬된 수열. 이 수열은 다음과 같이 주어진다: $C = 1,2,...,9,10,11,...,99,100,101,...$


$L(·)$ The function that denotes the length of a string, that is, the number of digits that make up the string.

$L(·)$ 문자열의 길이를 알려주는 함수. 문자열을 구성하는 자리수를 알려줌.


$O(·)$ Known as *the big-$O$ notation*. When a function $f(n)$ has that $f(n) \in O(g(n))$, it means that for some constant K we have $|f(n) / g(n) | \leq K$ for every $n$.

$O(·)$ *big-$O$ notation*(*big-$O$* 표기법). 함수 $f(n)$이 $f(n) \in O(g(n))$일 때, 이는 어떤 상수 $K$에 대하여 모든 $n$에 대해 $|f(n)/g(n)| \leq K$가 성립함을 의미한다.

$o(·)$ Known as the *little-O notation*. When a function $f(n)$ has that $f(n) \in o(g(n))$, it means that $f(n)/g(n) \rightarrow 0$ as $n \rightarrow \infty$. If we have a term $x + f(n)$ in this case, it also can be denoted as $x + o(g(n))$. The same holds for the *big-$O$ notation*.  

$o(·)$ *little-$O$ notation*(*little-$O$* 표기법). 함수 $f(n)$이 $f(n) \in o(g(n))$일 때, 이는 $f(n)/g(n)$이 $n$이 무한대로 갈 때 0으로 수렴함을 의미한다. 이 경우, 항 $x + f(n)$도 $x + o(g(n))$으로 표기할 수 있다. 동일하게 *big-$O$ notation*도 적용된다.

## Normality proof by Champernowne
Champernowne의 논문에서 했던 것처럼, 다음 세 가지 정리를 먼저 명시한다. 첫 번째와 두 번째 정리는 결국 챔퍼나운 상수가 실제로 정규수임을 증명하는데 필요하다.

### Theorem 2.1. *The decimal number $0.C^1$ is normal*

### Theorem 2.2. *The decimal number $0.C^j$ is normal, $\forall j \in \mathbb{N}$*

### Theorem 2.3. *The constant of Champernowne, given by $0.C$, is normal.*

이제 이 정리를 공식화했으므로, 첫 번째 정리인 정리 2.1.을 증명하자.
### Theorem 2.1.1 Normality proof of $0.C^1$
우리는 다음의 단계를 거쳐 상수 $0.C^1$가 정규수임을 증명할 것이다.

1. 먼저 수열 $c_i$의 임의의 문자 $s$의 개수를 센다.
2. 이전 결과를 이용해, 체인 $C^1_r$에서 나타나는 임의의 문자 $s$의 개수를 센다.
3. 다음으로 수열 $c_i$에서 $c_i$의 $N$번째 자리를 포함하는 멤버를 찾아야 한다.
4. 그 후, 수열 $c_i$의 멤버에서 문자열 $s$의 위치를 결정한다.
5. 각 멤버에서 문자열 $s$ 앞뒤에 올 수 있는 자리의 가능성을 결정한다.
6. 4단계와 5단계를 이용해, 수열 $c_i$에서 문자열 $s$의 분리되지 않은 발생 횟수를 찾는다.
7. 나뉘어진 발생 횟수와 함께, 우리는 수열 $c_i$에서 $s$의 발생 횟수를 $N$에 대해 찾는다.
8. 마지막으로, 수열 $C^1$에서 문자열 $s$의 발생 횟수를 $N$에 대해 결정한다.

**The number of arbitrary strings $s$ in the sequence $c_i$**
수열 $c_i$의 임의의 문자열 $s$의 개수

증명을 시작하기 위해, 수열 $c_i$에 집중하여 수열 $c_i$에 길이 $k$인 임의의 문자열 $s$이 얼마나 많이 나타나는지 찾자. 전에 말했던 것처럼, 수열의 모든 멤버 사이에 콤마를 넣어 수열을 보기 좋게 한다는 것을 잊지 말자. 예를 들어, 
$$ c_2 = 00,01,02,\ldots,98,99 \tag{2}$$
$s$의 두 자리 사이에 콤마가 있다면 문자열 $s$는 *divided*라고 한다. 이 경우가 아니라면, 우리는 $s$를 *undivided*라 한다. $c_2$의 $s=25$인 경우를 예로 들어 보자. $25$는 $\ldots,24,25,26,\ldots$에서 *undivided*로 나타나고,  $\ldots,52,53,\ldots$.에서 *divided*로 나타난다.

문자열 $s$가 $k > i$인 경우에서 *undivided*가 될 수 없음을 기억하자. $k \leq i$인 경우에서, $c_i$에 $s$가 *undivided*로 얼마나 많이 나타나는지 세는 것은 쉽다. 예를 들어, 문자열 $s = 25$는 수열 $c_4$에서 300번 *undivided*로 나타난다. 이 문자열은 세 가지 방법으로 나타날 수 있는데, 즉 $c_4$ 멤버의 왼쪽, 가운데 또는 오른쪽으로 나타날 수 있다($25\cdot\cdot, \cdot25\cdot, 25\cdot\cdot$). 멤버의 다른 자리가 어떤 자리수간 될 수 있기에, 모든 경우는 $c_4$에서 $10^2$번 나타난다(빈자리 두개 채우는 경우의 수 $10 \times 10 = 10^2$) ($2525$같이 이 자리수들이 다시 같은 문자열을 만들어내도 그렇다. 이건 두번 세어지지만($25\cdot\cdot$과 $\cdot\cdot25$에서 두번 세어짐), 문자열 $s = 25$를 두개 가지고 있어 괜찮다). 그러므로 일반적으로, 길이가 2인 모든 문자열 $s$는 $c_4$에서 $3 \cdot 10^2 = 300$번 $c_4$에서 세어진다.

같은 논증은 모든 수열 $c_i$에서 모든 길이의 문자열 $s$에 대해서도 사용될 수 있다. $c_i$에서 길이 $k$인 모든 문자열 $s$는 *undivided*로 $i - k + 1$개의 다른 위치로 나타나며, 각각의 위치에서, 문자열 $s$는 $10^{i - k}$번 나타난다. 그러므로, 모든 $i$에 대하여 $c_i$에서 어떤 길이 $k$를 가지는 모든 문자열 $s$는 $(i - k + 1)10^{i - k}$번 나타난다.

$c_i$의 *divided* 문자열 $s$의 발생에서, 문자열 $s$를 나누기 위한 콤마의 자리가 $k - 1$개 있고, $c_i$에는 콤마는 $10^i - 1$개 있으므로, 문자열 $s$는 최대 $(k - 1)(10^i - 1)$번 *divided*로 나타날 수 있다. 
($s = 0123456789$에 대해 $c_1 = 0,1,2,3,4,5,6,7,8,9$를 본다면, $s$는 $(10 - 1)(10^1 - 1) = 9$번 *divided*로 나타났다.)

수열 $c_i$의 길이가 $L(c_i) = i10^i$으로 써질 수 있음을 기억하자. 길이가 $k$인 모든 문자열 $s$의 *divided* 발생의 상한을 $c_i$의 길이로 나누면 다음과 같다.
$$ \frac{(k - 1)10^i}{i10^i} = \frac{k - 1}{i} \rightarrow 0, \text{as } i \rightarrow \infty \Rightarrow$$
$$ (k - 1)10^i \in o(L(c_i)), \tag{3}$$
전에 소개했던 *little-$o$* 표기법을 이용했다. 이제, 만약 $c_i$에 $s$의 *undivided* 발생 수까지 $L(c_i)$ 항에 대해 고려한다면, 다음과 같은 식을 얻는다.
$$(i - k + 1)10^{i - k} = i10^{i - k} - (k - 1)10^{i - k}$$
$$= 10^{-k}L(c_i) + o(L(c_i)) \tag{4}$$
// $i10^{i - k} = 10^{-k} \times i10^i = 10^{-k} \times L(c_i)$

만약 $(k - 1)10^i \in o(L(c_i))$이라면, $-(k - 1)10^i \in o(L(c_i))$도 성립하며, 이는 마지막 식을 정당화한다. 방정식 $(3)$과 $(4)$의 결과를 결합하면, $c_i$에서 문자열 $s$의 총 발생 횟수를 다음과 같이 나타낼 수 있다.

$$ v(c_i, s) = 10^{-k}L(c_i) + o(L(c_i)). \tag{5} $$
// $v(c_i, s)$는 $c_i$에서 $s$의 개수를 나타낸다.

$c_i$에 $s$의 *divided* 발생의 개수를 나타내기 위해 **Definition 2.1**와 같은 함수 $v$를 사용했다는 것을 기억하자. 또한 $o(L(c_i))$의 원소의 유한한 합은 다시 $o(L(c_i))$에 포함되고, 정의의 극한은 여전히 0임을 기억하자.