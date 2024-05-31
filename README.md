# 使い方

```
git clone https://github.com/k1350/hugo-microcms-sample.git
cd hugo-microcms-sample
git submodule update -i
```

content/post/_content.gotmpl の下記の値を置換する。

- `PUT_YOUR_SERVICE_ID`: 使用する microCMS のサービスID
- `PUT_YOUR_ARTICLE_ENDPOINT_NAME`: 使用する記事のAPI名
- `PUT_YOUR_API_KEY`: microCMS の APIキー

```
hugo server
```

## このリポジトリで前提としているAPIスキーマ

### articles

```json
{
    "apiFields": [
        {
            "idValue": "lrk4WAjnR8",
            "fieldId": "title",
            "name": "タイトル",
            "kind": "text",
            "required": true,
            "isUnique": false
        },
        {
            "fieldId": "content",
            "name": "内容",
            "kind": "richEditorV2",
            "required": true
        },
        {
            "fieldId": "tags",
            "name": "Tags",
            "kind": "relationList"
        },
        {
            "fieldId": "coverImage",
            "name": "カバーイメージ",
            "kind": "media"
        }
    ],
    "customFields": []
}
```

### tags

```json
{
    "apiFields": [
        {
            "idValue": "iGhXhpUpAy",
            "fieldId": "name",
            "name": "タグ名",
            "kind": "text",
            "isUnique": true
        }
    ],
    "customFields": []
}
```
