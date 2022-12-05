# bubblesort-ile-küçükten-büyüğe sıralama


#include<stdio.h>
#include<stdlib.h>
int main(void)
{
	int sinir,gecici,j,i;
	int dizi[100];
	printf("girilecek sayi adeti");
	scanf("%d",&sinir);      //kac adet sayi girilecegi hesaplanir
	
	for(i=0;i<sinir;i++)  // kullanicidan sayilar alinir
	{
		printf("%d)sayi giriniz",i+1);
		scanf("%d",&dizi[i]);
		
	}
	//alinan sayilar ekrana yazdirilir
	for(i=0;i<sinir;i++)
	{
		printf("%d ",dizi[i]);
		printf("\n\n");
	
	}
	//bubblesort algoritmasi(kücük büyüge siralama yapar)

	for(i=0;i<sinir;i++)
	
		for(j=0;j<sinir-1-i;j++)
		{
			if(dizi[j]>dizi[j+1])
			{
				gecici=dizi[j];
				dizi[j]=dizi[j+1];
				dizi[j+1]=gecici;
			}
			
		}
	

	//dizinin siralanmis halini ekrana yazdir
	for(i=0;i<sinir;i++)
	{
		printf("%d ",dizi[i]);
		printf("\n");
		
	}
	return 0;
}
