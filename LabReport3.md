# Part 1
## The Bug I want to cover is Failure-inducing Input
# Failure-Inducing Input:
`@Test 
public void testReverseInPlaceFailure() { 
    int[] input = {1, 2, 3, 4, 5};
    int[] expected = {5, 4, 3, 2, 1};
    ArrayExamples.reverseInPlace(input);
    assertArrayEquals(expected, input);
}`
# Non-failure Inducing Input:
`@Test
public void testReverseInPlaceSuccess() {
    int[] input = {1, 2, 3, 4, 5};
    int[] expected = {1, 2, 3, 4, 5};
    ArrayExamples.reverseInPlace(input);
    assertArrayEquals(expected, input);
}`
# Symptom for this bug would be:
## Before:
`public static void reverseInPlace(int[] arr) {
    int start = 0;
    int end = arr.length - 1;
    while (start < end) {
        int temp = arr[start];
        arr[start] = arr[end];
        arr[end] = temp;
        start++;
        end--;
    }
}`
## After:
`public static void reverseInPlace(int[] arr) {
    for (int i = 0; i < arr.length / 2; i++) {
        int temp = arr[i];
        arr[i] = arr[arr.length - i - 1];
        arr[arr.length - i - 1] = temp;
    }
}`
## Explanation:
The bug in the reverseInPlace method was due to incorrect indexing while swapping elements. In the original implementation, the while loop swaps elements starting from the beginning and end of the array until they meet in the middle. However, this logic doesn't handle arrays with odd lengths properly, as the middle element gets swapped twice, effectively reversing it back to its original position.
The fix changes the implementation to iterate only up to half of the array length, swapping the elements at index i with the corresponding element at index arr.length - i - 1. This ensures that each element is swapped only once, resulting in the correct reversal of the array.

# Part 2
## -v (invert match) - I found out about the -v option by searching online for advanced grep options.
# Examples:
## 1. Show lines not containing a specific pattern in files:
`grep -v "debug" ./technical/*.log`
## Output:
`file1.log:Error occurred in line 10.
file2.log:An error was found in the log.`
## Explanation: This command displays lines in .log files within the ./technical directory that do not contain the word "debug". It's useful when you want to filter out specific lines from the output.

## 2. Show lines not containing a specific pattern in directories:
`grep -vir "trace" ./technical/`
## Output:
`./technical/file3.log:Error: Memory usage high.
./technical/subdirectory/file4.log:Error encountered.`
## Explanation: Using the -v option with -r and -i, this command recursively searches through directories for lines not containing "trace" in .log files, ignoring case.
