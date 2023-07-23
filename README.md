# 0x1B. C - Sorting algorithms & Big O
### TEAM PROJECT BY - LAWRENCE MADUABUCHI & ABDULLAHI NGUI

## GENERAL :open_book::open_book::open_book::

<ol>
<li>Sorting algorithm</li>
<li>Big O notation</li>
<li>Sorting algorithms animations</li>
<li>CS50 Algorithms explanation in detail by David Malan</li>
<li>All about sorting algorithms</li>
</ol>

## RESOURCES:

<ol>
<li><a href="https://intranet.alxswe.com/rltoken/-j5MKLBlzZAC2RfJ5DTBIg" title="Sorting Algorithm" target="_blank">sorting</a> </li>
<li><a href="https://intranet.alxswe.com/rltoken/WRvrE2BaNVQFssHiUATTrw" title="Big Notation" target="_blank">Big Notation</a> </li>
<li><a href="https://intranet.alxswe.com/rltoken/ol0P7NbYVb5R31iOv4Q40A" title="Sorting Algorithm" target="_blank">Sorting Algorithm</a> </li>
<li><a href="https://intranet.alxswe.com/rltoken/_I0aEvhfJ66Xyob6dd9Utw" title="Algorithm in 6 Minutes" target="_blank">16 minutes Algorithm</a> </li>
<li><a href="https://intranet.alxswe.com/rltoken/Ea93HeEYuNkOL7sGb6zzGg" title="CS50 Algorithm explaination by David Malan" target="_blank">CS50 Algorithm by David Malan</a> </li>
</ol>


## FILES :Data Structure and Functions::bookmark_tabs::bookmark_tabs::
## Files
All of the following files are programs written in C:

| Filename | Description |
| -------- | ----------- |
| ` 0. Bubble sort; 0-bubble_sort.c, 0-O`| Write a function that sorts an array of integers in ascending order using the Bubble sort algorithm.|
| ` 1. Insertion sort` | Write a function that sorts a doubly linked list of integers in ascending order using the Insertion sort algorithm|
| ` 2. Selection sort; 2-selection_sort.c, 2-O` | Write a function that sorts an array of integers in ascending order using the Selection sort algorithm|
| ` 3. Quick sort` | Write a function that sorts an array of integers in ascending order using the Quick sort algorithm.|
| ` 4. Shell sort - Knuth Sequence` | Write a function that sorts an array of integers in ascending order using the Shell sort algorithm, using the Knuth sequence.|
| ` 5. Cocktail shaker sort` | Write a function that sorts a doubly linked list of integers in ascending order using the Cocktail shaker sort algorithm.|
| ` 6. Counting sort` | Write a function that sorts an array of integers in ascending order using the Counting sort algorithm.|
| ` 7. Merge sort` | Write a function that sorts an array of integers in ascending order using the Merge sort algorithm.|
| ` 8. Heap sort` | Write a function that sorts an array of integers in ascending order using the Heap sort algorithm|
| ` 9. Radix sort` | Write a function that sorts an array of integers in ascending order using the Radix sort algorithm.|
| ` 10. Bitonic sort` | Write a function that sorts an array of integers in ascending order using the Bitonic sort algorithm.|
| ` 11. Quick Sort - Hoare Partition scheme` | Write a function that sorts an array of integers in ascending order using the Quick sort algorithm.|
| ` 12. Dealer; 1000-sort_deck.c, deck.h` | Write a function that sorts a deck of cards.|

### print_array, and print_list functions:

**<p>Write a function that sorts an array of integers in ascending order using the Bubble sort algorithm</p>**

<pre><code>alex@/tmp/sort$ cat 0-main.c 
#include <stdio.h>
#include <stdlib.h>
#include "sort.h"

/**
* main - Entry point
*
* Return: Always 0
*/
int main(void)
{
int array[] = {19, 48, 99, 71, 13, 52, 96, 73, 86, 7};
size_t n = sizeof(array) / sizeof(array[0]);

print_array(array, n);
printf("\n");
bubble_sort(array, n);
printf("\n");
print_array(array, n);
return (0);
}

