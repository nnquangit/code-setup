# Javascript setup

### Typescript
```
npm i -g typescript

--- project ---
tsc --init
```

### Eslint
```
npm init @eslint/config

--- project ---
npm i eslint -S
```

### Prettier
```
npm install -g prettier

--- project ---
npx prettier-init
```

### Eslint & Prettier
```
npm install -g eslint

--- project ---
npm init @eslint/config
npm install --save-dev prettier eslint-config-prettier eslint-plugin-prettier

--- eslintrc file ---
{
  extends: ["prettier"],
  plugins: ["prettier"],
  rules: {
    "prettier/prettier": ["error"]
  },
}
```

### Eslint & Typescript
```

--- project ---
npm i eslint-config-airbnb-typescript -S
npm i @typescript-eslint/eslint-plugin -S
npm i @typescript-eslint/parser -S

--- eslintrc file ---
{
  extends: ["airbnb","airbnb-typescript"],
  extends: ["airbnb-base","airbnb-typescript/base"], //with out react
  parserOptions: {
    tsconfigRootDir: __dirname,
    project: './tsconfig.json'
  }
}
```
