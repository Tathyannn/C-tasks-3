#include <iostream>
using namespace std;

int main()
{
    const int n = 10;
    int matrix[n][n];

    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n; j++) {
            if (i == j) {
                matrix[i][j] = 0;
            } else {
                matrix[i][j] = 1;
            }
        }
    }

    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n; j++) {
            cout << matrix[i][j] << "   ";
        }
        cout << endl; 
    }

    return 0;
}



int main()
{
    const int n = 10;
    int x[n], y;

    for (int i = 0; i < n; i++) {
        cout << "x[" << i << "]=";
        cin >> x[i];
    }

    bool a = true;
    while (a) {
        a = false;
        for (int j = 0; j < n - 1; j++) {
            if (x[j] > x[j + 1]) {
                a = true;
                y = x[j];
                x[j] = x[j + 1];
                x[j + 1] = y;
            }
        }
    }

    for (int j = 0; j < n; j++) { 
        cout << x[j] << endl;
    }

    return 0;
}