alex@/tmp/sort$ gcc -Wall -Wextra -Werror -pedantic  -std=gnu89 0-bubble_sort.c 0-main.c print_array.c -o bubble
alex@/tmp/sort$ ./bubble
19, 48, 99, 71, 13, 52, 96, 73, 86, 7

19, 48, 71, 99, 13, 52, 96, 73, 86, 7
19, 48, 71, 13, 99, 52, 96, 73, 86, 7
19, 48, 71, 13, 52, 99, 96, 73, 86, 7
19, 48, 71, 13, 52, 96, 99, 73, 86, 7
19, 48, 71, 13, 52, 96, 73, 99, 86, 7
19, 48, 71, 13, 52, 96, 73, 86, 99, 7
19, 48, 71, 13, 52, 96, 73, 86, 7, 99
19, 48, 13, 71, 52, 96, 73, 86, 7, 99
19, 48, 13, 52, 71, 96, 73, 86, 7, 99
19, 48, 13, 52, 71, 73, 96, 86, 7, 99
19, 48, 13, 52, 71, 73, 86, 96, 7, 99
19, 48, 13, 52, 71, 73, 86, 7, 96, 99
19, 13, 48, 52, 71, 73, 86, 7, 96, 99
19, 13, 48, 52, 71, 73, 7, 86, 96, 99
13, 19, 48, 52, 71, 73, 7, 86, 96, 99
13, 19, 48, 52, 71, 7, 73, 86, 96, 99
13, 19, 48, 52, 7, 71, 73, 86, 96, 99
13, 19, 48, 7, 52, 71, 73, 86, 96, 99
13, 19, 7, 48, 52, 71, 73, 86, 96, 99
13, 7, 19, 48, 52, 71, 73, 86, 96, 99
7, 13, 19, 48, 52, 71, 73, 86, 96, 99

7, 13, 19, 48, 52, 71, 73, 86, 96, 99
</code></pre>
**<p>Write a function that sorts a doubly linked list of integers in ascending order using the Insertion sort algorithm</p>**

<pre><code>alex@/tmp/sort$ cat 1-main.c
#include <stdio.h>
#include <stdlib.h>
#include "sort.h"

/**
* main - Entry point
*
* Return: Always 0
*/
int main(void)
{
int array[] = {19, 48, 99, 71, 13, 52, 96, 73, 86, 7};
size_t n = sizeof(array) / sizeof(array[0]);

print_array(array, n);
printf("\n");
bubble_sort(array, n);
printf("\n");
print_array(array, n);
return (0);
}#include <stdio.h>
#include <stdlib.h>
#include "sort.h"

/**
* create_listint - Creates a doubly linked list from an array of integers
*
* @array: Array to convert to a doubly linked list
* @size: Size of the array
*
* Return: Pointer to the first element of the created list. NULL on failure
*/
listint_t *create_listint(const int *array, size_t size)
{
listint_t *list;
listint_t *node;
int *tmp;

list = NULL;
while (size--)
{
    node = malloc(sizeof(*node));
    if (!node)
        return (NULL);
    tmp = (int *)&node->n;
    *tmp = array[size];
    node->next = list;
    node->prev = NULL;
    list = node;
    if (list->next)
        list->next->prev = list;
}
return (list);
}
/**
* main - Entry point
*
* Return: Always 0
*/
int main(void)
{
listint_t *list;
int array[] = {19, 48, 99, 71, 13, 52, 96, 73, 86, 7};
size_t n = sizeof(array) / sizeof(array[0]);

list = create_listint(array, n);
if (!list)
    return (1);
print_list(list);
printf("\n");
insertion_sort_list(&list);
printf("\n");
print_list(list);
return (0);
}

alex@/tmp/sort$ gcc -Wall -Wextra -Werror -pedantic  -std=gnu89 1-main.c 1-insertion_sort_list.c print_list.c -o insertion
alex@/tmp/sort$ ./insertion
19, 48, 99, 71, 13, 52, 96, 73, 86, 7

