# inko-hmac

An HMAC implementation for the Inko programming language.

## Examples

    import hmac.Hmac

    let hmac = Hmac.new_sha1('my key')
    hmac.write('hello')
    hmac.finish.to_string # => 'fe072cabf75976329b8da24c67dbae2be29740a2'

You can also use `Hmac.sha1` etc. to generate an HMAC hash directly.

    import hmac.Hmac

    let hash = Hmac.sha1('my key', 'hello')
    hash.to_string # => 'fe072cabf75976329b8da24c67dbae2be29740a2'
