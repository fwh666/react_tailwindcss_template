# 安装
1、通过vite创建react项目

yarn create vite react-project --template react-ts
2、初始化Tailwind CSS

yarn add -D tailwindcss postcss autoprefixer
npx tailwindcss init -p

3、在生成的tailwind.config.js文件中，添加

module.exports = {
  content: [
    "./index.html",
    "./src/**/*.{vue,js,ts,jsx,tsx}", // 用到tailwind的地方
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
4、在./src/index.css中添加（注意，该文件必须导入到main.tsx中）

@tailwind base;
@tailwind components;
@tailwind utilities;

5、编写Html

<h1 class="text-3xl font-bold underline">
    Hello world!
</h1>

6、运行yarn dev，能够看到黑色加粗带下划线的Hello World!.