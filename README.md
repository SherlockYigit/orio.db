# Orio.db 
![Download](https://img.shields.io/npm/dt/orio.db.svg?style=flat-square)
![Quality](https://api.codacy.com/project/badge/Grade/9d3535f52e7b4bce8f70c761a27b0602)
[Orio.db](https://github.com/SherlockYigit/orio.db) is an open source project. It means being open source, you can contribute to its development yourself. 
| Documentation | Developer blog |
| :--: | :--: |
| [orio.db-docs](https://sherlockyigit.github.io/orio.db-docs) | *Soon..* |
## Changelog (2.1.3)
* Bugs in `unpush` function have been fixed.

## Examples
### Using with default settings 
```js
let db = require("orio.db");

// You fetch all the data saved in the database.
db.all();
// > [ { ID: key, data: value }, ... ]

// Sets data in created database.
db.set("user", { id: 1 });
// > { id: 1 }

// You fetch if there is data in the database created.
db.get("user");
// > { id: 1 }

// You check if there is data in the database created.
db.has("user");
// > true or false

// You push data to the array in the database created with the key.
db.push("user.ranks", "admin");
// > [ "admin" ]
/* or */
db.push("user.ranks", { rankName: "manager" });
// > [ "admin", { rankName: "manager" }  ]

// You unpush data to the array in the database created with the key.
db.unpush("user.ranks", "admin");
// > [ { rankName: "manager" }  ]
/* or */
db.unpush("user.ranks", { rankName: "manager" });
// > []

// You add number to the created database.
db.add("user.money", 500);
// > 500 

// You subtract number to the created database.
db.substract("user.money", 200);
// > 300

// You delete data from the created database.
db.delete("user"); 
// > true or false

// You delete all the data in the database.
db.deleteAll();
// > true or false
```
### Using with adjustable settings 
```js
let db = require("orio.db");

db.setOptions({
  adapter: "json",
  name: "database",
  path: "oriodb",
  deleteEmptyArray: true
}); // It's enough to use once. 

// You fetch all the data saved in the database.
db.all();
// > [ { ID: key, data: value }, ... ]

// Sets data in created database.
db.set("user", { id: 1 });
// > { id: 1 }

// You fetch if there is data in the database created.
db.get("user");
// > { id: 1 }

// You check if there is data in the database created.
db.has("user");
// > true or false

// You push data to the array in the database created with the key.
db.push("user.ranks", "admin");
// > [ "admin" ]
/* or */
db.push("user.ranks", { rankName: "manager" });
// > [ "admin", { rankName: "manager" }  ]

// You unpush data to the array in the database created with the key.
db.unpush("user.ranks", "admin");
// > [ { rankName: "manager" }  ]
/* or */
db.unpush("user.ranks", { rankName: "manager" });
// > []

// You add number to the created database.
db.add("user.money", 500);
// > 500 

// You subtract number to the created database.
db.substract("user.money", 200);
// > 300

// You delete data from the created database.
db.delete("user"); 
// > true or false

// You delete all the data in the database.
db.deleteAll();
// > true or false
```

## Support Server 
<a href="https://discord.gg/YdHRnsc"><img src="https://invidget.switchblade.xyz/YdHRnsc"></a>
## Sponsor Server
<a href="https://discord.gg/2mbTGR8YrX"><img src="https://invidget.switchblade.xyz/2mbTGR8YrX"></a>