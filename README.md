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

### Run your first test


Add this command in your package.json to run test

```
"test": "mocha -r ts-node/register spec/**/*.spec.ts"
```
