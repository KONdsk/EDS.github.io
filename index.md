# A 素数
```Cpp
int main()
{
  int n;
  cin >> n;
  for (int i = 0; i < n; i++)
  {
    int t, sign = 0;
    cin >> t;
    for (int i = 2; i < t; i++)
      if (t % i == 0)
        sign--;

    if (sign < 0 || t == 0 || t == 1)
      cout << "No" << endl;
    else
      cout << "Yes" << endl;
  }
  
  return 0;
}
```

# B 三角形
```Cpp

#include <iostream>
using namespace std;
int main()
{
  int a, b, c;

  cin >> a >> b >> c;
  if (a < b + c && a > abs(b - c))
  {
    double p = 0.5 * (a + b + c);
    double ans = sqrt((p - c) * (p - a) * (p - b) * p);
    printf("%.2f", ans);
  }
  else
  {
    cout << "Fail";
  }

  return 0;
}
```

# D 鸡兔同笼
```Cpp
#include <iostream>
using namespace std;

int main()
{
  int a, b, m, n;
  cin >> n >> m;
  if (m == 0 || m % 2 != 0) {
    cout << "False!";
    return 0;
  }
  a = (4 * n - m) / 2;
  b = (m - 2 * n) / 2;
  if (a < 0 || b < 0) {
    cout << "False!";
    return 0;
  }
  cout << a << " " << b;

  return 0;
}
```

# H 结构体
```Cpp
#include <iostream>
using namespace std;

struct student {
  string name;
  int grade;
} a;

int main()
{
  student a[100];
  int n, sum = 0;
  cin >> n;

  for (int i = 0; i < n; i++) {
    cin >> a[i].name >> a[i].grade;
    sum += a[i].grade;
  }
  int ave = sum / n;
  for (int i = 0; i < n; i++) {
    if (a[i].grade >= ave)
      cout << a[i].name << " " << a[i].grade << endl;
  }

  return 0;
}
```
