# GLBLoader

Provides functions for parsing or generating the binary GLB containers used by glTF (and certain
other formats).

Takes a JavaScript data structure and encodes it as a JSON blob with binary data (e.g. typed arrays)
extracted into a binary chunk.

## Functions

### parseGLB(arrayBuffer)

Parses an in-memory, GLB formatted `ArrayBuffer` into a JavaScript "JSON" data structure with
inlined binary data fields.

Parameters:

- `arrayBuffer` (ArrayBuffer) - an ArrayBuffer to decode

Returns: `Object`

### encodeGLB(json)

Writes JavaScript JSON data structure into an arrayBuffer that can be written atomically to file,
extracting binary fields from the data and placing these in a compact binary chunk following the
"stripped" JSON chunk.

Parameters:

- `json` (Object) - json object to encode

Returns: `ArrayBuffer`
