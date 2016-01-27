# Ovinger
package encapsulation;

public class Digit {
	
	int base;
	int value;
	
	public Digit(int base) {
		if (base > 0) {
			this.base = base;
		} else {
			throw new IllegalArgumentException("Negative base.");
		}
	}
	
	public int getBase() {
		return base;
	}

	public void setBase(int base) {
		this.base = base;
	}

	public int getValue() {
		return value;
	}

	public void setValue(int value) {
		this.value = value;
	}

	public boolean increment() {
		value += 1;
		if (value == base) {
			value = 0;
			return true;
		}
		return false;
	}
	
	public String toString(){
		return String.valueOf("0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ".charAt(value));
	}
}
