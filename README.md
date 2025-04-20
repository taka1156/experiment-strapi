# experiment-strapi

1.
```
npx create-strapi-app experiment-strapi --quickstart
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

コマンド一覧
| **コマンド**         | **実行方法**                          | **説明**                                                                                     |
|----------------------|---------------------------------------|---------------------------------------------------------------------------------------------|
| **build**           | `strapi build`                       | プロジェクトをビルドし、プロダクション用の静的アセットを生成します。                          |
| **console**         | `strapi console`                     | インタラクティブなコンソールを開いてリアルタイムで内部操作やデバッグを行います。                |
| **deploy**          | `strapi deploy`                      | カスタムのデプロイメント処理を実行します。                                                   |
| **dev / develop**   | `strapi develop` または `strapi dev` | 開発モードで起動し、ホットリロードが有効化されます。                                         |
| **start**           | `strapi start`                       | プロダクションモードで起動し、ビルド済みファイルを使用して効率的に動作します。                |
| **strapi**          | `strapi`                             | Strapi CLI の入口点。利用可能なコマンドを一覧表示します。                                     |
| **upgrade**         | `npx @strapi/upgrade latest`         | Strapi を最新バージョンにアップグレードします。                                              |
| **upgrade:dry**     | `npx @strapi/upgrade latest --dry`   | アップグレードをシミュレートし、変更点を事前に確認します（実際のアップグレードは行わない）。 |
