<p align="center"><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/logo.svg"/></a><br/><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/xxai.svg"/></a></p><p align="center"><a href="https://github.com/xxai-art/doc#readme"><img alt="I18N" src="https://cdn.jsdelivr.net/gh/wactax/img/t.svg"/></a>　<a href="https://groups.google.com/u/0/g/xxai-art"><img alt="Google Groups" src="https://cdn.jsdelivr.net/gh/wactax/img/g-groups.svg"/></a></p>

دا سپارښتنه کیږي چې لومړی نوډز، [direnv](https://direnv.net) ، [bun](https://github.com/oven-sh/bun) نصب کړئ، او بیا `direnv allow` ( [. envrc](https://github.com/xxai-art/doc/blob/main/.envrc) به ډایرکټر ته د ننوتلو وروسته په اتوماتيک ډول اجرا شي).

معنی دا ده: چینایي ژباړه جاپاني، کوریايي، انګلیسي، نورو ټولو ژبو ته انګلیسي ژباړه. که تاسو یوازې د چینایي او انګلیسي ملاتړ کول غواړئ، تاسو کولی شئ یوازې `zh: en` ولیکئ.

معنی دا ده: چینایي ژباړه جاپاني، کوریايي، انګلیسي، نورو ټولو ژبو ته انګلیسي ژباړه. که تاسو یوازې د چینایي او انګلیسي ملاتړ کول غواړئ، تاسو کولی شئ یوازې `zh: en` ولیکئ.

* [مخکینۍ کوډ](https://github.com/xxai-art/web)
* [په ټوله کې د سایټ لپاره د ژبې پیک](https://github.com/xxai-art/web/tree/main/i18n)
* [د ننوتلو ماډلونو لپاره د ژبې کڅوړې](https://github.com/wacpkg/user/tree/main/ui.i18n)
* [د ویب پاڼې څو ژبني اسناد](https://github.com/xxai-doc)

د مخکښې پای پروګرام کولو ژبه [@w5/coffee_plus](http://npmjs.com/@w5/coffee_plus) ده، کوم چې د کافي سکریپټ ترکیب پر بنسټ ځینې ځانګړتیاوې اضافه کوي، وګورئ [./coffee_plus.md](./coffee_plus.md) .

## د ویب پاڼو او اسنادو نړیوال کول

په لاندې 3 پروژو کې جوړ کړئ

* [@w5/mdt](https://www.npmjs.com/package/@w5/mdt)

  لاحقه `.mdt` ده، تاسو کولی شئ د `<+ ./coffee_plus/import.js>` سره ورته نحو څخه کار واخلئ ترڅو خارجي فایلونو ته مراجعه وکړئ، او د ضمیمې سره مارک ډاون پیدا کړئ `.md` .

* [@w5/trmd](https://www.npmjs.com/package/@w5/trmd)

  د مارک ډاون ژباړه به کوډونه او لینکونه ونه ژباړي، او ژباړل شوي جملې به خوندي کړي. که ژباړه تعدیل شوې وي مګر اصلي متن نه وي بدل شوی، د بیا پلي کولو سره به د ژباړې تعدیل له پامه ونه غورځول شي.

* [@w5/i18n](https://www.npmjs.com/package/@w5/i18n)

  `yaml` تولید شوي ویب پاڼې ژباړلو لپاره د ژبې فایلونه.

### د سند ژباړې اتومات لارښوونې

د کوډ ذخیره وګورئ [xxai-art/doc](https://github.com/xxai-art/doc)

دا سپارښتنه کیږي چې لومړی نوډز، [direnv](https://direnv.net) ، [bun](https://github.com/oven-sh/bun) نصب کړئ، او بیا `direnv allow` ( [. envrc](https://github.com/xxai-art/doc/blob/main/.envrc) به ډایرکټر ته د ننوتلو وروسته په اتوماتيک ډول اجرا شي).

په سلګونو ژبو ته د ژباړل شوي لوی کوډ بیس څخه د مخنیوي لپاره، ما د هرې ژبې لپاره جلا کوډ بیس جوړ کړ او د کوډ بیس ذخیره کولو لپاره ما یو سازمان جوړ کړ.

د چاپیریال متغیر `GITHUB_ACCESS_TOKEN` تنظیم کول او بیا [د create.github.coffee](https://github.com/xxai-art/doc/blob/main/create.github.coffee) چلول به په اوتومات ډول د کوډ ذخیره رامینځته کړي.

البته، تاسو کولی شئ دا د کوډ بیس کې هم واچوئ.

د ژباړې سکریپټ حواله [run.sh](https://github.com/xxai-art/doc/blob/main/run.sh)

د سکریپټ کوډ په لاندې ډول تشریح شوی:

[بنکس](https://bun.sh/docs/cli/bunx) د npx لپاره بدیل دی، کوم چې چټک دی. البته، که تاسو بن نصب نلرئ، تاسو کولی شئ د دې پرځای `npx` وکاروئ.

`bunx mdt zh` `.mdt` په zh ډایرکټر کې `.md` په توګه وړاندې کوي، لاندې 2 تړل شوي فایلونه وګورئ

* [coffee_plus.mdt](https://github.com/xxai-doc/zh/blob/main/coffee_plus.mdt)
* [coffee_plus.md](https://github.com/xxai-doc/zh/blob/main/coffee_plus.md)

`bunx i18n` د ژباړې لپاره اصلي کوډ دی (که تاسو یوازې `nodejs` نصب کړی وي ، مګر `bun` او `direnv` ندي نصب شوي ، تاسو کولی شئ د ژباړې لپاره `npx i18n` هم چلولی شئ).

دا به [i18n.yml](https://github.com/xxai-art/doc/blob/main/i18n.yml) پارس کړي، په دې سند کې د `i18n.yml` ترتیب په لاندې ډول دی:

```
en:
zh: ja ko en
```

معنی دا ده: چینایي ژباړه جاپاني، کوریايي، انګلیسي، نورو ټولو ژبو ته انګلیسي ژباړه. که تاسو یوازې د چینایي او انګلیسي ملاتړ کول غواړئ، تاسو کولی شئ یوازې `zh: en` ولیکئ.

وروستی یې [gen.README.coffee](https://github.com/xxai-art/doc/blob/main/gen.README.coffee) دی، کوم چې د اصلي سرلیک او د هرې ژبې د `README.md` د لومړي فرعي سرلیک تر مینځ مینځپانګې استخراج کوي ترڅو `README.md` ننوتل پیدا کړي. کوډ خورا ساده دی، تاسو کولی شئ دا پخپله وګورئ.

ګوګل API د وړیا ژباړې لپاره کارول کیږي. که تاسو ګوګل ته لاسرسی نشئ کولی، مهرباني وکړئ یو پراکسي ترتیب او تنظیم کړئ، لکه:

```
export https_proxy=http://127.0.0.1:7890 http_proxy=http://127.0.0.1:7890 all_proxy=socks5://127.0.0.1:7890
```

د ژباړې سکریپټ به په `.i18n` ډایرکټر کې ژباړل شوي کیچ رامینځته کړي ، مهرباني وکړئ دا `git status` سره وګورئ او د کوډ ذخیره کې یې اضافه کړئ ترڅو د تکرار ژباړې مخه ونیول شي.

مهرباني وکړئ هرکله چې تاسو د کیچ تازه کولو لپاره ژباړه تعدیل کړئ `bunx i18n` چل کړئ.

که اصلي متن او ژباړه په ورته وخت کې تعدیل شي، کیچ به ګډوډ شي، نو که تاسو غواړئ تعدیل کړئ، تاسو کولی شئ یوازې یو تعدیل کړئ، او بیا د کیچ تازه کولو لپاره `bunx i18n` چل کړئ.
