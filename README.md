Kebab O'Clock - Menu Management Guide
This guide provides instructions on how to manage the menu items for the Kebab O'Clock website by editing the associated JSON files.

1. Menu Data Structure
The menu items are organized into several JSON files, each representing a category. These files are loaded dynamically by the website to display the menu.

List of JSON Files:

beefy-tastic.json
chicken-menu.json
wrap-tastic.json
don-shawarma.json
grilled-tastic.json
wings-tenders.json
veggie-tastic.json
drinks-milkshakes.json
addons-sauces.json
loaded-fries.json
Important: All JSON files must be located in the same directory as index_fixed_dm.html.

2. Understanding a Menu Item JSON Object
Each menu item is represented by a JSON object with specific properties. Below is an example of a menu item and a detailed explanation of each field:
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

Field Explanations:
name

Description: The primary name of the menu item as displayed on the website.
Type: String
Example: "Chicken Tenders or Wings"
description

Description: A brief, descriptive text that appears under the item's name.
Type: String
Example: "Chicken wings or tenders with any 1 sauce"
image

Description: The filename of the image associated with the menu item. This image should be located in the same directory as the HTML file.
Type: String
Example: "Chicken Tenders or Wings.jpg"
tags

Description: An array of strings used for categorization and filtering.
The first tag in the array is typically displayed as a badge on the menu card.
Keywords or categories (e.g., "Wings/tenders", "chicken") help users find items through search and filters.
Special tags D or M are used to modify image sizing for specific item types:
D: For Drinks, adjusts image positioning to fit the box.
M: For Milkshakes, ensures the full image fits within the container (object-fit: contain).
Type: Array of Strings
Example: ["Wings/tenders", "chicken", "D"]
mealPriceModifier

Description: The additional cost applied to the base price when a customer opts for the "Chips and Drink" meal option.
Type: Number (decimal)
Example: 2.50
options

Description: (Optional) An array of objects defining different sizes, types, or variations of the menu item, each with its own name and price. If an item has no variations, this field can be omitted.
Type: Array of Objects
Structure of each option object:
name: The text displayed in the dropdown menu for this option.
price: The price for this specific option.
Example:
"options": [
  {"name": "5 piece", "price": 5.00},
  {"name": "10 piece", "price": 9.00},
  {"name": "15 piece", "price": 14.00},
  {"name": "20 piece", "price": 18.00}
]

showSlider

Description: This field MUST always be set to false. It is a legacy property and does not affect current functionality.
Type: Boolean
Example: false
sauces

Description: A boolean indicating whether the item allows customers to select a sauce (or dip/flavour, depending on the category). If true, a dropdown for sauce selection will appear in the item modal.
Type: Boolean
Example: true
vegetables

Description: A boolean indicating whether the item includes or allows customers to select vegetable options. If true, a multiple-choice section for vegetables will appear in the item modal.
Type: Boolean
Example: false
