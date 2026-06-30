# DAY-12-OF-90-DAYS-CC-CHALLENGE-

# 1. Enough Space


Chef's computer has N GB of free space. He wants to save X files, each of size 1 GB and Y files, each of size 2 GB on his computer. Will he be able to do so?

Chef can save all the files on his computer only if the total size of the files is less than or equal to the space available on his computer.

Input Format

The first line contains an integer T, denoting the number of test cases. The T test cases then follow:
The first and only line of each test case contains three integers N,X,Y, denoting the free-space in computer, the number of 1 and 2 GB files respectively.

Output Format

For each test case, print YES if Chef is able to save the files and NO otherwise.

You may print each character of the string in uppercase or lowercase (for example, the strings yEs, yes, Yes and YES will all be treated as identical).

Constraints

1≤T≤100

1≤N,X,Y≤100

Sample 1:

Input

4
6 3 1
2 2 2
4 3 2
5 1 2

Output


YES

NO

NO

YES

Explanation:

Test case 1: The total size of files is 3+1⋅2=5, which is smaller than the remaining space on the computer. Thus Chef will be able to save all the files.

Test case 2: The total size of files is 2+2⋅2=6, which is greater than the remaining space on the computer. Thus Chef will not be able to save all the files.

Test case 3: The total size of files is 3+2⋅2=7, which is greater than the remaining space on the computer. Thus Chef will not be able to save all the files.

Test case 4: The total size of files is 1+2⋅2=5, which is equal to the remaining space on the computer. Thus Chef will be able to save all the files.




#include <bits/stdc++.h>
using namespace std;

int main() {
    int t;
    cin >> t;
    
    while (t--) {
        int N, X, Y;
        cin >> N >> X >> Y;
        
        if (N >= (X + 2 * Y)) 
            cout << "YES" << endl;
        
        else 
            cout << "NO" << endl;
        
    }
    
    return 0;
}


# 2. Volume Comparison



Alice has two objects:

A cuboid with length A units, height B units, and width C units.
A cube with an edge length of X units.
Alice wants to know which of the two objects has a larger volume, or if their volumes are equal.

Input Format

The first and only line of input will contain four space-separated integers A, B, C and X, the length of the cuboid, the width of the cuboid, the height of the cuboid, and the length of the edge of the cube.


Output Format

Print a single line containing the string:

"Cuboid", if the volume of the cuboid is greater than the volume of the cube.
"Cube", if the volume of the cube is greater than the volume of the cuboid.
"Equal", if both objects have equal volume.
Print the string without quotes.
You can print each character of the output in either uppercase or lowercase.
For example, the strings Cube, CUBE, cube, and CuBe are considered identical.

Constraints

1≤A,B,C,X≤10

Sample 1:

Input
Output
1 3 10 3
Cuboid

Explanation:

The volume of the cuboid is 1×3×10=30 cubic units.

The volume of the cube is 3^3 =27 cubic units.

The cuboid has larger volume.

Sample 2:
Input
Output
1 1 1 2
Cube

Explanation:

The volume of the cuboid is 1×1×1=1 cubic units.

The volume of the cube is 2^3 =8 cubic units.

The cube has larger volume.

Sample 3:
Input
Output
8 4 2 4

Equal

Explanation:

The volume of the cuboid is 8×4×2=64 cubic units.

The volume of the cube is 4^3 =64 cubic units.
Both objects have the same volume.

