# Vue JSON To Table Parser

A Vue component that renders JSON data in Table structure.

Installation:

```
npm install vue-json-to-table
```

Declare and Add:

```
Open `main.js` and add the following:

import VueJsonToTable from 'vue-json-to-table'
Vue.use(VueJsonToTable)
```


How to use:

```
Add the following in that component where you want to use
<vue-json-to-table :data="jsonDataArr"></vue-json-to-table>
```

<p align="center">
  <img src="https://github.com/shashankgaurav17/vue-json-to-table-parser/raw/master/static/component.png" width="600">
</p>
<br>

Sample JSON Data

```

{
  "show": "Rick and Morty",
  "name": "Rick Sanchez",
  "associates_of_rick": ["Mr. Poopybutthole", "Scary Terry", "Mr. Meeseeks", "Noob Noob"],
  "best_friend": "Birdperson",
  "family_member": {
    "daughter": "Beth",
    "son_in_law": "Jerry Smith",
    "grand_son": "Morty",
    "grand_daughter": "Summer"
  },
  "awards_list": [
    {
      "year": "2014",
      "name": "BTVA Voice Acting Awards"
    },
    {
      "year": "2015",
      "name": "IGN Awards"
    },
    {
      "year": "2017",
      "name": "Golden Reel Awards"
    },
    {
      "2017": [
        {
          "category": "TV Series of the Year",
          "result": "WON"
        },
        {
          "category": "Best TV Episode",
          "result": "LOST"
        },
        {
          "category": "Best Comedic TV Performance",
          "result": "WON"
        }
      ]
    }
  ]
}

```


