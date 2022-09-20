function countCovidStatus(covidStatusArray) {

  let resurt = {

    'negative and low risk':null,

    'positive':null,

    'negative and high risk':null

  }

  const propertyNames = Object.keys(resurt);

  if(covidStatusArray == null || undefined){

    return undefined

  }

  else{

    covidStatusArray.forEach(item => {

      

      if (item === propertyNames[0]){

        resurt['negative and low risk']++;

      }

      else if (item === propertyNames[1]){

        resurt['positive']++;

      }

      else if (item === propertyNames[2]){

        resurt['negative and high risk']++;

      }

    });

  }

Object.keys(resurt).forEach(key=> {

 if ( resurt[key] == null){

      delete resurt[key]

 }

});

  return resurt;

}

// let demo =  countCovidStatus(['positive', 'negative and low risk', 'positive']) ;

// console.log(demo);
