# useViewPass

Cambia el estado para hacer visible u ocultar la password en un input.

```js
        const useViewPass = ( initialState = false ) => {
            
            const [isView, setView] = useState( initialState );

            const handleChangeViewPass = () => {
                setView( !isView )
            }

            return [ isView, handleChangeViewPass ]
        }
```
## Aplicación en el componente

```js
        <div className="form-group">
            <input
                type={ isView ? "text" : "password"}
                className="form-control"
                placeholder="Repita la contraseña"
                name='rPassword2'
                value={ rPassword2 }
                onChange={ handleRegisterInputChange } 
                com
                />
        </div>
```

## Estilo CSS 

```css
        .pass {
            position: relative;

        }
        .fas {
            position: absolute;
            padding: 10px;
            cursor: pointer;
            z-index: 100;
        }

        .fas {
            right: 0px;
        }

```

### Iconos

Extraidos de [Font-Awasome](https://fontawesome.com/).
Poner el siguiente código en la cabecera de tu index.html para la instalación.  

~~~
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css" integrity="sha512-iBBXm8fW90+nuLcSKlbmrPcLa0OT92xO1BIsZ+ywDWZCvqsWgccV3gFoRBv0z+8dLJgyAHIhR35VZc2oM/gI1w==" crossorigin="anonymous" referrerpolicy="no-referrer" />
~~~

### Bootstrap

Web oficial [Bootstrap](https://getbootstrap.com/)
O directamente copiar el siguiente código en la cabecera de tu index.html para la instalación.

~~~
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-EVSTQN3/azprG1Anm3QDgpJLIm9Nao0Yz1ztcQTwFspd3yD65VohhpuuCOmLASjC" crossorigin="anonymous">
~~~
