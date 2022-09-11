

<h1 align = center>Math - New Comers</h1>

 # Constnants

$$\Huge \pi \quad$$ `#define PI acos(-1)` used mostly in **Geomtry**</br>
$$\Huge \epsilon \quad$$`#define EPS 1e-9`  used in comparing **Doubles**</br>
$$\large MOD \quad$$ `#define Mod 1'000'000'007` used as common **Modulus** for big numbers </br>


---
# Functions
## Rounding 
1.  **Floor** $$\large floor(x)=\lfloor x \rfloor$$
**floor()** function **returns the largest integer less than or equal to a given number**.


<div align = center>
<table>
<thead>
<tr>
<th style="text-align:center">1</th>
<th style="text-align:center">1</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:center">0</td>
<td style="text-align:center">0</td>
</tr>
<tr>
<td style="text-align:center">1.1</td>
<td style="text-align:center">1</td>
</tr>
<tr>
<td style="text-align:center">1.7</td>
<td style="text-align:center">1</td>
</tr>
<tr>
<td style="text-align:center">-1.7</td>
<td style="text-align:center">-2</td>
</tr>
<tr>
<td style="text-align:center">-1.1</td>
<td style="text-align:center">-2</td>
</tr>
</tbody>
</table>
</div>


```cpp
#include <cmath>
floor(1.1); // 1
flooe(1.7); // 1
```


2. **ceil** $$\large ceil(x)=\lceil x \rceil$$
**ceil()** function **computes the smallest integer that is greater than or equal to x.**
<div align = center>
<table>
<thead>
<tr>
<th style="text-align:center">1</th>
<th style="text-align:center">1</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:center">0</td>
<td style="text-align:center">0</td>
</tr>
<tr>
<td style="text-align:center">1.1</td>
<td style="text-align:center">2</td>
</tr>
<tr>
<td style="text-align:center">1.7</td>
<td style="text-align:center">2</td>
</tr>
<tr>
<td style="text-align:center">-1.7</td>
<td style="text-align:center">-1</td>
</tr>
<tr>
<td style="text-align:center">-1.1</td>
<td style="text-align:center">-1</td>
</tr>
</tbody>
</table>
</div>


```cpp
#include <cmath>
ceil(1.1); // 2
ceil(1.7); // 2
```
 
3. **Round** $$\large round(x)=\lfloor x \rceil$$
**round()** function **returns the integral value that is nearest to the argument, with halfway cases rounded away from zero**.


<div align = center>
<table>
<thead>
<tr>
<th style="text-align:center">1</th>
<th style="text-align:center">1</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:center">0</td>
<td style="text-align:center">0</td>
</tr>
<tr>
<td style="text-align:center">1.1</td>
<td style="text-align:center">1</td>
</tr>
<tr>
<td style="text-align:center">1.7</td>
<td style="text-align:center">2</td>
</tr>
<tr>
<td style="text-align:center">-1.7</td>
<td style="text-align:center">-2</td>
</tr>
<tr>
<td style="text-align:center">-1.1</td>
<td style="text-align:center">-1</td>
</tr>
</tbody>
</table>
</div>



```cpp
#include <cmath>
round(1.1); // 1
round(1.7); // 2
```
4. **Truncate** <br> **trunc()** function **removes the decimal part from a number.**
<div align = center>
<table>
<thead>
<tr>
<th style="text-align:center">1</th>
<th style="text-align:center">1</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:center">0</td>
<td style="text-align:center">0</td>
</tr>
<tr>
<td style="text-align:center">1.1</td>
<td style="text-align:center">1</td>
</tr>
<tr>
<td style="text-align:center">1.7</td>
<td style="text-align:center">1</td>
</tr>
<tr>
<td style="text-align:center">-1.7</td>
<td style="text-align:center">-1</td>
</tr>
<tr>
<td style="text-align:center">-1.1</td>
<td style="text-align:center">-1</td>
</tr>
</tbody>
</table>
</div>


```cpp
#include <cmath>
trunc(1.1); // 1
trunc(1.7); // 2
```


