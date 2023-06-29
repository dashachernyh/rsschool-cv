# **CV**
<style>
   .round {
    border-radius: 100px; /* Радиус скругления */
    border: 3px solid sandybrown; /* Параметры рамки */
    box-shadow: 0 0 7px #666; /* Параметры тени */
   }
</style>
<img src="https://avatars.githubusercontent.com/u/55274971?v=4" width="100" height="111" class="round">  

1. Daria Chernyh
2. My contact:
   * Phone: +7 (999) 136-78-06
   * Email: dasha.chernyh.00@gmail.com
   * Telegram: @d_chernyh
3. Brief information:
   >I'm a second-year Master's student at the Lobachevsky University. 
   > I'm studying in the Applied Mathematics and Informatics faculty, focusing on research in [global optimization methods][1].
   > My aim is to gain experience at an IT company, work in real-time scenarios, and enhance my knowledge and professional
   > skills. Although I don't have extensive experience in the IT field, I have the desire and ability to quickly learn 
   > new information.
   > 
   > [1]:http://omega.sp.susu.ru/pavt2023/poster/018.pdf
4. My skills:
   * Programming language:
     * C
     * C++
     * Python
   * Framework:
     * Google test
     * Qt
   * OS:
     * Windows 7/10
     * Linux(Ubuntu)
   * Version control system:
     * Git (GitHub)
   * IDE
     * Visual Studio 2012/15/19
     * Clion
     * PyCharm
5. Code example on [LeetCode](https://leetcode.com/):
   >    [2217\. Find Palindrome With Fixed Length](https://leetcode.com/problems/find-palindrome-with-fixed-length/) 
   >    Given an integer array `queries` and a **positive** integer `intLength`, return *an array* `answer` *where* `answer[i]`
   >    is *either* the `queries[i]th` *smallest* ***positive palindrome*** *of length* `intLength` *or* `-1` *if no such 
   >    palindrome exists*.
    
      My solution:
      ````
      class Solution {
       public:
       vector<long long> kthPalindrome(vector<int>& queries, int intLength) {
           int count = intLength / 2;
           if (intLength % 2 == 0) {
               --count;
           }
           int lim = 9 * pow(10, count);
           vector<int> number(count + 1);
           vector<long long> res(queries.size());
           int copy_q;
           for(int i = 0; i < queries.size(); ++i) {
               copy_q = queries[i] - 1;
               if (copy_q >= lim) {
                   res[i] = -1;
                   continue;
               }
               for(int j = count; j >= 0; --j){
                   number[j] = copy_q % 10;
                   copy_q /= 10; 
               }
               number[0] += 1;
               long long palindrome = 0;
               if (intLength % 2 == 0) {
                   for (int k = 0, p = intLength - 1; k < count + 1; --p, ++k) {
                       palindrome += number[k] * pow(10, p);

                       palindrome += number[k] * pow(10, k);
                   }
               }
               else {
                   for (int k = 0, p = intLength - 1; k < count; --p, ++k) {
                       palindrome += number[k] * pow(10, p);

                       palindrome += number[k] * pow(10, k);
                   }
                   palindrome += number[count] * pow(10, count);
               }
                   res[i] = palindrome;
               }
           return res;
       }
    };
    ````
6. My experience:
   * Math tutor 2018-2022
   * Laboratory assistant at UNN 2022 - ...
7. Education:
   * Bachelor - Lobachevsky University (2018-2022) 
   * Intel Delta 11 Course "Additional Topics To The Software Engineering", March(2019)
   * Intel COMPUTER VISION SUMMER CAMP 2020, Julie (2020)
   * Master - Lobachevsky University (2022-2024)
8. English level : B1
