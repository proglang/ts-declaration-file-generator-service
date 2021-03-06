## Typescript declaration files generator service

### Installation
#### Docker
Install Docker.
https://docs.docker.com/install/

#### Install
Clone this repository and then run:

```shell
./install.sh
```

### Usage
#### Generate a Typescript declaration file from Javascript code


```shell
./bin/run.sh [JS-FILE] [TYPESCRIPT-MODULE-NAME] [OUTPUT_DIRECTORY]
```


#### Example
You can use the example provided in this repo under `example/calculator.js`.

```shell
./bin/run.sh examples/example.js calculator /tmp/ts-declaration-file-generator-service
```

You will find the declaration file under `/tmp/ts-declaration-file/calculator/index.d.ts`:

```shell
cat /tmp/ts-declaration-file-generator-service/calculator/index.d.ts
```

```typescript
export = Calculator;

declare class Calculator {
    constructor();
    sum(a: number, b: number): number;
}

declare namespace Calculator {
}
```