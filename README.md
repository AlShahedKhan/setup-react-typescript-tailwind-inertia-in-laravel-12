#Setup React, TypeScript in laravel 12 project 
1. Create new project and cd to the new project
2. Run this to setup inertia server-side in laravel 12
```
composer require inertiajs/inertia-laravel
```
3. Create app.blade.php in /views
```
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <title>Laravel</title>
        @viteReactRefresh
        @vite(['resources/css/app.css', 'resources/js/app.tsx'])
        <!-- In this article, we are going to use JSX syntax for React components -->
        @inertiaHead
    </head>
    <body>
        @inertia
    </body>
</html>
```
