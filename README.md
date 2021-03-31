# Vite-TailwindJIT-Issue
Reproduction of the issue of `vite build` hanging when a custom mode is used on an application using TailwindCSS' new JIT compiler.

## Steps to Reproduce

1) In this repo are two base directories, `JIT` and `regular`.
    * `JIT` houses a Vite initiated application that has only installed and set-up TailwindCSS with their new JIT compiler.
    * `regular` house a Vite initiated application that has only installed and set-up TailwindCSS with their base compiler.

2. In both applications, you can run `npm run build` and `npm run build:custom`.
    * `npm run build` - Will run the base `vite build` with no additional options.
    * `npm run build:custom` - Will run `vite build --mode custom` to override the default mode.

3. What you will see is that both the `JIT` and `regular` applications will successfully run the `npm run build` command without issue. However, where as `regular` will also successfully run `npm run build:custom`, the `JIT` application will hang after it lists the bundled files.
