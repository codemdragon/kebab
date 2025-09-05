This is a guide to using this website
You can edit of the JSONS to add or remove items to the menu

const jsonFiles = [
    "beefy-tastic.json",
    "chicken-menu.json",
    "wrap-tastic.json",
    "don-shawarma.json",
    "grilled-tastic.json",
    "wings-tenders.json",
    "veggie-tastic.json",
    "drinks-milkshakes.json",
    "addons-sauces.json",
    "loaded-fries.json"
];


Now ill cover how the JSONS work Your JSON will look something like this

{
  "name": "Chicken Tenders or Wings",
  "description": "Chicken wings or tenders with any 1 sauce",
  "image": "Chicken Tenders or Wings.jpg",
  "tags": ["Wings/tenders", "chicken","D"],
  "mealPriceModifier": 2.50,
  "options": [
    {"name": "5 piece", "price": 5.00},
    {"name": "10 piece", "price": 9.00},
    {"name": "15 piece", "price": 14.00},
    {"name": "20 piece", "price": 18.00}
  ],
  "showSlider": false,
  "sauces": true,
  "vegetables": false
}

Name: being the name of the item

Description: The short description that comes under it

Image: The name of the image in the folder

tags: This will include what it actually is in this example a "Wings/tenders"
        It will include Keywords or categories associated with the item
        It CAN include either D or M
                      D being for Drinks to modify the image sizing to fit the box
                      and the same for M
mealPriceModifier: This is the price modifier you add when you add chips and drinks(what you add to the base price)
Options: This is OPTIONAL and is there when there is a drop down for Sizes costing various prices, This can also include types
          The fields within it are "name": Which will have the text in the dropdown
                                   "price": Which will have the price for the size
                                   
  "options": [
    {"name": "5 piece", "price": 5.00},
    {"name": "10 piece", "price": 9.00},
    {"name": "15 piece", "price": 14.00},
    {"name": "20 piece", "price": 18.00}
  ],

showslider: THIS MUST ALWAYS BE FALSE

sauces: (True/False) Indicates if the item allows sauce selection(Drop down). The  Sauces include Dips and Flavours
vegetables: (True/Fasle) Indicates if the item includes or allows vegetable options(Multiple choice) 
