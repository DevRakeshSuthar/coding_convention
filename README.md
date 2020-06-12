# coding_convention

- Magic Number

      // Magic numbers

      const SECONDS_IN_A_DAY = 86400;

      for (var i = 0; i < SECONDS_IN_A_DAY; i++){
        // .....
      }
      
- Deep Nesting

      
      const aArray = [ [ [ 'value'] ] ];

         aArray.forEach((array1) => {
           array1.forEach( (array2) =>{
              array2.forEach( el => {
               console.log(el)
           })
           })
         })

                or

      const retrieveValue = (elem) => {
        if (Array.isArray(elem)){
          return retrieveValue(elem[0])
        }
        return elem 
      }

      retrieveValue(aArray)

- Stop Writting Commments too much - code must speak itself !

- Avoid Large Functions

      const addMulSub = ( a,b,c ) => {
        const addition = a+b+c
        const subtraction = a-b-c
        const multiplication = a*b*c

        return `${addition} ${subtraction}  ${multiplication}`
      } 

      const add = (a,b,c) => a+b+c
      const sub = (a,b,c) => a-b-c
      const mul = (a,b,c) => a*b*c
      
- Code repetition
