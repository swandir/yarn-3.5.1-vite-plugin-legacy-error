```shell
yarn -v
# 3.5.1

yarn config get pnpEnableInlining
# false

# fails
yarn vite build

# enable pnp data inlining
yarn config set pnpEnableInlining true && yarn

# now it works
yarn vite build

# now disable pnp data inlining again and downgrade yarn
yarn config set pnpEnableInlining false && yarn set version 3.5.0 && yarn

# works too
yarn vite build
```