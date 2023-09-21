# weather-program
>> Hello, this is my first upload to github! If i'm doing this all wrong i'm sure i'll get this right later 

>> I want to make a simple weather program using case switches which refer to a certain number of degrees with a line at the bottom that fuses the temperature into a sentence about the weather condition. My hope was to write a program connected to this one in which this program assists in closet organzation, organizing the clothes one wears according to the weather so it's easier to know what to wear.

>> I use case switches for the hot and cold temperatures from 20 to 90 degrees...
>> line 18 starts with the heat
>> line 42 starts with the cold
>> at line 69 I use an array to combine the case switches of the functions at 18 & 42
>> and at line 111 I assemble the weather conditions (with more switches)
>> line 148 is where I would like the line to print out a temperature with its condition ( i have a randomizer on the side in hopes I could print random weather conditions and get different results)

More info at the bottom >> line 151

// which top should I wear to keep me cool when I go outside?
function itsHot(szl) {

let top = "";
switch (szl) {
  case 1:
    top = "shirt";
    console.log("Sixty degree weather means you will probably want to dress fashionably warm.");
    break;
  case 2:
    top = "hoodie";
    console.log("In seventy degree weather a hoodie is light and casual! If not a hoodie, what would you like to wear?");
    break;
  case 3:
    top = "jacket";
    console.log("Feel free to show some skin if you are so inclined. It is beautiful outside.");
    break;
  case 4:
    top = "coat";
    console.log("You only really need a shirt in this kind of weather unless you have business to dress for.");
    break;
}
}

itsHot();

// which top should I wear to keep me warm when I go outside?
function itsCold(brr) {

let top = "";
switch (brr) {
  case 1:
    top = "shirt";
    console.log("Is it twenty degree weather? Wear at least three layers of clothing with some gloves to keep you warm!");
    break;
  case 2:
    top = "hoodie";
    console.log("Around thirty degrees? Wear enough layers of clothing to keep you from feeling chilly!");
    break;
  case 3:
    top = "jacket";
    console.log("You can get away with a few layers with a thick coat in fourty degree weather!");
    break;
  case 4:
    top = "coat";
    console.log("In fifty degree weather a light coat or jacket will be enough!");
    break;
}
}


itsCold();

// What is the weather like outside?
function theWeather(morningWalk) {
  
let theJourney = [20, 30, 40, 50, 60, 70, 80, 90];  
switch (morningWalk) {
  case 1:
      theJourney = [0]; 
    itsCold(1);
    break;
  case 2:
     theJourney = [1];
    itsCold(2);
    break;
  case 3:
    theJourney = [2];
    itsCold(3);
    break;
  case 4:
    theJourney = [3];
    itsCold(4);
    break;
  case 5:
    theJourney = [4];
    itsHot(1);
    break;
  case 6:
    theJourney = [5];
    itsHot(2);
    break;
  case 7:
    theJourney = [6];
    itsHot(3);
    break;  
  case 8:
    theJourney = [7];
    itsHot(4);
    break; 
    
  
  }  
}

// Do we have inclement weather?
function weatherConditions(theSkies) {
  
  let weatherType = "";
  switch (theSkies) {  
    case 1: 
     weatherType = "Rain";
      console.log(" And please remember to take an umbrella with you, it is raining.");
     break;
    case 2:
      weatherType = "Snow";
      console.log(" Be careful as you walk today as it is snowing. Would you like an umbrella?");
      break;
    case 3:
      weatherType = "Sleet";
      console.log(" The floor will be wet and icy because of sleet. Consider taking an extra pair of shoes on your travels today.");
      break;
    case 4:
      weatherType = "Humid";
       console.log(" It is quite hot and humid outside. Help yourself to an extra bottle of water in case you need something to drink.");
      break;  
    case 5:
      weatherType = "Windy";
       console.log("Secure your belongings and tighten your clothing! It may be blown away.");
      break;
    case 6:
      weatherType = "Fog";
       console.log("You may experience limited visibility on your travels today. Please be vigilant.");
      break;
        case 7:
	    weatherType = "Clear";
	     console.log("There are currently no weather conditions to report."
	    break;
  } 
}

weatherConditions();

console.log(theWeather(8) + weatherConditions(1));  This line returns "You only really need a shirt in this kind of weather unless you have business to dress for." " And please remember to take an umbrella with you, it is raining."


my logic was that if I use case switches and arrays I should be able to use numbers that report strings of sentences back to me, and if I needed to edit or add anything I could just edit the information within the function rather than the sentences. But what has been happening recently is I return "NaN" along with the console.log report at the end of the test, so as far as I know the beginning stages of this program works, but I can't seem to find what the problem is with the NaN problem. Testing using isNaN and Number.isNaN seems like a solution but consideing I'm fusing cases with strings, the question is "with which values?"  I test using codepen.io by the way

THank you

personal random digital scribbles below
// this is the key to this program
theWeather(); 
// this is the key to this program

// variables:
top
theJourney 
weatherType
//
 
// functions:
itsCold (top) 
itsHot (top)
theWeather (theJourney)
weatherConditions (weatherType)
//
