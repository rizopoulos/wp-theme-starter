# The Mozaik WordPress Theme Boilerplate

The goals of the boilerplate are to:

1. be a product used and produced by the entire team (suggestions, issues and pull requests are welcome and encouraged)
1. be easy to set up
1. be easy to use
1. be easy to understand
1. be easy to modify
1. guide the development process to be consistent where it can be
1. offer a robust development and build workflow (currently powered by the cli and gulp)
1. make getting off the ground with a new project really fast

## Reading Recommendations

1. [WordPress Developer Documentation](http://codex.wordpress.org/Developer_Documentation)
1. We generally follow the [WordPress PHP Coding Standards](https://make.wordpress.org/core/handbook/coding-standards/php/) in our WP code.

## Important Prerequisites

1. Read [the WordPress theme development guidelines](http://codex.wordpress.org/Theme_Development)
1. Understand [the WordPress template hierarchy](http://codex.wordpress.org/images/9/96/wp-template-hierarchy.jpg)
1. Understand [the WordPress Loop](http://codex.wordpress.org/The_Loop)
1. Understand [how WordPress helps with Data Validation/Sanitization](http://codex.wordpress.org/Data_Validation)
1. Read up on the following WordPress core APIs:
	- [the Plugin API](http://codex.wordpress.org/Plugin_API)
	- [the Shortcode API](http://codex.wordpress.org/Shortcode_API)

## Development Guidelines

- Avoid committing the built theme to the project repository
- Avoid making changes directly to the built theme -- Always use the build process
- In production avoid uploading the theme development directory to a public server
- Avoid committing the `wp-uploads` directory to the project repository
- It is good practice to enable `WP_DEBUG` in your `wp-config.php` file, *but only* during development

## Standard Theme Development Process

### Development

1. Install WordPress and clear it of unnecessary default themes & plugins
1. Clone/Download this repository into a directory in your WordPress `wp-content/themes` directory
1. Change the `package.json` with your new theme's configuration
1. Open the terminal and `cd wp-content/themes/<devthemename>`
1. Run `npm install` to install all dev dependencies
1. Run `gulp` to begin the dev build process that uses libsass, browsersync and webpack
1. Log in to the admin and enable the *built theme*
1. Develop your theme in the `/assets` and `/theme` directories, the built theme will be generated by gulp

### Production

1. Delete files you are not using from inside the `/theme` directory
1. [Add a screenshot.png](http://codex.wordpress.org/Theme_Development#Screenshot)
1. Before deploying run `gulp --build`
1. Deploy the built theme directory, *not the dev directory*