# LarvelBase
This project is template with step by step guide of installing all components and tools to get started with my web development layout.

# Installation

In order to create our desired project we need some tools and frameworks to help us out.

## Tools

Version control is essential for all of your projects.
For version control we can use [git](https://git-scm.com/download/win).

Along with version control we will need [NodeJS](https://nodejs.org) for most of our components and tools to work.
I also recommend installing [XAMPP](https://www.apachefriends.org/download.html). This will install the selected PHP version and has the tools to host your website.
Finally we can install [composer](https://getcomposer.org/).

## Frameworks

Now that we have the proper tools installed we can start creating our project.

### Laravel

Creating a laravel project is super easy with composer.
Open up your `command prompt` or `git bash` and navigate to the folder you want the project folder to be created in.
After you have navigated to the desired folder, use the following command to create your laravel project.
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

To help us make our website look beautiful we need a framework to help us out.
For this we can use [TailwindCSS](https://tailwindcss.com/).
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

After typescript has been installed use the command below to generate a typescript configuration file.
```bash
tsc --init
```
