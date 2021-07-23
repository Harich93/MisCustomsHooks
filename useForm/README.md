# useForm

Hook para manejo de input

````js
    const useForm = ( initialState = {} ) => {

        const [values, setValues] = useState(initialState);

        const reset = () =>{
            setValues( initialState );
        } 

        const handleInputChange = ( { target } ) => {
            setValues({
                ...values,
                [ target.name ]: target.value
            });
        };

        return [ values, handleInputChange, reset ];
    }
````

Ejemplo de uso en componente:

````js
    const [ values, handleInputChange ] = useForm({
        name,
    });
    
    const { name } = values;
    
    <input
        type='text'
        name='name'
        value={name}
        onChange={ handleInputChange }
    />
````
