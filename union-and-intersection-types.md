# Practical Example of Combining Union and Intersection Types in TypeScript

Union and intersection types are really good tools in TypeScript that help us to handle different kinds of data. When we are learning these types looks bit confusing at first but they become easy when we try them out. A union type lets a value be one of several types using the pipe symbol, while an intersection type combines multiple types into one using the ampersand symbol.

we can look at a example where we want to combine user roles and permissions. Suppose we have an Admin type and a User type, and we want to mix them together. By using an intersection type we can make sure an object has all the properties from both types at the same time. On the other hand a union type lets a variable accept either a string or a number depending on what the user types.

code example :
type Admin = {
name: string;
adminLevel: number;
};

type Employee = {
employeeId: string;
department: string;
};

type SuperEmployee = Admin & Employee;

type Identifier = string | number;

function processEmployee(emp: SuperEmployee, id: Identifier): string {
return "Processing ID: " + id + " for employee: " + emp.name;
}
