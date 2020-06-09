# ts-tdd

This is the repository of basic skeleton for the start in Typescript.


## Initial setup

### Create new repository

Create a new repository and clone  

```
git clone <git_repo_url>
```

### Initialize npm

Navigate to the repo

```
cd <directory_name>
```

Initialize npm

```
npm init
```

This will generate basic `package.json` file having project basic information

#### Install needed npm modules

Create empty directory and install modules required for running test cases

```
npm install @types/chai @types/mocha chai mocha ts-node typescript --save
```

Following is the description for these packages:


@types/chai: 

@types/mocha

chai:

mocha

ts-node:

typescript:


#### Create basic directories

Create these basic directories for the code and specs

```
src
spec
```

src: Where we'll have our code
spec: Where we'll have our test cases

#### Create test file

Create a file: `spec/first.spec.ts`

Use this code and put in your first spec file:


```
import {expect} from 'chai';

describe('First spec', () => {
  it('passes', () => {
      expect(1).to.equal(1);
  })
});

```

### Create mocha config file

Create file with name `.mocharc.json` in root of directory of your project

```
{
  "diff": true,
  "extension": ["ts"],
  "require": ["ts-node/register"],
  "package": "./package.json",
  "reporter": "spec",
  "slow": 75,
  "timeout": 2000,
  "ui": "bdd",
  "watch-files": ["**/*.ts"],
  "watch-ignore": ["node_modules"],
  "spec": "**/*.spec.ts"
}

```


### Run your first test

Make sure we have this command in the `package.json`

```
"test": "mocha"
```

Then run following command in the terminal:

```
npm test
```

You will see following output then you are all set.

```
> ts-tdd@1.0.0 test <your-project-directory-path>
> mocha



  First spec
    ✓ passes


  1 passing (11ms)

```

### Run your test in watch mode

```
npm test -- --watch 
```

This way if you change in your any file and save it test will automatically run.
