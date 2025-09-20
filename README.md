# baldrick-tsconfig-es2024

> Shared basic [TypeScript config](https://www.typescriptlang.org/docs/handbook/tsconfig-json.html) for ES2024

This is _not an official_ [base](https://github.com/tsconfig/bases). It should support Node.js 22 and above, but should provide ES2024 support for [ES modules](https://hacks.mozilla.org/2018/03/es-modules-a-cartoon-deep-dive/).

It includes:

-   `allowSyntheticDefaultImports` is activated (true) to provide backwards compatibility, Node.js allows you to import most CommonJS packages with a default import. This flag tells TypeScript that it's okay to use import on CommonJS modules (Sindre Sorhus)
-   `declaration` is activated (true) and generate .d.ts files for every TypeScript or JavaScript file inside your project. 
-   `esModuleInterop` is activated (true) which should result in better support for import of dependencies regardless whether they are `ES` or `commonjs`.
-   `forceConsistentCasingInFileNames` is activated (true) and TypeScript will issue an error if a program tries to include a file by a casing different from the casing on disk.
-   `moduleDetection` is set to `force` which ensures that every non-declaration file is treated as a module. 
-   `newLine` is set to `LF` (unix).
-   `noEmitOnError` is activated (true) and this will not emit compiler output files like JavaScript source code, source-maps or declarations if any errors were reported.
-   `noFallthroughCasesInSwitch` is activated (true) and you get report errors for fallthrough cases in switch statements.
-   `noImplicitOverride` is activated (true) and you can ensure that the sub-classes never go out of sync, by ensuring that functions which override include the keyword `override`.
-   `noImplicitReturns` is activated (true) and TypeScript will check all code paths in a function to ensure they return a value.
-   `noPropertyAccessFromIndexSignature` is activated (true) and will raise an error when the unknown field uses dot syntax instead of indexed syntax.
-   `noUncheckedIndexedAccess` is activated (true) and this will add undefined to any un-declared field in the type.
-   `noUnusedLocals` is activated (true) and you get report errors on unused local variables.
-   `noUnusedParameters` is activated (true) and you get report errors on unused parameters in functions.
-   `resolveJsonModule` is deactivated (false) as TypeScript does not support resolving JSON files by default.
-   `skipLibCheck` is activated (true) and skip type checking of declaration files.
-   `strict` is activated (true) and enables a wide range of type checking behavior that results in stronger guarantees of program correctness. 
-   `useDefineForClassFields` is activated (true) and switches to the upcoming standard version of class fields runtime behavior.

## Install

    $ npm install --save-dev baldrick-tsconfig-ES2024

## Usage

`tsconfig.json`

```json
{
	"extends": "baldrick-tsconfig-es2024"
}
```

## Other

This project was strongly inspired by [Sindre Sorhus tsconfig](https://github.com/sindresorhus/tsconfig)

```
