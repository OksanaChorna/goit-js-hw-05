# goit-js-hw-05

## task 5_3 Перший варіант

```
class Storage {
constructor(items) {
this.items = items;
}
getItems() {
return this.items;
}
addItem(item) {
return this.items.push(item);
}
removeItem(item) {
const newItems = [];
for (const key of this.items) {
if (key === item) continue;
console.log(key);
newItems.push(key);
}
this.items = newItems;
}
}

const storage = new Storage([
"Нанитоиды",
"Пролонгер",
"Железные жупи",
"Антигравитатор",
]);

const items = storage.getItems();
console.table(items); // [ "Нанитоиды", "Пролонгер", "Железные жупи", "Антигравитатор" ]

storage.addItem("Дроид");
console.table(storage.items); // [ "Нанитоиды", "Пролонгер", "Железные жупи", "Антигравитатор", "Дроид" ]

storage.removeItem("Пролонгер");
console.table(storage.items); // [ "Нанитоиды", "Железные жупи", "Антигравитатор", "Дроид" ]
```

## task 5_4

```

class StringBuilder {
constructor(value) {
this._value = value;
}
get value() {
return this._value;
}
append(str) {
this._value += str;
}
prepend(str) {
this._value = str + this._value;
}
pad(str) {
this._value = str + this._value + str;
}
}
const builder = new StringBuilder(".");

builder.append("^");
console.log(builder.value); // '.^'

builder.prepend("^");
console.log(builder.value); // '^.^'

builder.pad("=");
console.log(builder.value); // '=^.^='

```
