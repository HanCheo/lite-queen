# Lite Queen - executable

## Dependencies

- [BunJS](https://bun.sh/docs/installation)
- [make-vfs – Used to embed the `_ui/out` Next.js static export into the binary](https://github.com/seveibar/make-vfs/tree/main)
- [swr – hooks for fetching data and syncing them in the client](https://swr.vercel.app/docs/getting-started)

## Development

The executable serves the statically exported UI bundle. Generate the bundle and copy it before running the server:

```bash
npm --prefix _ui run build
npm --prefix _ui run generate-static-bundle
cp _ui/static-ui-bundle.js executable/
npm --prefix executable run dev
```

