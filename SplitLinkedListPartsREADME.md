# leet-day54

# Split Linked List in Parts

You are given the head of a singly linked list and an integer `k`. Your task is to split the linked list into `k` consecutive linked list parts. 

The objective is to ensure that the length of each part is as equal as possible, with no two parts having a size differing by more than one. If there are remaining nodes after dividing the list into `k` parts, these nodes should be evenly distributed among the first few parts, in the order of occurrence in the input list. Parts occurring earlier should always have a size greater than or equal to parts occurring later.

## Problem Statement

Given the head of a singly linked list and an integer `k`, split the linked list into `k` consecutive linked list parts.

### Input

- The number of nodes in the list is in the range `[0, 1000]`.
- `0 <= Node.val <= 1000`
- `1 <= k <= 50`

### Output

Return an array of the `k` parts, where each part is represented by a pointer to the head node.

## Example

### Example 1

Input:
```cpp
head = [1,2,3], k = 5
```

Output:
```
[[1],[2],[3],[],[]]
```

Explanation:
- The first element `output[0]` has `output[0].val = 1`, `output[0].next = null`.
- The last element `output[4]` is `null`, but its string representation as a `ListNode` is `[]`.

### Example 2

Input:
```cpp
head = [1,2,3,4,5,6,7,8,9,10], k = 3
```

Output:
```
[[1,2,3,4],[5,6,7],[8,9,10]]
```

Explanation:
- The input has been split into consecutive parts with size difference at most 1, and earlier parts are a larger size than the later parts.

## Approach

1. Calculate the length of the linked list.
2. Determine the size of each part and the number of parts with one extra node.
3. Iterate through the linked list, splitting it into parts and updating the pointers accordingly.
4. Return an array of pointers to the heads of these parts.

## Time Complexity

The time complexity of this solution is O(N), where N is the number of nodes in the linked list.
