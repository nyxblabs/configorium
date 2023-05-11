# Changelog


## v0.0.2


### 🚀 Enhancements

  - **index.ts): add functionality to read, write, parse, and update configuration files ✅ test(index.test.ts:** Add tests for read, write, parse, and update functionality The index.ts file adds functionality to read, write, parse, and update configuration files. The read function reads a configuration file and returns its contents as an object. The write function writes an object to a configuration file. The parse function parses a configuration file and returns its contents as an object. The update function updates a configuration file with new values. The index.test.ts file contains tests for the read, write, parse, and update functionality. ([6a18fd9](https://github.com/nyxblabs/configorium/commit/6a18fd9))

### 🩹 Fixes

  - **package.json:** Correct changelog command to use nyxlx instead of changelogen The changelog command was updated to use the correct command, nyxlx, instead of changelogen. This ensures that the changelog is generated and pushed correctly during the release process. ([34fef62](https://github.com/nyxblabs/configorium/commit/34fef62))

### 🏡 Chore

  - **github:** Add various GitHub templates and files This commit adds various GitHub templates and files such as issue templates, pull request template, funding file, and code of conduct. These templates and files help contributors to follow the guidelines and standards set by the project. The CONTRIBUTING.md file is also added, which provides a link to the contribution guidelines. ([9ebdc5f](https://github.com/nyxblabs/configorium/commit/9ebdc5f))
  - **package.json:** Update scripts to include prepack, build, dev, lint, release, and test The package.json file has been updated to include new scripts for prepack, build, dev, lint, release, and test. The prepack script runs the nyxr build command, the build script runs the unbuild command, the dev script runs the vitest command, the lint script runs the eslint command, the release script runs the nyxr test command, changelogen command, and pnpm publish command, and the test script runs the nyxr lint command and the vitest run command with coverage. These changes improve the development workflow by providing more options for building, testing, and releasing the application. ([3b9968b](https://github.com/nyxblabs/configorium/commit/3b9968b))
  - **package.json): update changelogen dependency to latest version ✅ test(index.test.ts:** Refactor test suite to use single quotes and remove unused import statements The changelogen dependency in package.json was updated to the latest version to ensure that the latest features and bug fixes are available. The test suite was refactored to use single quotes and remove unused import statements to improve code readability and maintainability. ([0164287](https://github.com/nyxblabs/configorium/commit/0164287))

### 🎨 Styles

  - **.eslintignore): add dist folder to eslint ignore list 🎨 style(.eslintrc): add eslint-config-unjs and disable @typescript-eslint/no-non-null-assertion rule 🎨 style(.gitignore:** Add dist and types folders to git ignore list The dist folder is now added to the eslint ignore list to avoid linting the compiled code. The eslint-config-unjs package is added to the eslint configuration to improve the linting rules. The @typescript-eslint/no-non-null-assertion rule is disabled to avoid linting errors. The dist and types folders are added to the git ignore list to avoid committing the compiled code and type definitions. ([b4fe55b](https://github.com/nyxblabs/configorium/commit/b4fe55b))

### ❤️  Contributors

- Nyxb <contact@nyxb.xyz>

