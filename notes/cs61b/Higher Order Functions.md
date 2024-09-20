````python
def tenX(x):
   return 10*x
   
def do_twice(x):
	return f(f(x))
print(do_twice(tenx, 2))        
````

````java
public class HoFDemo {
   public static int do_twice(IntUnaryFunction f, int x){
       return f.apply(f.apply(x));
   }

    public static void main(String[] args) {
        System.out.println(do_twice(new Tenx(), 2));
    }
}
class Tenx implements IntUnaryFunction{
    @Override
    public int apply(int x) {
        return 10* x;
    }
}
interface IntUnaryFunction{
    int apply(int x);
}
````

