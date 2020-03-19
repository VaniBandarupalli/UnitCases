# UnitCases
package Unit.Testcases;
import static org.junit.Assert.*;
import org.junit.Test;
import org.junit.Before;
//import org.junit.Test;
public class AppTest
{
	App pro;
	@Before
	public void Demo()
	{
		pro=new App();
	}
	@Test
	public void fstAlpha()
	{
		assertEquals("BCD",pro.remove("ABCD"));
	}
	@Test
	public void fstTwoAlpha()
	{
		assertEquals("CD",pro.remove("AACD"));
	}
	@Test
	public void secAlpha()
	{
		assertEquals("BCD",pro.remove("BACD"));
	}
	@Test
	public void noAlpha()
	{
		assertEquals("BBAA",pro.remove("BBAA"));
	}
	@Test
	public void nextAlpha()
	{
		assertEquals("BAA",pro.remove("AABAA"));
	}
}
