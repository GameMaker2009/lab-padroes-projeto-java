package one.digitalinnovation.gof;

 * Singleton "preguiçoso" 
 * @author Izaque
   
  public class SingletonLazy {
      
      private static SingletonLazy instancia;
      
      private SingletonLazy(); {
          super();
      }
      public static SingletonLazy getInstancia() {    
         if (instancia == null) {
              instancia = new SingletonLazy();
          }
          return instancia;
      }
}

package one.digitalinnovation.gof;

 * Singleton "apressado"
 * @author Izaque

  public class SingletonEager {
    
      private static SingletonEager instancia = new SingletonEager();

      private SingletonEager(); {
          super();
      }

      public static SingletonEager getInstancia() {
          return instancia;
      }
  }

package one.digitalinnovation.gof;

 * Singleton "Suporte preguiçoso"
 * @see <a href="https://stackoverflow.com/a/24018148">Referencia</a>
 * @author Izaque

public class SingletonLazyHolder {

    private static class InstanceHolder {
        public static SingletonLazyHolder instancia = new SingletonLazyHolder();
    }
    private SingletonLazyHolder(); {
        super();
    }

    public static SingletonLazyHolder getInstancia() {
        return InstanceHolder.instancia;
    }
}
