# SimpleStorage Contract

Some part of the `SimpleStorage` contract demonstrates how to use mappings, events, and Solidity’s data locations (storage, memory, and calldata)
to create an efficient and interactive smart contract for storing and retrieving data on the Ethereum blockchain.

## Implementation Details

### Mappings  
I implemented a mapping called `nameToFavoriteNumber` that associates a person's name with their favorite number. 
This approach allows for efficient data storage and quick retrieval. With the `addPerson_M` function,
I add a new entry to this mapping, storing names as keys and their favorite numbers as values. 

### Events  
I created an event called `NumberUpdated`. By emitting this event in the `storeNumber_M` function. 

### Data Locations  
To demonstrate the different data locations in Solidity, my contract uses:
- **Storage**: The `nameToFavoriteNumber` mapping is stored persistently on the blockchain.
- **Memory**: I use a function called `updateNumber` with a memory variable, `tempNumber`, for intermediate calculations,
  showing how memory is used for temporary data during function execution.
- **Calldata**: The `concatenateString` function uses a `calldata` parameter for input efficiency,
  as this location is for function inputs that won’t be modified, saving gas and reducing costs.
