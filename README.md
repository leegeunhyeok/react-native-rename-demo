# react-native-rename-demo

This project following official [environment setup guide](https://reactnative.dev/docs/getting-started).

## Steps

### 1. Create new react-native project

```bash
npx react-native init AwesomeTSProject --template react-native-template-typescript
```

### 2. Enable fabric

```properties
# gradle.properties

newArchEnabled=true
```

### 3. Build

```bash
# It takes few minutes...
yarn android
```

- Build successfully and no crash on start
- ![first build](https://user-images.githubusercontent.com/26512984/205422148-7c0f9b19-0379-4692-9f93-a02d6950da7d.png)

### 4. Rename packages 

- Reference: https://github.com/junedomingo/react-native-rename/pull/163

```bash
# Move to home directory and clone here.
cd ~

git@github.com:leegeunhyeok/react-native-rename.git && cd react-native-rename
git checkout feat/support-newarchitecture
npm install && npm run build
npm install -g . 

# Move to RN project
cd YOUR_REACT_NATIVE_PROJECT_PATH
react-native-rename "Rename" -b com.test.rename
```

### 5. Rebuild

```bash
# using `--active-arch-only` flag for reduce build time
yarn android --active-arch-only
```
- It also no crash on start
