# Stack
A program where i simulate a stack as an Abstract Data Type without using its default methods

_______________________________________________________________________________________________________________________________________________________________________
|      La Classe       |
|----------------------|

-Attributi 

    La classe è formata da 3 Attributi:

    Un array di stringhe che sarà il nostro stack
  
    Una costante DIM con valore 10 che mi serve per dare una grandezza allo stack
  
    Un variabile int di nome slotOcc che indicherà quanti slot sono stati occupati da una stringa
 
 -Codice della classe
 
    public class Stack{
      final int DIM = 10;
      String[] stack;
      private int slotOcc;
    }
    
-Costruttore

    public Stack(){
      stack = new String[DIM];
      slotOcc = 0;
    }

_______________________________________________________________________________________________________________________________________________________________________
|     I miei Metodi    |
|----------------------|

-Add

    public void add(String s){
        if(!isFull()){
            stack[slotOcc+1] = s;
            slotOcc++;
        }
    }

-Delete

    public void remove(){
        if(!isEmpty()){
            stack[slotOcc] = null;
            slotOcc--;
        }
    }
    
-Size
    
    public int getSize(){
		return slotOcc;
	}
    
-isFull

    public boolean isFull(){
		if(slotOcc == DIM){
			return true;
		}else return false;
	}

-isEmpty

    public boolean isEmpty(){
		if(slotOcc == 0){
			return true;
		}else return false;
	}
