# useCounter Hook

    const useCounter = ( initialState = 10 ) => {

        const [counter, setCounter] = useState(initialState);

        const increment = () => {
            setCounter( counter + 1 );
        };

        const decrement = () => {
            setCounter( counter - 1 );
        };

        const reset = () => {
            setCounter( initialState );
        }; 

        return {
            counter,
            increment,
            decrement,
            reset
        };
    }

### Ejemplo de uso:

    const [ counter, increment, decrement, reset ] = useCounter();