19, 48, 71, 99, 13, 52, 96, 73, 86, 7
19, 48, 71, 13, 99, 52, 96, 73, 86, 7
19, 48, 13, 71, 99, 52, 96, 73, 86, 7
19, 13, 48, 71, 99, 52, 96, 73, 86, 7
13, 19, 48, 71, 99, 52, 96, 73, 86, 7
13, 19, 48, 71, 52, 99, 96, 73, 86, 7
13, 19, 48, 52, 71, 99, 96, 73, 86, 7
13, 19, 48, 52, 71, 96, 99, 73, 86, 7
13, 19, 48, 52, 71, 96, 73, 99, 86, 7
13, 19, 48, 52, 71, 73, 96, 99, 86, 7
13, 19, 48, 52, 71, 73, 96, 86, 99, 7
13, 19, 48, 52, 71, 73, 86, 96, 99, 7
13, 19, 48, 52, 71, 73, 86, 96, 7, 99
13, 19, 48, 52, 71, 73, 86, 7, 96, 99
13, 19, 48, 52, 71, 73, 7, 86, 96, 99
13, 19, 48, 52, 71, 7, 73, 86, 96, 99
13, 19, 48, 52, 7, 71, 73, 86, 96, 99
13, 19, 48, 7, 52, 71, 73, 86, 96, 99
13, 19, 7, 48, 52, 71, 73, 86, 96, 99
13, 7, 19, 48, 52, 71, 73, 86, 96, 99
7, 13, 19, 48, 52, 71, 73, 86, 96, 99

7, 13, 19, 48, 52, 71, 73, 86, 96, 99
</code></pre>

</code></pre>
**<p>Write a function that sorts an array of integers in ascending order using the Selection sort algorithm</p>**

<pre><code>alex@/tmp/sort$ cat 2-main.c
#include <stdio.h>
#include <stdlib.h>
#include "sort.h"

/**
* main - Entry point
*
* Return: Always 0
*/
int main(void)
{
int array[] = {19, 48, 99, 71, 13, 52, 96, 73, 86, 7};
size_t n = sizeof(array) / sizeof(array[0]);

print_array(array, n);
printf("\n");
selection_sort(array, n);
printf("\n");
print_array(array, n);
return (0);
}

alex@/tmp/sort$ gcc -Wall -Wextra -Werror -pedantic  -std=gnu89 
2-main.c 2-selection_sort.c print_array.c -o select
alex@/tmp/sort$ ./select
19, 48, 99, 71, 13, 52, 96, 73, 86, 7

7, 48, 99, 71, 13, 52, 96, 73, 86, 19
7, 13, 99, 71, 48, 52, 96, 73, 86, 19
7, 13, 19, 71, 48, 52, 96, 73, 86, 99
7, 13, 19, 48, 71, 52, 96, 73, 86, 99
7, 13, 19, 48, 52, 71, 96, 73, 86, 99
7, 13, 19, 48, 52, 71, 73, 96, 86, 99
7, 13, 19, 48, 52, 71, 73, 86, 96, 99

7, 13, 19, 48, 52, 71, 73, 86, 96, 99
alex@/tmp/sort$
</code></pre>
<code><pre>
**<p>Write a function that sorts an array of integers in ascending order using the Shell sort algorithm, using the Knuth sequence</p>**

<pre><code>alex@/tmp/sort$ cat 100-main.c
#include <stdio.h>
#include <stdlib.h>
#include "sort.h"

/**
 * main - Entry point
 *
 * Return: Always 0
 */
int main(void)
{
    int array[] = {19, 48, 99, 71, 13, 52, 96, 73, 86, 7};
    size_t n = sizeof(array) / sizeof(array[0]);
    print_array(array, n);
    printf("\n");
    shell_sort(array, n);
    printf("\n");
    print_array(array, n);
    return (0);
}
