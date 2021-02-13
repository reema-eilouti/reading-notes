# Class 07 Reading Notes

## HTML Tables and JS Constructor Functions

### HTML Tables

- The `<table>` element is used to add tables to a web page.
- A table is drawn out row by row. Each row is created with the `<tr>` element.
- Inside each row there are a number of cells represented by the `<td>` element *(or `<th>` if it is a header)*.
- You can make cells of a table span more than one row or column using the **rowspan** and **colspan** attributes.
- For long tables you can split the table into a `<thead>`, `<tbody>`, and `<tfoot>`.


### JavaScript Object Constructors

- It is considered good practice to name **constructor functions** with an upper-case first letter.
```
function Person(first, last, age, eye) {
  this.firstName = first;
  this.lastName = last;
  this.age = age;
  this.eyeColor = eye;
}
```
- Objects of the same type are created by calling the constructor function with the **new** keyword:
```
let myFather = new Person("John", "Doe", 50, "blue");
let myMother = new Person("Sally", "Rally", 48, "green");
```
- Adding a Property to an Object:
```
myFather.nationality = "English";
```
- Adding a Method to an Object:
```
myFather.name = function () {
  return this.firstName + " " + this.lastName;
};
```



##### [Go Back](code_201_reading_notes.md)