<div align="center">

## One Line Bubble Sort


</div>

### Description

This is the bubble sort in one line. 	what allows you to do this is that c++ allows you to use more than one counter in its 'for' loop, by having i and x counters going through the array at the same time we can have x go through the whole array before i increments	by restricting i until x has finished looking through the array The other aspect that is smaller is the exchanging of values, normally you would set up a temp value and hold one of the values in that temp variable, then copy the second value to the first and finally copy the temp variable to the second value, an easy way to exchange two values is to XOR the values 3 times, this is why it works:

Values (5 and 10)

In binary they are 0101 and 1010, to switch we xor them 3 times:

*remember ^= in c++ = XOR and i^=x stores the return value in i, x remains unchanged*

0101	i= 0101, x = 1010 here

XOR	1010	xor them together

=	1111	then you get 1111 in i, x is still 1010

1010	now xor x and i storing new val in x

XOR	1111	-this is i

=	0101	then x = 0101 (5), i still = 1111 (15)

1111	now xor i against x one more time

XOR	0101	-this is x it still = 5 since we are xoring i with x, i will change only

=	1010	-now i = 1010 (10)

-now i = 10 and x = 5 they are switched
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[PlanetCPP\-Chris\(Hound\)/Micheal\(xix\)](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/planetcpp-chris-hound-micheal-xix.md)
**Level**          |Intermediate
**User Rating**    |3.8 (15 globes from 4 users)
**Compatibility**  |C\+\+ \(general\), Microsoft Visual C\+\+, Borland C\+\+
**Category**       |[Algorithms](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/algorithms__3-29.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/planetcpp-chris-hound-micheal-xix-one-line-bubble-sort__3-2795/archive/master.zip)





### Source Code

```
/*
	One line bubble sort
	www.PlanetCPP.com
*/
#include <iostream>
using std::cout;
using std::endl;
using std::cin;
int main()
{
  	int i,x,arraysize=0,tmp=0;
  	int arry[50]={0};	//initiate array of 50 integers
  	cout<<"Enter in integer values, use negative # to stop\n";
  	cin>>tmp;
  	while(tmp>=0)	//loop till # is negative
    	{
    		arry[arraysize]=tmp;
    		arraysize+=1;	//increment counter
    		cin>>tmp;
    }
    	//start bubble sort code
    	for(i=0,x=1;i<arraysize,x<arraysize;i++,x++){if(arry[i]>arry[x]){arry[x]^=arry[i];arry[i]^=arry[x];arry[x]^=arry[i];}if(x<(arraysize-1)){i--;}else{x=i+1;}}
    	//end bubble sort code
    	for(i=0;i<arraysize;i++)	//show array after sorted
    		cout<<arry[i]<<endl;
	return 0;
}
  /*
  	what allows you to do this is that c++ allows you to
  	use more than one counter in its 'for' loop, by having
  	i and x counters going through the array at the same time
  	we can have x go through the whole array before i increments
  	by restricting i until x has finished looking through the array
  	The other aspect that is smaller is the exchanging of values,
  	normally you would set up a temp value and hold one of the values
  	in that temp variable, then copy the second value to the first and
  	finally copy the tempo variable to the second value, an easy way to
  	exchange two values is to XOR the values 3 times, this is why it works:
  	Values (5 and 10)
  	In binary they are 0101 and 1010, to switch we xor them 3 times:
  	*remember ^= in c++ = XOR and i^=x stors the return value in i x
  	remains unchanged*
  		0101	i= 0101, x = 1010 here
  	XOR	1010	xor them together
  	=	1111	then you get 1111 in i, x is still 1010
  		1010	now xor x and i storing new val in x
  	XOR	1111	-this is i
  	=	0101	then x = 0101 (5), i still = 1111 (15)
  		1111	now xor i against x one more time
  	XOR	0101	-this is x it still = 5 since we are xoring i with x, i will change only
  	=	1010	-now i = 1010 (10)
  				-now i = 10 and x = 5 they are switched
  */
```

