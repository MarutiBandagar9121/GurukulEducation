

## 🧞 Commands

All commands are run from the root of the project, from a terminal:

| Command                   | Action                                           |
| :------------------------ | :----------------------------------------------- |
| `npm install`             | Installs dependencies                            |
| `npm run dev`             | Starts local dev server at `localhost:4321`      |
| `npm run build`           | Build your production site to `./dist/`          |
| `npm run preview`         | Preview your build locally, before deploying     |
| `npm run astro ...`       | Run CLI commands like `astro add`, `astro check` |
| `npm run astro -- --help` | Get help using the Astro CLI                     |

## 👀 Want to learn more?

Feel free to check [our documentation](https://docs.astro.build) or jump into our [Discord server](https://astro.build/chat).

ip:147.93.97.164
ssh -i "C:\maruti\static\sshFiles-gurukul\ssh_gurukul.ppk" root@147.93.97.164
Root pass: MarutiBandagar9121@
paraphrase: MarutiBandagar

certbot certonly --webroot -w /var/www/html/ -d gurukuleducation.org -d www.gurukuleducation.org

admin interface=domain:7080
username:admin
cat .litespeed_password
ufw allow from 192.0.2.0 to any port 7080
ufw allow 7080 all ip
ufw delete allow 7080
admin_pass=NgBHUidWzGkCYClj
dist path: usr/local/lsws/gurukul/html/astro

astro add nodejs
npm run build
node ./dist/server/entry.mjs


/usr/local/lsws/Example/html/node/app.js
/usr/local/lsws/Example/html/node/


setup server
mkdir /usr/local/lsws/gurukul
mkdir /usr/local/lsws/gurukul/{conf,html,logs}
chown lsadm:lsadm /usr/local/lsws/gurukul/conf


using pm2 process manager



root@srv693688:/usr/local/lsws/gurukul/html/astro/dist/server# cat entry.mjs
import { renderers } from './renderers.mjs';
import { c as createExports, s as serverEntrypointModule } from './chunks/_@astrojs-ssr-adapter_D3THNE1z.mjs';
import { manifest } from './manifest_DBWBWgFW.mjs';

const serverIslandMap = new Map();

const _page0 = () => import('./pages/aboutus.astro.mjs');
const _page1 = () => import('./pages/contactus.astro.mjs');
const _page2 = () => import('./pages/faq.astro.mjs');
const _page3 = () => import('./pages/gallery.astro.mjs');
const _page4 = () => import('./pages/services.astro.mjs');
const _page5 = () => import('./pages/testimonials.astro.mjs');
const _page6 = () => import('./pages/videosgallery.astro.mjs');
const _page7 = () => import('./pages/index.astro.mjs');
const pageMap = new Map([
    ["src/pages/aboutus.astro", _page0],
    ["src/pages/contactus.astro", _page1],
    ["src/pages/faq.astro", _page2],
    ["src/pages/gallery.astro", _page3],
    ["src/pages/services.astro", _page4],
    ["src/pages/testimonials.astro", _page5],
    ["src/pages/videosgallery.astro", _page6],
    ["src/pages/index.astro", _page7]
]);

const _manifest = Object.assign(manifest, {
    pageMap,
    serverIslandMap,
    renderers,
    middleware: () => import('./_noop-middleware.mjs')
});
const _args = {
    "mode": "standalone",
    "client": "file:///usr/local/lsws/gurukul/html/astro/dist/client/",
    "server": "file:///usr/local/lsws/gurukul/html/astro/dist/server/",
    "host": true,
    "port": 3000,
    "assets": "_astro"
};
const _exports = createExports(_manifest, _args);
const handler = _exports['handler'];
const startServer = _exports['startServer'];
const options = _exports['options'];
const _start = 'start';
if (_start in serverEntrypointModule) {
        serverEntrypointModule[_start](_manifest, _args);
}

export { handler, options, pageMap, startServer };

Running the server: node dist\server\entry.mjs