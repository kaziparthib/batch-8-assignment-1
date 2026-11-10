# Understanding TypeScript Compilation and tsconfig.json

When we write TypeScript code browsers cannot read it directly. Browsers only understand normal JavaScript. Because of this we need a compiler. This compiler is called tsc. It helps translate files.

Under the hood, tsc does a lot of work. First it scans all our code. Next it checks for any typing errors. If it finds mistakes, it warns us in the terminal. If everything looks good, it removes all the types. Then it creates clean JavaScript files. This entire process is called transpilation.

The tsconfig.json file is also very important. It acts like a map for the compiler. Inside this file we give instructions to tsc. We can choose which JavaScript version we want to use. We can also turn on strict type checking rules.

code example:
{
"compilerOptions": {
"target": "es2016",
"strict": true
}
}
