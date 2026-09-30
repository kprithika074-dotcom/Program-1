#include <iostream>
using namespace std;

int main() {
    int a[100], n, i, sum = 0;
    int max, min;

    cout << "Enter number of elements: ";
    cin >> n;

    cout << "Enter " << n << " elements:" << endl;

    for (i = 0; i < n; i++) {
        cin >> a[i];
    }

    cout << "\nArray elements are: ";
    for (i = 0; i < n; i++) {
        cout << a[i] << " ";
        sum = sum + a[i];
    }

    max = a[0];
    min = a[0];

    for (i = 1; i < n; i++) {
        if (a[i] > max)
            max = a[i];

        if (a[i] < min)
            min = a[i];
    }

    cout << "\n\nSum = " << sum;
    cout << "\nAverage = " << (float)sum / n;
    cout << "\nLargest element = " << max;
    cout << "\nSmallest element = " << min;

    return 0;
}
