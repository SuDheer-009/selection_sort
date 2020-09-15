# selection_sort
#include <stdio.h>
int main()
{
  int array[500], n, x, y, p, f;
  printf("Enter number of elements\n");
  scanf("%d", &n);
  printf("Enter %d integers\n", n);
  for (x = 0; x < n; x++)
    scanf("%d", &array[x]);
  for (x = 0; x < (n - 1); x++)
  {
    p = x;
    for (y = x + 1; y < n; y++)
    {
      if (array[p] > array[y])
        p = y;
    }
    if (p != x)
    {
      f = array[x];
      array[x] = array[p];
      array[p] = f;
    }
  }
  printf("Sorted list in ascending order:\n");
  for (x = 0; x < n; x++)
    printf("%d\n", array[x]);
  return 0;
}
