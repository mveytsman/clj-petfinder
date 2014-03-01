# clj-petfinder

A Clojure library for interacting with the Petfinder.com API.

## Installation

Put the following in `project.clj`
```clojure
[clj-petfinder "0.1.0-SNAPSHOT"]
```

## Usage

### Authentication
You will need to make a map of your Petfinder.com credentials that you then pass to all of the API calls

```clojure
(def creds {:api-key "YOUR KEY" :api-secret "YOUR SECRET"})
```

### Examples

```clojure
; List Breeds
(breeds creds "cat")

; Get Pet by ID
(pet creds "7411969")

; Get Random Pet
(random-pet creds {:animal "cat" :breed "tiger" :location "90210"})

; Search for Pets
(find-pets creds "Toronto, ON" {:animal "cat" :count 3})

; Get Shelter by ID
(shelter creds "ON155")

; Search for Shelters
(find-shelters creds "Toronto, ON" {:count 3})

; Search for Shelters by Breed
(find-shelters-by-breed creds "cat" "tiger")

; List Pets by Shelter
(shelter-pets creds "AR270")
```

## License

Copyright © 2014 Max Veytsman

Distributed under the Eclipse Public License either version 1.0 or (at
your option) any later version.
