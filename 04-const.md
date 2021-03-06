# Const Variables

Const is a block scoped variable which maintains constant values. Const cannot be updated or re-declared.

``` JavaScript 
const meganFullName = "Hi, I'm Megan Jovon Ruth Pete."
meganFullName = "Hi, I'm Jovon." // error: Identifier 'megan' has already been declared
```
Again, `const` variables cannot be updated or redeclared. Every const declaration must be initialized at the time of declaration.

While  `const` can’t be updated or re-declared, the properties of this object can be updated or mutated. 

<strong>For example:</strong>

```JavaScript
const theeStallionProfile = {
  name: "Megan Jovon Ruth Pete",
  rapName: "Megan Thee Stallion",
  alias: "The Hot Girl Coach",
  situationShip: "MoneyBagYo",
  pets: {
    name: "4oe",
    breed: "French Bulldog"
  }
}

theStallionProfile.situationShip = "Trey Songz";
```

In this example, Megan Thee Stallion’s profile shares some industry knowledge about her life. As a person, Megan Thee Stallion always expresses her relationship status as single; however, she has situations. In her [NPR debut](https://www.npr.org/2019/12/02/782026665/megan-thee-stallion-tiny-desk-concert), her newly released song "Fkn Around" discussed the following: “Everyone wants to know who Megan’s dating, but that depends on whatever the day is.” She has situations in different time zones, area codes, and weekdays so it really depends. What remains <strong>constant</strong> is Megan will have situations and interested men have to be okay with that. So back to JavaScript, as a `const` variable, Megan will remain the fluid individual she is. That stance on her profile will never change. However, her properties can definitely change (MoneyBagYo, Trey Songz, European Papi out in Italy, Man in Texas, West Coast Thang, and etc.)
