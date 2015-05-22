# consul-plugins-titan

Recipes are not yet available on the Cloudbreak UI, thus if you’d like to try this Titan plugin, we suggest to use the [Cloudbreak Shell](https://github.com/sequenceiq/cloudbreak-shell).

Clone the project from GitHub.

```
git clone https://github.com/sequenceiq/consul-plugins-titan.git
```

From Cloudbreak shell (after the usual steps - use `hint`):

```
recipe add --file /consul-plugins-titan/titan-recipe.json
```

Alternatively you can use the `--url` parameter to create the Titan recipe.

```
recipe add --url https://raw.githubusercontent.com/sequenceiq/consul-plugins-titan/master/titan-recipe.json
```

For using your recipe you have to select it. (you can check your recipes with `recipe list` command)
```
recipe select --id RECIPE_ID
```
In case of your blueprint and credential have already been selected and the instance groups are configured (`instancegroup configure`), create your stack with `create stack` command. If your stack is ready, you are able to create your cluster:

```
cluster create --description "Cloudbreak provisoned cluster with Titan"
```
