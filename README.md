# B.z-sort

#include <iostream>

#include <algorithm>

using namespace std;

int arr[1000];

int res[1000];


int main()
{

	int n;
	cin >> n;

	int s = 0, e = n - 1;

	for (int i = 0; i < n; i++)
	{
		cin >> arr[i];
	}

	sort(arr, arr + n);

	for (int i = 0; i < n; i++)
	{
		if (i % 2 == 1)
		{
			res[i] = arr[e--];
		}
		else
			res[i] = arr[s++];
	}
	for (int i = 0; i < n; i++)
	{
		cout << res[i] << " ";
	}

	return 0;
}
