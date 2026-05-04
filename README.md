# sem-4-prac-daa
'''


# insertion sort 
#include <iostream>
using namespace std;
int main()
{
    int n;

    cout << "Enter number of elements: ";
    cin >> n;

    int arr[1000];

    cout << "Enter elements:\n";
    for(int i = 0; i < n; i++)
    {
        cin >> arr[i];
    }

    int comparisons = 0;

    // Insertion Sort
    for(int i = 1; i < n; i++)
    {
        int key = arr[i];
        int j = i - 1;

        while(j >= 0)
        {
            comparisons++;   // counting comparison

            if(arr[j] > key)
            {
                arr[j + 1] = arr[j];
                j--;
            }
            else
            {
                break;
            }
        }

        arr[j + 1] = key;
    }

    cout << "\nSorted Array is:\n";
    for(int i = 0; i < n; i++)
    {
        cout << arr[i] << " ";
    }

    cout << "\nTotal Comparisons = " << comparisons;

    return 0;
}

'''
