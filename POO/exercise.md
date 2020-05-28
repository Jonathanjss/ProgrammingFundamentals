    class Chocolate{
      constructor(brand, color, flavor, cacaoPorcen, temperature, grWeight){
        this.brand = brand;
        this.color = color;
        this.flavor = flavor;
        this.cacaoPorcen = cacaoPorcen;
        this.temperature = temperature;
        this.grWeight = grWeight;
      }
    
      calcGrames(){
        return this.grWeight * 50;
      }
      calcState(){
        if(this.temperature < 30){
          return "Your chocolate is solid."
        }else if( this.temperature >= 30 && this.temperature < 45){
          return "Your chocolate is liquid.";
        }else{
          return "Time to put your chocolate into your fridge.";
        }
      }  
    };
    
    class Seasons extends Chocolate{
      constructor(brand, color, flavor, cacaoPorcen, temperature, grWeight, chocSeason){
        super(brand, color, flavor, cacaoPorcen, temperature, grWeight);
        this.chocSeason = chocSeason;
      }
    
      sellFast(){
        switch(true){
          case (this.chocSeason.toLowerCase() === "spring"):
            return 'Chocolate doesn\'t sell much this season.';
          case (this.chocSeason.toLowerCase() === "summer"):
            return 'Nobody drinks chocolate in summer.';
          case (this.chocSeason.toLowerCase() === "outum"):
            return 'Time to start buying chocolate.';
          case (this.chocSeason.toLowerCase() === "winter"):
            return 'Chocolate sells a lot this season.';
        }
      }
    }
    
    const hersheyChoc = new Chocolate('Hershey\'s', 'dark', 'bitter', 80, 27, 25);
    
    console.log(hersheyChoc.brand);
    console.log(hersheyChoc.calcGrames());
    console.log(hersheyChoc.calcState());
    
    
    const abuelitaChoc = new Seasons('Nestle', 'dark', 'bitter', 90, 25, 90, 'Winter');
    console.log(abuelitaChoc.brand);
    console.log(abuelitaChoc.chocSeason.toLowerCase());
    console.log(abuelitaChoc.sellFast());

[https://jsfiddle.net/JonathanSosa/7k45opgc/2/](https://jsfiddle.net/JonathanSosa/7k45opgc/2/)


    class Toy{
      constructor (name, price, brand){
        this.name = name;
        this.price = price;
        this.brand = brand;
      }
    }
    
    const toy1 = new Toy('The Eiffel Tower', 2500, 'Lego');
    console.log(toy1.name);
    console.log(toy1.price);
    console.log(toy1.brand);
    
    class sportArticles extends Toy{
      constructor(name, price, brand, sport){
        super(name, price, brand);
        this.sport = sport;
      }
    }
    
    const sportArticle1 = new sportArticles('Racker', 400, 'Wilson', 'Tennis');
    console.log(sportArticle1.sport);
    
    class Cars extends Toy{
      constructor(name, price, brand, year){
        super(name, price, brand);
        this.year = year;
      }
    }
    
    const car1 = new Cars("Carrera GT", 2000000, "Porsche", 2015);
    console.log(car1.price);

[https://jsfiddle.net/JonathanSosa/tn6j5o02/](https://jsfiddle.net/JonathanSosa/tn6j5o02/)
