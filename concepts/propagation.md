# Propagation

When an `ItemClass` inherits from another `ItemClass`, it can be unknown or undefined how any changes to the parent `ItemClass` should be propagated to the child `ItemClass`.

Raindrops introduces the concept of permission-less updates(`--inheritance-update`) to handle this situation.

{% tabs %}
{% tab title="ItemClass" %}
```bash
item-cli update_item_class \
         -k <keypair> \
         --env devnet \
         -cp example-configs/itemClass.json \
         --inheritance-update
```

This tells the endpoint **not** to accept any changes to a child `ItemClass` except for those _**also**_ present on the parent `ItemClass`. This means anybody can enforce inheritance at any time across any size tree of inheritance.
{% endtab %}

{% tab title="ItemClass instance" %}
```
item-cli update_item \
         -k <keypair> \
         --env devnet \
         -m DQKJRRHjyiS1DgDuMWtdD2Cy2nbLqEP86sQ8nnBQMv2w \
         -i 10 \
         -cm FKZJRRHjyiS1DgDuMWtdD2Cy2nbLqEP86sQ8nnBQMv2w \
         --inheritance-update
```

This updates the Item instance with the new `ItemUsageStates` that may arise from changes in `ItemUsage`s in the parent class.
{% endtab %}
{% endtabs %}

Similar logic exists for the [Player](https://github.com/long-banana/raindrops-docs/blob/main/concepts/broken-reference/README.md) contract.
