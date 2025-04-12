# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

### All
- **Dev**: `composer run dev`

### Backend
- **Lint**: `composer run lint -- --dirty` (view errors) or `composer run lint:fix -- --dirty` (fix errors)
- **Test**: `composer run test` (all files) or `composer run test -- tests/Feature/SomeTest.php` (single file)

### Frontend
- **Format**: `npm run format`
- **Lint**: `npm run lint`

## Style Guidelines

### Common
- **File encoding**: UTF-8, LF line endings
- **Trailing newline**: all files must have a newline at the end of the file
- **Git**: add prefix in commit log like feat, fix, build, chore, ci, docs, style, refactor, perf, test
  - like this: "fix: incorrect usage of Foo component"

### Backend
- **PHP**: Use PSR-12 standards. Laravel Pint for formatting
- **Error Handling**: Use Laravel's built-in exception handling
- **Test**:
  - Common
    - use `it()` function instead of `test()`
    - group tests with `describe()` function when the test file contains multiple `it()` functions
  - Feature Test
    - use `assertInertia()` to assert props are correct when props given by the Controller

### Frontend
- **JavaScript/TypeScript**: 
  - Use 4 spaces for indentation, 150 character line limit
  - Single quotes for strings, semicolons required
  - Use prettier for formatting with organize-imports plugin
- **Vue**: Use Vue 3 Composition API with TypeScript
- **Naming**: Use camelCase for JS/TS variables, PascalCase for components
- **Types**:
  - TypeScript with explicit types where possible
  - use `type` instead of `interface` when you write a custom type
- **Imports**: Organize imports in alphabetical order
- **UI Components**: Use pre-built UI components from resources/js/components/ui/
- **Styling**: Use Tailwind CSS with prettier-plugin-tailwindcss for class sorting

Follow all ESLint/Prettier configurations defined in the project.

## Requirements/Specifications

- **Summary**: described in docs/README.md
- **Detail**: described in docs/specs/*.md
