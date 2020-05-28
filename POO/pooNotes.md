    class Person{
      constructor(name, age){
        this.name = name;
        this.edad = age;
      }
      greet(){
        return `Hola mi nombre es ${this.name}`;
      }
    }
    
    const John = new Person('Jonathan Sosa', 29);
    const Eli = new Person('Elizabeth', 28);
    
    console.log(John.greet());
    console.log(John.edad);
    
    
    
    
    class Godin extends Person{
      goToWork(){
        return true;
      }
    }
    
    const Laura = new Godin('Laura', 32);
    console.log(Laura.edad);
    console.log(Laura.goToWork());
    
    
    
    
    \*
    class Godin extends Person{
      constructor(name, age, company){
        //super es usado para no sobreescribir el constructor.
        super(name, age);
        this.company = company;
      }
    }
    goToWork(){
      return this.company;
    }
    *\

