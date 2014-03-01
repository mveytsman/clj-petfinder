# clj-petfinder

A Clojure library for interacting with the Petfinder.com API.

## Usage

### Authentication
You will need to make a map of your Petfinder.com credentials that you then pass to all of the API calls

```clojure
(def creds {:api-key "YOUR KEY" :api-secret "YOUR SECRET"})
```

### Examples

#### List Breeds

```clojure
(breeds creds "cat")
```

#### Get Pet by ID

```clojure
(pet creds "7411969")
 ```
 
#### Get Random Pet

```clojure
(random-pet creds {:animal "cat" :breed "tiger" :location "90210"})
```

#### Search for Pets

```clojure
(find-pets creds "Toronto, ON" {:animal "cat" :count 3})
```

#### Get Shelter by ID

```clojure
(shelter creds "ON155")
```

### Search for Shelters

```clojure
(find-shelters creds "Toronto, ON" {:count 3})
```

### Search for Shelters by Breed

```clojure
(find-shelters-by-breed creds "cat" "tiger")
```

### List Pets in a Shelter

```clojure
(shelter-pets creds "AR270")
```

## License

Copyright © 2014 Max Veytsman

Distributed under the Eclipse Public License either version 1.0 or (at
your option) any later version.
