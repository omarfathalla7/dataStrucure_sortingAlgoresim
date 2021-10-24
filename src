/*
 static void printArray(int arr[]){  // An utility function to print array of size n
        
        int n = arr.length;
        for (int i=0; i<n; ++i)
            System.out.print(arr[i] + " ");
        System.out.println();
    }
 */
package data;
import java.util.Scanner; 


public class Data { 
    
    
     static void bubbleSort(int[] arr) {  
        int n = arr.length;  
        int temp = 0;  
         for(int i=0; i < n; i++){  
                 for(int j=1; j < (n-i); j++){  
                          if(arr[j-1] > arr[j]){  
                                 //swap elements  
                                 temp = arr[j-1];  
                                 arr[j-1] = arr[j];  
                                 arr[j] = temp;  
                         }  
                          
                 }  
         }  // end function bubble  sort
         
     

   }
 ///////////////////////////////////////////////  
  static  void insertionSort(int array[])
   {  
        int n = array.length;  
        for (int j = 0; j < n; j++) {  
            int key = array[j];  
            int i = j-1;  
            while ( (i >= 0) && ( array [i] > key ) ) {  
                array [i+1] = key;  
                i--;  
            }  
            array[i+1] = key;  
        }  
    } //end function insertion sort
  //////////////////////////////////////////////////
 void merge(int arr[], int beg, int mid, int end)  
{  
  
int l = mid - beg + 1;  
int r = end - mid;  
  
int LeftArray[] = new int [l];  
int RightArray[] = new int [r];  
  
for (int i=0; i<l; ++i)  
LeftArray[i] = arr[beg + i];  
  
for (int j=0; j<r; ++j)  
RightArray[j] = arr[mid + 1+ j];  
  
  
int i = 0, j = 0;  
int k = beg;  
while (i<l&&j<r)  
{  
if (LeftArray[i] <= RightArray[j])  
{  
arr[k] = LeftArray[i];  
i++; }  else  
{  
arr[k] = RightArray[j];  
j++;  
}  
k++;  
}  
while (i<l)  
{  
arr[k] = LeftArray[i];  
i++;  
k++;  
}  
  
while (j<r)  
{  
arr[k] = RightArray[j];  
j++;  
k++;  
}  
}  
  
void sort(int arr[], int beg, int end)  
{  
if (beg<end)  
{  
int mid = (beg+end)/2;  
sort(arr, beg, mid);  
sort(arr , mid+1, end);  
merge(arr, beg, mid, end);  
}  
}  
  
 ////////////////////////////////////////////////////////
  
  //Quick sort
 static void swap(int[] arr, int i, int j)//function to swap two elements
{
    int temp = arr[i];
    arr[i] = arr[j];
    arr[j] = temp;
}/* This function takes last element as pivot, places
   the pivot element at its correct position in sorted
   array, and places all smaller (smaller than pivot)
   to left of pivot and all greater elements to right
   of pivot */
 static int partition(int[] arr, int low, int high){
     int pivot = arr[high]; //pivot
         int i = (low - 1); //Index of smaller element and indicates the right 
                            //position of pivot found so far
   for(int j = low; j <= high - 1; j++){
  if (arr[j] < pivot) {// If current element is smaller than the pivot
            i++;// Increment index of smaller element
         swap(arr, i, j);}}
             swap(arr, i + 1, high);
        return (i + 1);}
 static void quickSort(int[] arr, int low, int high){/*main function that implement
     quicksort as arr[]is the array to be sorted ,low is the index of starting 
     and high is the index of end */
    if (low < high) {
    int pi = partition(arr, low, high); // pi is partitioning index, arr[p]is now at right place
     quickSort(arr, low, pi - 1);//sort elements before partition
     quickSort(arr, pi + 1, high);//sort eleents after partition
    }}//end function quicksort5
  
  ///////////////////////////////////////////////////////
  
   //SHELL SORT