### resources
#### articles
[Floor](https://www.programiz.com/cpp-programming/library-function/cmath/floor)
[Ceil](https://www.programiz.com/cpp-programming/library-function/cmath/ceil)
[round](https://www.programiz.com/cpp-programming/library-function/cmath/round)
[trunc](https://www.programiz.com/cpp-programming/library-function/cmath/trunc)
#### Videos
[YT -   Portfolio Courses](https://www.youtube.com/watch?v=FixR9aiVsy4)
[YT - Mostafa saad](https://youtu.be/Syx2qDjj7TE?list=PLPt2dINI2MIY7l5zyFd1W28rei3b-AXaJ&t=702)

---

## Factorization
a **factors** of on a number are the digits that this number is divisble by
we can get all factor of a number in order if O( $\sqrt{n}$ )
```cpp 
vector < ll > Get_Divisors(ll n){
	vector < ll > divisors;
	for(int i = 1; i < sqrt(n); i++)
	
	if(n % i == 0) divisors.push_back(i), divisors.push_back(n / i);
	
	//check if the number is perfect square so we dont repeat factors
	if(sqrt(n) == int(sqrt(n))) divisors.push_back(sqrt(n));
	
	return divisors;
}

```
### problems
[Perfect number](https://leetcode.com/problems/perfect-number/)</br>
### Resources
[YT - mostafa saad](https://youtu.be/-5ApOQDhBtU)</br>



## Prime numbers
### Primality test
**a prime number** is a number that can only be divided by 1 and itself
we can determine if a number is prime or not by order of O( $\sqrt{n}$ )
```cpp
bool is_prime(ll n){

	if(n < 2 || (n % 2 == 0 && n != 2)) return false;
	
	for(int i = 3; i <= sqrt(n); i += 2)
	
	if(n % i == 0) return false;
	
	return true;

}
```
### prime factorization 
there is a theory that any number can be represented by a collection of prime numbers risen to a a certain power 
$$\Huge n = p_1^a \times p_2^b \times p_3^c \times \dots $$
in the worst case this algorithm wil get excuted inorder of O( $\large\sqrt{n}$ ) but that is only the case for prime numbers.
```cpp
vector < int > prime_factorization(ll n){

	vector < int > factors;
	
	while(n % 2 == 0) factors.push_back(2), n /= 2;
	
	for(int i = 3; i <= sqrt(n); i += 2)
	
		while(n % i == 0) factors.push_back(i), n /= i;
	
	if(n > 2) factors.push_back(n);
	
	return factors;
}
```
[problem](https://www.codechef.com/problems/GEEK09)
## binary exponatation
it's a an algorithm to calculate the a number raised to a certain power in order of O( $\log{n}$ )
instead of order of O(n)
 ```cpp
 ll fast_power(ll x , ll b)

{

    ll result = 1;

    while(b)

    {

        if(b &1 )

            result*=x;

        x*=x;

        b/=2;

    }

    return result;

}
```
#### resources
[YT - errichto](https://www.youtube.com/watch?v=L-Wzglnm4dM&t=1s)</br>
[YT - Mr algortihm](https://www.youtube.com/watch?v=SsAQaWHe8oc&t=286s)


## GCD & LCM
### resources
[video on GCD]( https://www.youtube.com/watch?v=7HCd074v8g8&t=18s)</br>
[1 - article on GCD](https://www.geeksforgeeks.org/euclidean-algorithms-basic-and-extended/)</br>
[2- article on GCD](https://www.khanacademy.org/computing/computer-science/cryptography/modarithmetic/a/the-euclidean-algorithm)</br>
[article on LCM ](https://www.geeksforgeeks.org/program-to-find-lcm-of-two-numbers/)
</br>
[video on GCD & LCM](https://youtu.be/YklnFXpq0ZE?t=138)</br>

## Permutations & Combinations
### resources 
[article on nPr & nCr](https://www.mathsisfun.com/combinatorics/combinations-permutations.html)

