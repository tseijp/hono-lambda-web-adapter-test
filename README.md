# hono-lambda-web-adapter-test

## Quick start

```
git clone https://github.com/tseijp/hono-lambda-web-adapter-test
cd hono-lambda-web-adapter-test
sam build
sam deploy --guided
```

## Getting started

```
npm create hono@latest
# ? Target directory hono-lambda-web-adapter-test
# ? Which template do you want to use? nodejs
cd hono-lambda-web-adapter-test
npm i -D typescript
```

### The following steps shall be taken in advance.

- Add "outDir": "./dist" to the compilerOptions section tsconfig.json.
- Add "exclude": ["node_modules"] to tsconfig.json.
- Add "build": "tsc" to script section of package.json.
- Add "type": "module" to package.json.


### Deploy to lambda

before install docker and aws sam

```ruby
sam build
sam local invoke --region ap-northeast-1
sam deploy --guided
```

### Connect to CI/CD

```
echo dist >> .gitignore
echo 'samconfig.toml' >> .gitignore
echo '**/.aws-sam' >> .gitignore
sam pipeline init --bootstrap
git add .
git commit -m ":tada: init commit"
git push
```

> ```
> npm install
> npm run dev
> ```
> 
> ```
> open http://localhost:3000
> ```
