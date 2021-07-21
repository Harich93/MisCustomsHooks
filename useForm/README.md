# useForm

Hook para manejo de input

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
    
Ejemplo:

    const [ values, handleInputChange ] = useForm({
        name,
    });
    
    <input
        type='text'
        name='name'
        value={name}
        onChange={ handleInputChange }
    />
