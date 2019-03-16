# Votes-calculation-using-Command-line-interpreter-in-java
public class Ballot
{
	public static void main(String[] args)
	{
		int a[]={1,2,3,4,5};
		int n=args.length;
		int count[]=new int[n];
		int i,j,k1=0,k2=0,k3=0,k4=0,k5=0,s=0;
		for(i=0;i<n;i++)
		{
			count[i]=Integer.parseInt(args[i]);
		}
		System.out.println("The votes count=");
		for(i=0;i<n;i++)
		{
			System.out.print(count[i]+" ");
		}
		System.out.println(" ");
		for(i=0;i<5;i++)
		{
			for(j=0;j<n;j++)
			{
				if(a[i]==count[j])
				{
					if(a[i]==1)
					 k1++;
					else if(a[i]==2)
					 k2++;
					else if(a[i]==3)
					 k3++;
					else if(a[i]==4)
					 k4++;
					else if(a[i]==5)
					 k5++;
				}
			}
		}
		System.out.println("Candidate Name=     1      2      3      4      5"); 
		System.out.println("No.of votes are =   "+k1+"\t"+k2+"\t"+k3+"\t"+k4+"\t"+k5);
		for(i=0;i<n;i++)
		{
			if(count[i]>5)
			s++;
		}
		System.out.println("No.of spoilt votes ="+s);
	}
}
