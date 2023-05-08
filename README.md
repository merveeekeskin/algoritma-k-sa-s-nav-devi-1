
#include <stdio.h>


// Linear Search fonksiyonu tanımlanıyor


int linear_search(int arr[], int n, int x) {


// Dizinin her bir elemanı için eger aranan eleman bulunamıyorsa elemanın indeksini döndür



    for (int i = 0; i < n; i++) {
        if (arr[i] == x) {
       
            return i;
            }
    }
     // eğer eleman bulunamazsa -1 döndürür
    return -1;
}

int main() {


    int n;
    
    
    // dizinin boyutunu kullanıcıdan iste
    
    
    printf("Dizinin boyutunu giriniz: ");
    
    
    scanf("%d", &n);
    
    
    int arr[n];
    
    
    // dizinin her bir elemanını kullanıcıdan iste
    
    
    for (int i = 0; i < n; i++) {
    
    
        printf("Dizinin %d. elemanını giriniz: ", i+1);
        
        
        scanf("%d", &arr[i]);
        
        
    }

    int aranan;
    
    
    // aranacak elemanı kullanıcıdan iste
    
    
    printf("Aranacak elemanı giriniz: ");
    
    
    scanf("%d", &aranan);
    
    
// linear search fonksiyonunu kullanarak aranan elemanın indeksini bul


    int index = linear_search(arr, n, aranan);
    
    
    // eğer indeks -1 değilse ve sayı bulunmuşsa
    
    
    if (index != -1) {
    
    
        printf("%d elemanı dizinin %d. sırasında bulunmuştur.\n", aranan, index+1);
        
        
        // eğer indeks -1 ise ve indeks bulunmadıysa
        
        
    } else {
    
    
        printf("%d elemanı dizide bulunamamıştır.\n", aranan);
        
        
    }
    
    

    return 0;
    
    
}
