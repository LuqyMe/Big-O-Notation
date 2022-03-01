#Time_Complexity

#include <iostream>
using namespace std;

#O(1)
int main(){
     cout << "testing" << endl;
     return 0;
 }

# O(Log n)
  #include<iostream>
#include<algorithm>
#include<array>

const size_t arraySize = 10;

void printArray(std::array<int, arraySize> &angka){
    std::cout << "Array: ";
    for(int &a : angka){
        std::cout << a << " ";
    }
    std::cout << std::endl;
}

int main(){
    std::array<int, arraySize> angka = {3,4,5,1,2,6,8,7,9,0};

    int angkaCari = 5;
    bool ketemu;

    std::sort(angka.begin(), angka.end());
    ketemu = std::binary_search(angka.begin(), angka.end(), angkaCari);
    printArray(angka);

    std::cout << ketemu << std::endl;
    std::cin.get();
    return 0;
}

# O(n)
 int main(){
     int i, n;
     cout << "Masukkan bilangan : " << endl;
     cin >> n;
     for (i=1;i<=n;i++){
         cout << i << " ";
     }
     return 0;
 }
                      
# O (n log n)
#include<iostream>
using namespace std;

int linearSearch(int array[], int size, int searchValue){
    for(int i = 0; i < size; i++){
        if(searchValue == array[i]){
            return i;
        }
    }

    return -1;
}

int main(){
    int a[] = {15,23,4,21,54,36};
    int userValue;

    cout << "Masukkan angka : " << endl;
    cin >> userValue;

    int result = linearSearch(a,6,userValue);

    if(result >=0){
        cout << "Nomer " << a[result] << " ditemukan dalam index " << result << endl;
    }
    else{
        cout << "Nomer" << userValue << "tidak ditemukan." << endl;
    }
}                  
