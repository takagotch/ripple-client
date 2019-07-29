### ripple-client
---
https://github.com/ripple/ripple-client/

```js
// test/unit/util/jsonRewriterSpec.js
'use strict';

describe('JsonRewriter', function() {
  var rewriter = window.rippleclient.rewriter,
    account = 'xxx',
    data = {}
    
  it('should parse incoming trust line right', function(done) {
    var tx = rewriter.processTxn(data.transaction, data.meta, account);
    expect(tx).to.be.an('object');
    expect(tx.transaction).to.be.an('object');
    
    done();
  });
});

```

```
```

```
```


