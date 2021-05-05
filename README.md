# findmaximum
package com.bridgelabz.findmaximum;


import java.util.Scanner;

public class FindMaximum <E extends Comparable<E>> {
	private E firstvalue;
	private E secondvalue;
	private E thirdvalue;

	public FindMaximum(E firstvalue, E secondvalue, E thirdvalue) {
		super();
		this.firstvalue = firstvalue;
		this.secondvalue = secondvalue;
		this.thirdvalue = thirdvalue;
	}

	public static void main(String[] args) {
		FindMaximum.findMax(20,5, 10);
		FindMaximum.findMax(20.5f, 15.6f, 18.9f);
		FindMaximum.findMax("Apple", "strawberry", "carrot");
	}

	public static <E extends Comparable<E>> E findMax(E firstvalue, E secondvalue, E thirdvalue) {
		E max = firstvalue;
		if (secondvalue.compareTo(max) > 0) {
			max = secondvalue;
		}
		if (thirdvalue.compareTo(max) > 0) {
			max = thirdvalue;
		}
		printMax(max);
		return max;
	}
	
	public static <E> void printMax(E max)
	{
		System.out.println("Maximum Value is : "+max);
	}
}
