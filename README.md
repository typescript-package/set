
<a href="https://www.typescriptlang.org/">
  <img
    src="https://avatars.githubusercontent.com/u/189666396?s=150&u=9d55b1eb4ce258974ead76bf07ccf49ef0eb0ea7&v=4"
    title="The typescript package enhances the development of typescript-based applications by providing well-structured, reusable, easy-to-use packages."
  />
</a>

## typescript-package/set

<!-- npm badge -->
[![npm version][typescript-package-npm-badge-svg]][typescript-package-npm-badge]
[![GitHub issues][typescript-package-badge-issues]][typescript-package-issues]
[![GitHub license][typescript-package-badge-license]][typescript-package-license]

A lightweight **TypeScript** library for enhanced `set` management.

## Table of contents

- [Installation](#installation)
- [Api](#api)
  - [`CoreSet`](#coreset)
  - [`DataSet`](#dataset)
- [Contributing](#contributing)
- [Support](#support)
- [Code of Conduct](#code-of-conduct)
- [Git](#git)
  - [Commit](#commit)
  - [Versioning](#versioning)
- [License](#license)

## Installation

### 1. Install peer `data` dependencies

```bash
npm install @typescript-package/data --save-peer
```

### 2. Install the `set` package

```bash
npm install @typescript-package/set --save-peer
```

## Api

```typescript
import {
  // Abstract.
  CoreSet,
  SetOnHook,

  // Class.
  DataSet,
  ImmutableSet,
} from '@typescript-package/set';
```

### `CoreSet`

The abstract core class for building customizable `Set` and `DataCore` related classes.

```typescript
import { CoreSet } from '@typescript-package/set';
```

### `DataSet`

The `DataSet` is a concrete class that extends `CoreSet` and encapsulates its data within a `DataCore` store, providing additional data management capabilities.

```typescript
import { DataSet } from '@typescript-package/data';

// Define a `DataCore` implementation for holding a data in `DataSet`.
export class CustomSetData<Type> extends Data<Set<Type>> {
  constructor(initialValue?: Set<Type>, ...args: any[]) {
    super(initialValue ?? new Set());
    console.log(`...args: any[]`, args);
  }
}

// Create a new `DataSet` instance with predefined entries and customized data holder.
export const dataSet = new DataSet
(
  [0, 27, 37, 47],
  [CustomSetData, 'a', 'b', 1]
);

console.debug(`dataSet`, dataSet);

// Check the `CustomSetData`.
console.log(`Data holder of \`CustomSetData\`:`, dataSet.data); // Output: CustomSetData {#locked: false, #value: Value}

// Log the size of the set
console.log("Size:", dataSet.size); // Output: Size: 4

// Check if a value exists
console.log("Has 27?", dataSet.has(27)); // Output: Has '27'? true

// Add a new value
dataSet.add(57);
console.log("Size after add:", dataSet.size); // Output: Size after add: 5

// Iterate over entries
dataSet.forEach(value => console.log(`${value}`));
// Output:
// 0
// 27
// 37
// 47
// 57

console.debug(`SymbolValue`, dataSet[SymbolValue]());

// Delete an entry
dataSet.delete(0);
console.log("Size after delete:", dataSet.size); // Output: Size after delete: 4

// Clear the set
dataSet.clear();
console.log("Size after clear:", dataSet.size); // Output: Size after clear: 0
```

## Contributing

Your contributions are valued! If you'd like to contribute, please feel free to submit a pull request. Help is always appreciated.

## Support

If you find this package useful and would like to support its and general development, you can contribute through one of the following payment methods. Your support helps maintain the packages and continue adding new.

Support via:

- [Stripe](https://donate.stripe.com/dR614hfDZcJE3wAcMM)
- [Revolut](https://checkout.revolut.com/pay/048b10a3-0e10-42c8-a917-e3e9cb4c8e29)

Thanks for your support!

## Code of Conduct

By participating in this project, you agree to follow **[Code of Conduct](https://www.contributor-covenant.org/version/2/1/code_of_conduct/)**.

## GIT

### Commit

- [AngularJS Git Commit Message Conventions][git-commit-angular]
- [Karma Git Commit Msg][git-commit-karma]
- [Conventional Commits][git-commit-conventional]

### Versioning

[Semantic Versioning 2.0.0][git-semver]

**Given a version number MAJOR.MINOR.PATCH, increment the:**

- MAJOR version when you make incompatible API changes,
- MINOR version when you add functionality in a backwards-compatible manner, and
- PATCH version when you make backwards-compatible bug fixes.

Additional labels for pre-release and build metadata are available as extensions to the MAJOR.MINOR.PATCH format.

**FAQ**
How should I deal with revisions in the 0.y.z initial development phase?

> The simplest thing to do is start your initial development release at 0.1.0 and then increment the minor version for each subsequent release.

How do I know when to release 1.0.0?

> If your software is being used in production, it should probably already be 1.0.0. If you have a stable API on which users have come to depend, you should be 1.0.0. If you’re worrying a lot about backwards compatibility, you should probably already be 1.0.0.

## License

MIT © typescript-package ([license][typescript-package-license])

## Packages

- **[@typescript-package/affix](https://github.com/typescript-package/affix)**: A **lightweight TypeScript** library for the affix - prefix and suffix.
- **[@typescript-package/are](https://github.com/typescript-package/are)**: Type-safe `are` checkers for validating value types in TypeScript.
- **[@typescript-package/data](https://github.com/typescript-package/data)**: A lightweight **TypeScript** library for basic data management.
- **[@typescript-package/descriptor](https://github.com/typescript-package/descriptor)**: A **lightweight TypeScript** library for property descriptor.
- **[@typescript-package/guard](https://github.com/typescript-package/guard)**: Type-safe guards for guarding the value types in TypeScript.c
- **[@typescript-package/history](https://github.com/typescript-package/history)**: A **TypeScript** package for tracking history of values.
- **[@typescript-package/is](https://github.com/typescript-package/is)**: Type-safe is checkers for validating value types in TypeScript.
- **[@typescript-package/map](https://github.com/typescript-package/map)**: A lightweight **TypeScript** library for enhanced `map` management.
- **[@typescript-package/name](https://github.com/typescript-package/name)**: A **lightweight TypeScript** library for the name with prefix and suffix.
- **[@typescript-package/property](https://github.com/typescript-package/property)**: A **lightweight TypeScript** package with features to handle object properties.
- **[@typescript-package/queue](https://github.com/typescript-package/queue)**: A **lightweight TypeScript** library for managing various queue and stack structures.
- **[@typescript-package/range](https://github.com/typescript-package/range)**: A **lightweight TypeScript** library for managing various types of ranges.
- **[@typescript-package/regexp](https://github.com/typescript-package/regexp)**: A **lightweight TypeScript** library for **RegExp**.
- **[@typescript-package/state](https://github.com/typescript-package/state)**: Simple state management for different types in **TypeScript**.
- **[@typescript-package/storage](https://github.com/typescript-package/storage)**: The storage of data under allowed names.
- **[@typescript-package/type](https://github.com/typescript-package/type)**: Utility types to enhance and simplify **TypeScript** development.
- **[@typescript-package/wrapper](https://github.com/typescript-package/wrapper)**: A **lightweight TypeScript** library to wrap the text with the opening and closing chars.

<!-- This package: typescript-package  -->
  <!-- GitHub: badges -->
  [typescript-package-badge-issues]: https://img.shields.io/github/issues/typescript-package/set
  [isscript-package-badge-forks]: https://img.shields.io/github/forks/typescript-package/set
  [typescript-package-badge-stars]: https://img.shields.io/github/stars/typescript-package/set
  [typescript-package-badge-license]: https://img.shields.io/github/license/typescript-package/set
  <!-- GitHub: badges links -->
  [typescript-package-issues]: https://github.com/typescript-package/set/issues
  [typescript-package-forks]: https://github.com/typescript-package/set/network
  [typescript-package-license]: https://github.com/typescript-package/set/blob/master/LICENSE
  [typescript-package-stars]: https://github.com/typescript-package/set/stargazers
<!-- This package -->

<!-- Package: typescript-package -->
  <!-- npm -->
  [typescript-package-npm-badge-svg]: https://badge.fury.io/js/@typescript-package%2Fset.svg
  [typescript-package-npm-badge]: https://badge.fury.io/js/@typescript-package%2Fset

<!-- GIT -->
[git-semver]: http://semver.org/

<!-- GIT: commit -->
[git-commit-angular]: https://gist.github.com/stephenparish/9941e89d80e2bc58a153
[git-commit-karma]: http://karma-runner.github.io/0.10/dev/git-commit-msg.html
[git-commit-conventional]: https://www.conventionalcommits.org/en/v1.0.0/
