# Go pg escape.

 Escape Postgres queries.
 

## Installation

```
$ go get github.com/drylikov/go-pg-escape
```

## Example

```go
s := Escape("SELECT %I FROM %I WHERE %I=%L", "some stuff", "some table", "some column", "some value")
exp := `SELECT "some stuff" FROM "some table" WHERE "some column"='some value'`
assert.Equal(t, exp, s)
```





















