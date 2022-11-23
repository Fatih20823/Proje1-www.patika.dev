# Proje1-www.patika.dev

* Insertion sort
		public static void main(String[] arg) {
 
			int[] dizi = new int[] {22,27,16,2,18,6};
			
			for (int i = 1; i < dizi.length; i++) {
			    int key = dizi[i];
			    int j = i-1;
			    while(j>=0 && dizi[j]>key) {
			    	dizi[j+1] = dizi[j];
			    	j = j-1;
			    }
			    dizi[j+1]=key;
			}
			
			
			for (int i = 0; i < dizi.length; i++) {   //Output [2 3 4 5 6 7 8 9 15]
				System.out.print(dizi[i]+" ");
			}
//	    Öncelikle dizideki ikinci eleman başlangıç elemanı olarak seçilir ve kendisinden önce gelen 
//	yani solunda eleman ile kıyaslanır. Eğer birinci eleman ikinci elemandan büyükse yer değiştirirler. 
//	Değilse bir sonraki elemana geçilir. İkinci eleman birinci indise 
//	alınır ilk eleman ikincisi indise alınır ve üçüncü eleman ile ikinci eleman kıyaslanır.  
//	Bu şekilde dizi elemanlarının hepsine bakılana kadar ve doğru sıralama elde edilene kadar işlem 
//	devam eder.
		}
    
    Big-O gösterimi O(n^2)'dir
    
    Time Complexity: Dizi sıralandıktan sonra 18 sayısı aşağıdaki case'lerden hangisinin kapsamına girer? Yazınız
    
    Average-case: Bu case, verilen input setindeki değerlerin dizi içerisindeki dağılımına göre belirlenir. 
    Bu örnek için average-case aradığımız değerin, dizi’nin ortasındaki, yani 18 değerinin olması olabilir.
    
    * Selection Sort
    		public static void main(String[] arg) {

			int[] dizi = new int[] {7,3,5,8,2,9,4,15,6};
			
			for (int i = 0; i < dizi.length;i++) {          
				int enKucuk=dizi[i],enKucukyeri=i;
				for(int j = i+1; j < dizi.length;j++) {
					if(dizi[j]<enKucuk) {
						enKucuk = dizi[j];
						enKucukyeri = j;							
					}
	
				}
				int temp = dizi[i];
				dizi[i] = dizi[enKucukyeri];
				dizi[enKucukyeri] = temp;									
			}
			
			
			for (int i = 0; i < dizi.length; i++) {   //Output [2 3 4 5 6 7 8 9 15]
				System.out.print(dizi[i]+" ");
			}
//    Algoritma şu şekilde çalışır. Listenin ilk elemanına alır (7). 
//  Kendinden sonraki tüm sayılar ile kıyaslanır. Listedeki en küçük sayıyı 
//  bulduğumuzda indisdeki değer (7) ile yer değiştiririz.
		}
