# Lein Cheat Sheet

## Tests

### Run all tests

    lein test

### Run specific tests namespace

    lein test :only myns.person.bill-test


### JSON to EDN

Open the lein console.

    lein 

Create a namespace (e.g. `hello`) and require cheshire

    (ns hello  (:require [cheshire.core :as json]))

Define your json as a string scaping double quotes.

    (def my-json-string "{\"number\": 1}")

Convert the json string to EDN and print it pretty

    (clojure.pprint/pprint (cheshire.core/parse-string my-json-string true))

Output:

{:number 1}

```