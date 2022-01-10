package consolePurpose;

public class Test
{

	public static void main(String[] args) 
	{
		
		System.out.println("Test Console ");
		Singleton s1 = Singleton.getInstance();
		System.out.println("One : "+s1);
		
		Singleton s2 = Singleton.getInstance();
		System.out.println("Two : "+s2);
		
		Singleton s3 = Singleton.getInstance();
		System.out.println("Two : "+s3);
		
		if(s1 == s2 && s2 == s3)
		{
			System.out.println("SingleTon Object");
		}
		else
		{
			System.err.println("Not SingleTon Object");
		}
	}
}

class Singleton
{
	private static Singleton singleton_object;
	
	public Singleton() {
		System.out.println("Already Objected Created");
	}
	
	public static Singleton getInstance()
	{
		if(singleton_object == null)
		{
			singleton_object = new Singleton();
		}
		return singleton_object;
		
	}
}

-----------------------------------------------------------------------------------------------------------------
                                                    OUTPUT

Test Console 
Already Objected Created
One : consolePurpose.Singleton@ea30797
Two : consolePurpose.Singleton@ea30797
Two : consolePurpose.Singleton@ea30797
SingleTon Object
                                                    
