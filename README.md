# Sylius Admin Module for Ingredients

## Table of Contents
- [Project Setup](#project-setup)
- [Admin Login](#admin-login)
- [Creating the Ingredients Module](#creating-the-ingredients-module)
- [Optional Enhancements](#optional-enhancements)
- [Submitting Your Work](#submitting-your-work)

## Project Setup

To get started with the Sylius project, you can follow these steps:

1. **Docker Installation**: If you have Docker installed, you can use it to set up the project.
    - Clone the project repository.
    - Navigate to the project directory.
    - Run `docker-compose up -d` to start the containers.
    - Wait some minutes. During that you can check the containers what is happening exactly. (It will run the composer install command, etc.)
    - You can use the `bin/console sylius:install` command if it will be necessary. You can create a new admin user for this command.
    - You should now have the project accessible at http://localhost.

2. **Environment Configuration**: Ensure that you have set up the necessary environment variables, such as your database connection details. Refer to the project's documentation for specific configuration details.

## Admin Login

After setting up the project, you can access the Sylius admin interface at `http://localhost/admin/`. Log in with the appropriate credentials or create a user with admin privileges to proceed with the task. Default login: `sylius` is the username and `sylius` is the password

## Creating the Ingredients Module

The main task is to create an ingredients module in the Sylius administration system. This module should allow administrators to manage ingredients. For the first step, it is totally enough to create only a save form for this. Here's how you can achieve this:

1. **Create a New Module Folder**: Inside the existing `/src/` folder of your project, create a new folder named `/Sylius/Bundle/IngredientsBundle/`.

2. **Override the Base Sylius Modules**: Please try to solve this task as a module. So, if it is necessary, please try to override the existing Sylius bundles and components. You can find them inside the `vendor/sylius/sylius/src/Sylius` folder.

3. **Create a New Admin Page**: To create a new admin page for managing ingredients, follow these steps:
    - Define a new routing configuration for the ingredients module.
    - Create a new controller for handling ingredient-related actions.
    - Create a template for the admin page.

4. **Define Fields for Ingredients**:
    - You should create a form to add ingredients to the database. The form should include the following fields:
        - Ingredient Name (string)
        - Supplier (you can use a database relation structure or a string)
        - Supplier SKU Number (string)

5. **Controller Actions**: Create controller actions for adding, editing, and deleting ingredients in the database.

6. **Database Configuration (Optional)**:
   - If you choose to use a database relation structure for the supplier field, make sure to define the necessary entities and relationships.
   - Please use migrations for the new database table. You can find some examples in the Sylius documentations.

### Optional Enhancements

If you find the task too easy and want to add additional functionality, consider implementing the following enhancements:

- Implement validation and error handling for the ingredient form.
- Add a list view to display all existing ingredients with options to edit or delete them.
- Implement search and filtering options for the ingredients list.
- Create a stock management system that connects ingredients with products.

## Submitting Your Work

Once you have completed the task, you can submit your work to the employer by following these options:

- **Email**: Compress your project files and send them as an email attachment to the provided contact.
- **GitHub**: If you prefer to use version control, upload your project to a private GitHub repository and share the repository link with the employer.

That's it! You've successfully created a Sylius admin module for managing ingredients. Feel free to explore additional features and functionalities if you find the task too simple. Good luck with your test task!

If you have any questions, please do not hesitate to contact us.

You can find the base Sylius documentations here:
- https://github.com/Sylius/Sylius-Standard
- https://docs.sylius.com/en/1.12/
