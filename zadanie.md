package com.company;

public class Main {
    public Main() {
    }

    public static void main(String[] args) {
        int[] A = new int[]{150, 122, 66, 11,1, 8, 5, 7, 8, 55, 200, 77, 95, 123, 6, 35};
        int liczba = A.length;
        int z1 = A[0];
        int z2 = A[0];
        int z3 = A[0];
        int index = 0;
        int index2 = 0;
        int index3 = 0;
        for(int i=0; i<liczba; i++) {
            if(A[i]<z3&&A[i]>=z2)
            {
                z3=A[i];
                index3 = i;
            }
            if(A[i]<z2&&A[i]>=z1)
            {
                z3=z2;
                index3=index2;
                z2=A[i];
                index2 = i;
            }
            if (A[i]<z1){
                z3=z2;
                index3=index2;
                z2=z1;
                index2=index;
                z1=A[i];
                index=i;
            }
        }
        System.out.println("Pierwsza najmniejsza liczba to " +z1 +" znajdująca się pod indeksem "+index);
        System.out.println("Druga najmniejsza liczba to " +z2 +" znajdująca się pod indeksem "+index2);
        System.out.println("Trzecia najmniejsza liczba to " +z3 +" znajdująca się pod indeksem "+index3);

    }
}
