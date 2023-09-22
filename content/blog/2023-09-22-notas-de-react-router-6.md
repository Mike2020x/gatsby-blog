---
layout: blog
title: Notas de react Router 6
date: '2023-09-22T11:39:27-05:00'
thumbnail: /assets/images/descarga.png
rating: '4'
---
# React Router 6

Como ya sabrás React nos permite crear SPA (Single Page Application), y mostrar varias vistas dentro de la misma página, sin embargo, tener navegación entre páginas, una URL específica para una vista o simplemente retroceder/avanzar en el historial de navegación son características que todo usuario debería poder hacer en un sitio web, React logra todo esto con ayuda de la librería React Router.

## Instalamos React Router Dom

```
npm install react-router-dom@6
```

## BrowserRouter

BrowserRouter es un componente que se utiliza en React para permitir la navegación por una aplicación web utilizando la \[API de Historial HTML5]. Cuando se utiliza BrowserRouter, se establece una correspondencia entre las rutas definidas en la aplicación y las URL que se utilizan en el navegador.

**main.jsx**

```
import { BrowserRouter } from "react-routerdom";
ReactDOM.createRoot(document.getElementById("root")).render(
<React.StrictMode>
<ThemeProvider theme={theme}>
 <BrowserRouter><CssBaseline /><App />
</BrowserRouter>
    </ThemeProvider>
</React.StrictMode>
);
```

## Routes & Route

El componente Routes es el componente principal que se utiliza para definir un conjunto de rutas que la aplicación puede manejar. Este componente se utiliza para definir las rutas principales y secundarias de la aplicación. Dentro de Routes, se pueden definir varias instancias del componente Route para especificar qué componentes deben renderizarse para cada ruta.

El componente Route se utiliza para definir una ruta específica dentro de la aplicación. Para definir una ruta, se utiliza la prop path para especificar la URL que se va a asociar con el componente que se va a renderizar. El componente Route también acepta una prop element que especifica el componente que se debe renderizar cuando se accede a la ruta especificada.

**App.jsx**

```
import { Route, Routes } from "react-router-dom";
<Routes>
  <Route
    path="/"
    element={<Home />}
  />
  <Route
    path="/login"
    element={<Login />}
  />
  <Route
    path="/register"
    element={<Register />}
  />
</Routes>
```

## NavLink

El componente NavLink es un componente proporcionado por la librería "react-router-dom" que se utiliza para crear enlaces de navegación en una aplicación de React.

**Navbar.jsx**

```
import { NavLink } from "react-router-dom";
// navegationLinks.map
<Button
  color="inherit"
  key={item.title}
  component={NavLink}
  to={item.path}
>
  {item.title}
</Button>

// Drawer
<NavListDrawer
  navegationLinks={navegationLinks}
  component={NavLink}
  setOpen={setOpen}
/>
```

**NavListDrawer.jsx**

```
<ListItemButton
  component={component}
  to={item.path}
  onClick={() => setOpen(false)}
>
```

## Resumen

En este artículo, hemos explorado cómo utilizar React Router 6 para habilitar la navegación en aplicaciones React. Hemos aprendido a instalar la librería react-router-dom, a utilizar el componente BrowserRouter para gestionar la navegación, a definir rutas con Routes y Route, y a crear enlaces de navegación con el componente NavLink. Con estas herramientas, puedes proporcionar a tus usuarios una experiencia de navegación fluida en tu aplicación de React.
