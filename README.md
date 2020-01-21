# This is the h1 
## This is the h2
### this is the h3

---








1. Server 

```java
import java.util.*;
import java.net.*;
import java.io.*;
class Server 
{
	public static void main(String[] ar) throws Exception
	{
		ServerSocket ss=new ServerSocket(5555);
		Socket s=ss.accept();
		System.out.println("Connected...");
		InputStream is=s.getInputStream();
		DataInputStream dis=new DataInputStream(is);
		int num=Integer.parseInt(dis.readUTF());
		System.out.println("akdfjksd");
		
		int fact=1;
		for(int i=num;i>1;i--)
			fact*=i;
		
		OutputStream os=s.getOutputStream();
		DataOutputStream dos=new DataOutputStream(os);
		dos.writeUTF(fact+"");
		dos.close();
	}		
}

```


2. Sample

```java
import java.util.Arrays;
class ThirdProgram{
	public static void main(String[] args) {
		String s="ssspppqqqqabcdefabcde";
		char array[]=s.toCharArray();

		char least=' ';

		int count=0;
		int previous=0;


		for (char c : array) {
			for(int i=0;i<array.length;i++){
				if(c==array[i]){
					count+=1;
				}
			}


				if(count<previous){
					least=c;
			}
			count=0;
	}



		System.out.println("*^^^^^^^^^^^^^^^^^*");
		System.out.println(least);
		System.out.println("*^^^^^^^^^^^^^^^^^*");



	}
}
```