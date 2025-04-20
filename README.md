# experiment-strapi

1.
```
npx create-strapi-app@latest experiment-strapi
```


## [日本語化](https://github.com/yasudacloud/strapi-plugin-ja-pack?tab=readme-ov-file#%E3%82%BB%E3%83%83%E3%83%88%E3%82%A2%E3%83%83%E3%83%97)

1.
```
experiment-strapi/src/admin/app.example.tsx
```

2.
```
yarn add strapi-plugin-ja-pack
```

```ts
// experiment-strapi/config/plugins.ts
export default ({env}) => ({
    i18n: true,
    'strapi-plugin-ja-pack': {
        enabled: true,
    }
});
```

```tsx
// experiment-strapi/src/admin/app.tsx
import type { StrapiApp } from '@strapi/strapi/admin';

export default {
config: {
    locales: [
        'ja'
    ],
},
bootstrap(app: StrapiApp) {
    console.log(app);
    },
};
```

3.
```
npm run build
npm run develop
```


