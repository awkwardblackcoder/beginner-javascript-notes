# Const Variables

Const is a blocked scope variable which maintains constant values. Const cannot be updated or re-declared.

``` JavaScript 
const meganOnStage = "Hi, I'm Megan Thee Stallion."
meganOnStage = "Hi, I'm Jovon Ruth Pete." // error: Identifier 'megan' has already been declared
```
Again, `const` variables cannot be updated or redeclared. Every const declaration must be initialized at the time of declaration.

While  `const` can’t be updated or re-declared, the properties of this object can be updated or mutated. 

<strong>For example:</strong>

```JavaScript
const theeStallionProfile = {
  name: "Megan Pette",
  stageName: "Megan Thee Stallion",
  situationShip: "MoneyBagYo",
  pets: {
    name: "4oe",
    breed: "French Bulldog"
  }
}

theStallionProfile.situationShip = "Trey Songz"
```

In this example, Megan Thee Stallion’s Profile shares some industry knowledge about her life. As a person, Megan Thee Stallion always expresses her relationship status as single; however, she has situations. In her NPR debut, her newly released song discussed the following: “Everyone wants to know who Megan’s dating, but that depends on whatever the day is.” She has situations in different time zones, area codes, and weekdays so it really depends. What remains <strong>constant</strong> is Megan will have situations and interested men have to be okay with that. So back to JavaScript, as a const variable, Megan will remain the fluid individual she is. That stance on her profile will never change. However, her properties can definitely change (MoneyBagYo, Trey Songz, European Papi out in Italy, Man in Texas, West Coast Thang, and etc.)
