# sgd#include <conio.h>
#include <iostream.h>

template < class T>
	void nhap(T a[], int n)
	{
		int i;
		cout << "Nhap cac phan tu cua mang :\n";
		for (i = 0; i < n; i++)
		{
			cout << "A[" << i + 1 << "]=";
			cin >> a[i];
		}
	}

template < class T>
	void xuat(T a[], int n)
	{
		int i, j;
		for (i = 0; i < n; i++) cout << a[i] << " ";
	}

template < class T>
	void sapxep(T a[], int n)
	{
		int i, j;
		T tg;
		for (i = 0; i < n - 1; i++)
			for (j = i + 1; j < n; j++)
				if (a[i] > a[j])
				{
					tg = a[i];
					a[i] = a[j];
					a[j] = tg;
				}
	}

void main()
{
	int a[100], n;
	float b[100];
	clrscr();
	cout << "Nhap so phan tu n= ";
	cin >> n;
	cout << "\nNhap mang so nguyen:\n";
	nhap(a, n);
	cout << "Mang truoc khi sap xep :\n";
	xuat(a, n);
	sapxep(a, n);
	cout << "\nMang sau khi sap xep :\n";
	xuat(a, n);
	cout << "\nNhap mang so thuc:\n";
	nhap(b, n);
	cout << "Mang truoc khi sap xep :\n";
	xuat(b, n);
	sapxep(b, n);
	cout << "\nMang sau khi sap xep :\n";
	xuat(b, n);
}
