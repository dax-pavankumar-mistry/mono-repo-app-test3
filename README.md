## Setup for monorepo projects

### Step 1: Global installation
```
yarn global add turbo
```

### Step 2: Create turbo project
```
npx create-turbo@latest
```
- Add project directory name when prompted
- select package manager (yarn, npm, pnpm)

### Step 3: To run project
- To run both apps together
```
yarn dev
yarn build
```

- To run individual apps
```
yarn dev --filter=app1
yarn dev --filter=app2

yarn build --filter=app1
yarn build --filter=app2
```

### For consistent dependency versions across all packages
```
npm install -g syncpack
```

- To list all dependencies with different versions
```
syncpack list-mismatches
syncpack list-mismatches --filter=packageName
```

- To fix all mismatched versions
```
syncpack fix-mismatches
syncpack fix-mismatches --filter=packageName
```