    int sort(int arr[])// function to sort arr using shellSort 
    {
        int n = arr.length;
         for (int gap = n/2; gap > 0; gap /= 2) // Start with a big gap, then reduce the gap
        {
            for (int i = gap; i < n; i += 1)
            {               
                int temp = arr[i];/*add a[i] to the elements that have been gap 
                sorted save a[i] in temp and make a hole at position i*/
                int j;
                for (j = i; j >= gap && arr[j - gap] > temp; j -= gap)
                    arr[j] = arr[j - gap];/*shift earlier gap-sorted elements up until
                the correct location for a[i] is found*/
                
                  arr[j] = temp; //put temp (the original a[i]) in its correct LOCATION
            }
        }
                 return 0;
    }

  /////////////////////////////////////////////////////
  
 static void sort1(int arr[])
    {
      int n = arr.length;
     for (int i = n / 2 - 1; i >= 0; i--)        // Build heap (rearrange array)
            heapify(arr, n, i);
    for (int i = n - 1; i > 0; i--) { // One by one extract an element from heap
     int temp = arr[0];             // Move current root to end
            arr[0] = arr[i];
            arr[i] = temp;
            heapify(arr, i, 0);            // call max heapify on the reduced heap
    }
    }
 static void heapify(int arr[], int n, int i){/* To heapify a subtree rooted with node i which is
                                        an index in arr[]. n is size of heap*/
     int largest = i; // Initialize largest as root
        int l = 2 * i + 1; // left = 2*i + 1
        int r = 2 * i + 2; // right = 2*i + 2
         if (l < n && arr[l] > arr[largest])         // If left child is larger than root
            largest = l;
     if (r < n && arr[r] > arr[largest])    // If right child is larger than largest so far
            largest = r;
         if (largest != i) {        // If largest is not root
            int swap = arr[i];
            arr[i] = arr[largest];
            arr[largest] = swap;
            heapify(arr, n, largest);// Recursively heapify the affected sub-tree
        }
    }
 

  
  /////////////////////////////////////////////
 /*main function*/
    public static void main(String[] args) {
    do{   
        Scanner input= new Scanner(System.in);    //System.in is a standard input stream  
     System.out.println("ENTER THE SIZE OF ARRAY");
       int n=input.nextInt();  
         int arr[] = new int [n];
        System.out.println("ENTER ELEMENT OF ARRAY");
        for(int i=0;i<n;++i){
         arr[i]=input.nextInt();
      }
      System.out.println("to bubble sort enter [1]");
      System.out.println("to insertion sort enter [2]");
      System.out.println("to merge sort enter [3]");
      System.out.println("to Quick sort enter [4]");
      System.out.println("to shell sort enter [5]");
      System.out.println("to heap sort enter [6]");
      
      int X=input.nextInt();
   
   switch (X) 
 {
    case 1:
          System.out.println("After bubble Sort");  
        bubbleSort(arr);//sorting array elements using bubble sort  
                for(int i:arr){  
                        System.out.print(i + " ");  
                }
                System.out.println("\n"); 
    break;
    case 2:
     System.out.println("After Insertion Sort");  
           insertionSort(arr);//sorting array using insertion sort        
              for(int i:arr){    
             System.out.print(i+" ");    
            }  
             System.out.println("\n"); 
    break;
    case 3:
         System.out.println("merge sort"); 
     Data ob2 = new Data();  
ob2.sort(arr, 0, arr.length-1);  
   for(int i:arr){
       System.out.println(i+" ");
   }
     System.out.println("\n");
     break;
    case 4:
          System.out.println("After quick Sort"); 
            quickSort(arr, 0, n - 1);;//sorting array using quick sort      
               
              for(int i:arr){    
             System.out.print(i+" ");    
            }  
             System.out.println("\n");
    break;
    case 5:
         Data ob = new Data();
        ob.sort(arr);
                System.out.println(" After shellSort");  
                for(int i:arr){  
                        System.out.print(i + " ");  
                }
                System.out.println("\n"); 
    break;
    case 6:
        Data ob3 = new Data();
        ob3.sort1(arr);
         System.out.println("Array After heapSort");  
         for(int i:arr){  
           System.out.print(i + " ");  
                }
                System.out.println("\n"); 

     break;
    
  default:
    System.out.println("DATA STRUCTURE");
}
      } while( true);
    }

  
}
    
    

    
    
    

