## API Definition

Available methods:



### **griddb.entities.create**

Creates an entity based on following information:

- name: name of the entity.
- countryID: ID of the country where the entity is located
- cityID: ID of the city where the entity is located


Note: An entity is always linked to a private keypair, only one entity can be created per keypair.

### **griddb.entities.update**

updates an entity based on following information:

- name: name of the entity.
- countryID: ID of the country where the entity is located
- cityID: ID of the city where the entity is located


### **griddb.entities.get**

Fetches an entity from storage based on an ID.


### **griddb.entities.list**

lists all entities from storage.



### **griddb.entities.delete**

Deletes the entity linked to the private key.



### **griddb.twins.create**

Creates a twin based on following information:

- peerID: Yggdrassil peer ID.



Note: A twin is by default anonymous, check `griddb.twins.add_entit` to add an entity to a twin.

### **griddb.twins.get**

Get twin from storage based on an ID.


### **griddb.twins.list**

lists all twins from storage.



### **griddb.twins.delete**

Deletes a twin from storage based on an ID. Only the creator of this twin can delete this twin.

### **griddb.twins.set_entity**

Add an entity to a twin. The entity that is being added must sign a message composed of the twinID and entityID. Only the twin's owner can add an entity to it's twin.

- entityID: entity ID to add.
- twinID: twin ID to update.
- signature: signature signed by private key of entity


### **griddb.twins.delete_entity**

Removes an entity from a twin. Only the twin's owner can remove an entity from it's twin.

- entityID: entity ID to remove.
- twinID: twin ID to update.



### **griddb.signer.sign**

Sign an entityID and twinID combination and returns a signed message.

- entityID: entity ID.
- twinID: twin ID.

```js
```

### **griddb.tft.vest**

Vest an amount of tokens for a specific duration, if the tft price provided is equal to the real tft price. It unlocks the current and previous vesting months.

locked, perBlock, startingBlock, tftPrice

- locked: amount of tokens to lock
- perBlock: amount of tokens that unlock every block (1 block = 6 seconds)
- startingBlock: block number to start the vesting on
- tftPrice: price of tft that will trigger unlock condition (decimal number eg: 0.50)
- callback: optional callback



### **griddb.tft.price**

Gets the TFT Price.

```js
const price = await client.getPrice()
```

### **griddb.tft.balance**

Gets your account's balance.


https://github.com/threefoldtech/substrate-pallet-tfgrid/blob/master/src/types.rs

### **griddb.farm.get**

params: 
- farm_id
- farm_name?
response: 
- name: string
- entity_id: int
- twin_id: int
- pricing_policy_id: int
- certification_type: (farm, entity)
- country_id: int
- city_id: int

### **griddb.farm.create**
creates farm with
- name: string
- entity_id: int
- twin_id: int
- pricing_policy_id: int
- certification_type: (farm, entity)
- country_id: int
- city_id: int

response: 
- farm_id

## **griddb.farm.list**
lists all farms

response: 
list of farm objects

## **griddb.farm.delete**

params:
- farm_id

response: 
- bool True/ false in case of error
- error in case of error


## **griddb.node.create**
creates a node

params: 

- id: int
- farm_id: int
- twin_id: int
- resources: Resources
- location: longitude latitude
- country_id: int
- city_id: int

reponse: 
id

## **griddb.node.get**
gets one node by id
response: 
- id: int
- farm_id: int
- twin_id: int
- resources: Resources
- location: longitude latitude
- country_id: int
- city_id: int

## **griddb.node.list**
lists all nodes

## **griddb.node.delete**
delete a specific node by id