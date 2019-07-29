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
    expect(tx.transaction.type).to.equal('trusted');
    expect(tx.transaction.currency).to.equal('TST');
    expect(tx.transaction.counterparty).to.equal('xxx');
    expect(tx.effects).to.be.an.instanceof(Array);
    expect(tx.effects).to.have.length(1);
    expect(tx.effects[0].type).to.equal('trust_create_remote');
    expect(tx.effects[0].currency).to.equal('TST');
    expect(tx.effects[0].noRipple).to.be.true;
    assert.equal(tx.effects[0].limit.to_number(), 0);
    assert.equal(tx.effects[0].limit_peer.to_number(), 541);
    
    done();
  });
});

```

```
```

```
```


