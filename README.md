# LarvelBase
This project is template with step by step guide of installing all components and tools to get started with my web development layout.

# Installation

## Tools
Before we can create our desired project and install all the components we need some tools to help us build it.
Let's start by installing our version control [git](https://git-scm.com/download/win).

Along with version control we will need [NodeJS](https://nodejs.org) for most of our components and tools to work.
I also recommend installing [XAMPP](https://www.apachefriends.org/download.html) to host your website and to installs the selected PHP version with it.
After installing the tools mentioned above we need [composer](https://getcomposer.org/).

## Frameworks

### Laravel

Now that we have the proper tools installed we can create a laravel project using composer.
Open up your `command prompt` or `git bash` and navigate to the desire root folder you want the project to be installed in.
After you have navigated to the desired folder use the following command to create your laravel project.
*Note: Make sure to replace `application-name` with the desired project name.*
```bash
composer create-project laravel/laravel application-name
```

After the laravel project has been created navigate to the project folder and execute the following command to install the remaining components.
```bash
npm install
```

*Make sure to change the application name and other configurations in the `.env` file.*

### Tailwind

To make our websites beautiful we will need [TailwindCSS](https://tailwindcss.com/).
Install it and it's postcss processing component with the following command.
```bash
npm install tailwindcss@latest postcss@latest autoprefixer@latest
```
The postcss processing allows you to use @apply keyword in your css files.

We also need the following tailwind plugins
- [Typography](https://github.com/tailwindlabs/tailwindcss-typography)
- [Forms](https://github.com/tailwindlabs/tailwindcss-forms)
- [Aspect Ratio](https://github.com/tailwindlabs/tailwindcss-aspect-ratio)
- [Line Clamps](https://github.com/tailwindlabs/tailwindcss-line-clamp)
- [Container Queries](https://github.com/tailwindlabs/tailwindcss-container-queries)

You can install the plugins with the following commands.
```bash
npm install -D @tailwindcss/typography
npm install -D @tailwindcss/forms
npm install -D @tailwindcss/aspect-ratio
npm install -D @tailwindcss/line-clamp
npm install @tailwindcss/container-queries
```

Then add the plugins to your `tailwind.config.js` file:

```js
// tailwind.config.js
module.exports = {
  theme: {
    // ...
  },
  plugins: [
    require('@tailwindcss/typography'),
    require('@tailwindcss/forms'),
    require('@tailwindcss/aspect-ratio'),
    require('@tailwindcss/line-clamp'),
    // ...
  ],
}
```

### TypeScript
To reduce errors and get our web scripts more object oriantated like in C languages, we need to install [TypeScript](https://www.typescriptlang.org/).
You can install it with the following command.
```bash
npm install -g typescript
```
