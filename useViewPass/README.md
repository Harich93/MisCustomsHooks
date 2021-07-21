## useViewPass

Cambia el estado para hacer visible u ocultar la password en un input.

        export const useViewPass = ( initialState = false ) => {
            
            const [isView, setView] = useState( initialState );

            const handleChangeViewPass = () => {
                setView( !isView )
            }

            return [ isView, handleChangeViewPass ]
        }

### Icono

Iconos utilizado extraido de font-awasome.
Poner el siguiente codigo en la cabecera de tu index.html para la instalación.  

~~~
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css" integrity="sha512-iBBXm8fW90+nuLcSKlbmrPcLa0OT92xO1BIsZ+ywDWZCvqsWgccV3gFoRBv0z+8dLJgyAHIhR35VZc2oM/gI1w==" crossorigin="anonymous" referrerpolicy="no-referrer" />
~~~
