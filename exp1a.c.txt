#include <stdio.h>
#include <math.h>

double calc_loge_loge(int n) {
  return log(log(n));
}

double calc_log2(int n) {
  return log2(n);
}

double calc_n_log2_n(int n) {
  return n * log2(n);
}

double calc_log2_fact(int n) {
  int i;
  double fact = 0;
  for (i = 1; i <= n; i++) {
    fact += log2(i);
  }
  return fact;
}

double calc_log2_square(int n) {
  return pow(log2(n), 2);
}

double calc_linear(int n) {
  return n;
}

double calc_cubic(int n) {
  return n * n * n;
}

double calc_power2(int n) {
  return pow(2, n);
}

double calc_power32(int n) {
  return pow(1.5, n);
}

double calc_exp(int n) {
  return exp(n);
}

int main() {
  int n;
  
  printf("n\tloge(loge(n))\tlog2(n)\tn*log2(n)\tlog2(n!)\t(log2(n))^2\tn\tn^3\t2^n\t(3/2)^n\te^n\n");
  
  for (n = 1; n <= 100; n++) {
    double loge_loge_n = calc_loge_loge(n);
    double log2_n = calc_log2(n);
    double n_log2_n = calc_n_log2_n(n);
    double log2_fact_n = calc_log2_fact(n);
    double log2_square_n = calc_log2_square(n);
    double linear_n = calc_linear(n);
    double cubic_n = calc_cubic(n);
    double power2_n = calc_power2(n);
    double power32_n = calc_power32(n);
    double exp_n = calc_exp(n);
    printf("%d\t%.1lf\t\t%.1lf\t%.1lf\t%.1lf\t%.1lf\t%.1lf\t%.1lf\t%.1lf\t%.1lf\t%.1lf\n", n, loge_loge_n, log2_n, n_log2_n, log2_fact_n, log2_square_n, linear_n, cubic_n, power2_n,power32_n,exp_n);
    // printf("%.3f\n",exp_n);
  }
    return 0;
}