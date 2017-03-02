Guideline for writing good code

1.Write a javadoc

 ->Write a java doc every method for understand what is the code work.

2.Write TODO Comment.

 ->Write the TODO comment explains why the function has a degenerate implementation
and what that function’s future should be.

3.Don't write a Bad Comment.

 ->Don't write a comment that the code already showed.It's waste some lines of code. 

4.Write UML before code.

 ->UML will make you see overall promgram, it make codeing easier.

5.Use Singleton pattern.

 ->Encapsulation will make each class in program not confuse. [Link](https://8thlight.com/blog/uncle-bob/2015/06/30/the-little-singleton.html)

 ->Use getters/setters in other class for get the value or set the value	
	
	public double getValue() {
		return this.value;
	}
	public String getCurrency() {
		return this.currency;
	}
	
6.Don't Repeat your code


	```public abstract class AbstractValuable implements Valuable {
	/** Value of the money. */
	private double value;
	/** The currency of money. */
	private String currency;
	...
	public double getValue() {
		return this.value;
	}

	public String getCurrency() {
		return this.currency;
	}
	}```



	```public class Coin extends AbstractValuable {
	public static final String DEFAULT_CURRENCY = "Baht";
	/** Value of the coin. */
	private double value;
	/** The currency of coin. */
	private String currency;

	...
	public double getValue() {
		return this.value;
	}

	public String getCurrency() {
		return this.currency;
	}
	}```

	 -> In the Coin class has extend the AbstractValuable class, and the AbstractValuable class already have getValue() method and getCurrency() method. So Don't write its twice in the Coin class.

