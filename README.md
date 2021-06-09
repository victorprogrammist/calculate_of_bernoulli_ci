# calculate_of_bernoulli_ci

Author Telnov Victor, v-telnov@yandex.ru
 
This code under licence CC BY-NC-ND

```txt
// It evaluates the probability by the value of area integral of Bernoulli formula.
// Such value it is the confidence interval of probability - the probability of the probability -
// for the case of the uniform distribution of a probability.

// With dir_right_to_left == false
//   calculates from zero to one the area equal p_quantile.
//   p_quantile is the confidence interval - probability of probability.

//   For example, if p_quantile == 0.3,
//    when k success, from n attemps is 1/1,
//    then probability of process will be more or equal 0.5477 with the probability 0.3
//    for k = 1 from n = 2 - probability of process more or equal 0.3633
//    for k = 1 from n = 3 - probability of process more or equal 0.2724
//     (it is low border of the distribution of the probability).

// if dir_right_to_left == true then it calculates area from one to zero
//     (high border of the distribution of the probability)

// er - it is a residual error which is somewhat arbitrary

double bernoulli_integral_inverse(
        unum k, unum n,
        double p_quantile, bool dir_right_to_left = false,
        double er = 0.00001);
        
```
