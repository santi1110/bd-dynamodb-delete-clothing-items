Since we only ever want to retrieve items from the table when they're active, we can hardcode the value 'active' into the
`load()` method meaning that we don't need to accept a value for the sort key.
