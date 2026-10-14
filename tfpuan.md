- **NetID:** tfpuan
- **Major:** Computer Science
- **Question that I chose from the memoization exercise:** Unique paths in a Grid with Obstacles
- **Link to the question article:** https://www.geeksforgeeks.org/dsa/unique-paths-in-a-grid-with-obstacles/#using-topdown-dpmemoization-omn-time-and-omn-space
- **My solution:**

\```
int uniPathRec(int i, int j, int** grid, int szGrid) {
    int r = szGrid;
    int c = szGrid;

    if (i == r || j == c) {
        return 0;
    }

    if (grid[i][j] == 1) {
        return 0;
    } 

    if (i == r-1 && j == c-1) {
        return 1;
    }

    return uniPathRec(i+1, j, grid, szGrid) + uniPathRec(i, j+1, grid, szGrid);
}

int uniquePaths(int** grid, int szGrid) {
    return uniPathRec(0, 0, grid, szGrid);
}

int main() {

	int** grid[3] = { { 0, 0, 0 },{ 0, 1, 0 },{ 0, 0, 0 } };

	printf(uniquePaths(grid));
}

\```
