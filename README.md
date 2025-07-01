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

4. Create its middleware via
   `php artisan inertia:middleware`

5. Register middleware via

```
$middleware->web(append: [
            HandleInertiaRequests::class
        ]);
```
6. Give Client-side setup with npm via
```
npm install @inertiajs/react react react-dom
npm install -D @types/react @types/react-dom typescript @vitejs/plugin-react
```

