# inko-hmac

An HMAC implementation for the Inko programming language.

## Examples

    import hmac.Hmac

    let hmac = Hmac.new_sha1('my key'.to_byte_array)
    hmac.write('hello'.to_byte_array)
    hmac.finish.to_string # => 'fe072cabf75976329b8da24c67dbae2be29740a2'

You can also use `Hmac.sha1` etc. to generate an HMAC hash directly.

    import hmac.Hmac

    let hash = Hmac.sha1('my key'.to_byte_array, 'hello'.to_byte_array)
    hash.to_string # => 'fe072cabf75976329b8da24c67dbae2be29740a2'
