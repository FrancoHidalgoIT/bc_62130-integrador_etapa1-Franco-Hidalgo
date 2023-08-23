# Para comezar a desarrollar

## Instalo las dependencias (leer el archivo package.json)

```sh
npm i
npm install
```

## Arracar el servidor de desarrollo

```sh
npm run dev
```


## Una vez terminado el desarrollo. Puedo buildear el proyecto.

```sh
npm run build
```

------------------------------------------
/* ------------------------------------- */
/* HEADER                                */
/* ------------------------------------- */

.main-header {
  background-color: rgb(209, 232, 255);
  display: flex;
  flex-direction: column;
  align-items: center;
 
  @media (max-width: 768px) {
    & {
      flex-direction: column-reverse;
    }
  }
} 


#menu {
  display: none;

  &:checked + .nav-bar {
    display: block;
  }

  &:checked ~ .search-bar .menu-toogle__label {
    background-color: yellow;
  }

} 
 

/* ------------------------------------- */
/* NAVBAR                                */
/* ------------------------------------- */

.nav-bar {
  color: #fff;
  display: flex;


  &__nav-list {
    position: relative;
    display: flex;
    list-style-type: none;
    

    @media (max-width: 768px) {
      & {
        flex-direction: column;
      }
    }
  }

  &__nav-item {
    text-align: center;
    background-color: transparent;
  }

  &__nav-link {
      

    display: block;
    color: black;
    padding: 1em 2em;
    border-radius: 5px 5px;
    border: none;

    &:hover {
      color: black;
      background-color: aqua;
    }

  }

  @media (max-width: 768px) {
    & {
      display: none;
      margin-right: 0px 0px;
    }
  }
} 

/* ------------------------------------- */
/* SEARCH BAR                            */
/* ------------------------------------- */

.search-bar {
  background-color: olivedrab;
  display: flex;
  justify-content: space-between;

  &__logo-container,
  &__form-container {
    padding: 1em;
  }

  &__logo-container {
    background-color: yellow;
  }

  &__form-container {
    background-color: gold;
    display: flex;
    flex-basis: 100%;
    justify-content: center;
  }

  &__form-label {
    background-color: greenyellow;
  }

  &__form-search {
    background-color: deeppink;
    width: 70%;
  }

  &__form-submit {
    background-color: darkslategray;
    color: white;
  }

  &__carrito-container {
    flex: 0 0 3em; /* shorthand (grow shrink basis */
    background-color: goldenrod;
  }
}

/* ------------------------------------- */
/* MENU TOOGLE                           */
/* ------------------------------------- */

.menu-toggle {
  display: none;
  background-color: red;
  flex: 0 0 3em;
  position: relative;
  cursor: pointer;

  &__label {
    display: block;
    background-color: black;
    height: 100%;
  }

  &__top-bread,
  &__meat,
  &__bottom-bread {
    display: block;
    background-color: #333;
    height: .2em;
    position: absolute;
    left: .5em;
    right: .5em;
  }

  &__top-bread {
    top: .8em;
  }

  &__meat {
    top: 50%;
    margin-top: -.1em;
  }

  &__bottom-bread {
    bottom: .8em;
  }

  @media (max-width: 768px) {
    & {
      display: block;
    }
  }
}
