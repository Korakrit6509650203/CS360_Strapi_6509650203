1.การอธิบาย Strapi ใน README จากความเข้าใจที่ได้จากการศึกษา


2.ขั้นตอนการติดตั้ง และนําขึ้นให้บริการโดยใช้ Linux CLI
    -ดูขั้นตอนการติดตั้งผ่านเว็บไซต์ https://docs.strapi.io/dev-docs/installation/cli
    -เริ่มด้วยการพิมพ์ npx create-strapi-app@latest my-project ใน CMD
    -หลังจากนั้น เลือก Quickstart(recommended) ซึ่งค่าเริ่มต้นคือ SQLite DB
    -หลังจากนั้น เลือก skip และรอจนกว่าจะโหลดไฟล์เสร็จ
    -โหลดเสร็จแล้ว strapi จะถูกรันขึ้นหน้าเว็บแอพลิเคชั่น Strapi บนเครื่อง Local ซึ่งไฟล์จะถูกเก็บใน ไดร์ฟ C:\Users\ชื่อหลักในคอม\my-project
    -จากนั้นไปที่ https://github.com/ชื่อ git ของตนเอง
    -สร้าง repository ใหม่ อาจตั้งชื่อว่า CS360_Strapi_เลขนักศึกษา
    -กดเลือกสร้างไฟล์ README.md ด้วย
    -จากนั้นเข้าแอพลิเคชั่น gitHub Desktop
    -Login เข้าสู่ระบบรหัสเดียวกับบน web git ให้เรียบร้อย
    -จากนั้นเลือก git clone จาก Repository ของตนที่เพิ่งสร้างขึ้นมา ในที่นี้คือ CS360_Strapi_เลขนักศึกษา
    -จากนั้นกด Show in Explorer หรือคีย์ลัดคือ Ctrl + Shift + F
    -จากนั้น copy โค้ด และโฟลเดอร์ของ Strapi มาใส่ในโฟล์เดอร์ที่เพิ่งเปิดมา
    -จากนั้นกลับมาที่ gitHub Desktop แล้วพิมพ์ข้อความว่านำ Source code Strapi ขึ้น git ตรง Summary(required)
    -จากนั้นกด Commit to main
    -และกด pull
3.ความเข้าใจเกี่ยวกับ .gitignore ใน README
    -เป็นไฟล์ที่ใช้ในการควบคุมระบบเวอร์ชัน Git เพื่อบอกให้ Git รู้ว่าควรละเว้น/ไม่สนใจ(ignore) ไฟล์ หรือไดเรกทอรีบางอย่าง
    จากการติดตามการเปลี่ยนแปลง หรือการจัดเก็บใน repository ใน git

4.การนําเว็บแอปพลิเคชัน Strapi ขึ้นให้บริการบน AWS EC2 และการสาธิตการเข้าใช้งานกับ TA

5.การใช้ Git




# 🚀 Getting started with Strapi

Strapi comes with a full featured [Command Line Interface](https://docs.strapi.io/dev-docs/cli) (CLI) which lets you scaffold and manage your project in seconds.

### `develop`

Start your Strapi application with autoReload enabled. [Learn more](https://docs.strapi.io/dev-docs/cli#strapi-develop)

```
npm run develop
# or
yarn develop
```

### `start`

Start your Strapi application with autoReload disabled. [Learn more](https://docs.strapi.io/dev-docs/cli#strapi-start)

```
npm run start
# or
yarn start
```

### `build`

Build your admin panel. [Learn more](https://docs.strapi.io/dev-docs/cli#strapi-build)

```
npm run build
# or
yarn build
```

## ⚙️ Deployment

Strapi gives you many possible deployment options for your project including [Strapi Cloud](https://cloud.strapi.io). Browse the [deployment section of the documentation](https://docs.strapi.io/dev-docs/deployment) to find the best solution for your use case.

```
yarn strapi deploy
```

## 📚 Learn more

- [Resource center](https://strapi.io/resource-center) - Strapi resource center.
- [Strapi documentation](https://docs.strapi.io) - Official Strapi documentation.
- [Strapi tutorials](https://strapi.io/tutorials) - List of tutorials made by the core team and the community.
- [Strapi blog](https://strapi.io/blog) - Official Strapi blog containing articles made by the Strapi team and the community.
- [Changelog](https://strapi.io/changelog) - Find out about the Strapi product updates, new features and general improvements.

Feel free to check out the [Strapi GitHub repository](https://github.com/strapi/strapi). Your feedback and contributions are welcome!

## ✨ Community

- [Discord](https://discord.strapi.io) - Come chat with the Strapi community including the core team.
- [Forum](https://forum.strapi.io/) - Place to discuss, ask questions and find answers, show your Strapi project and get feedback or just talk with other Community members.
- [Awesome Strapi](https://github.com/strapi/awesome-strapi) - A curated list of awesome things related to Strapi.

---

<sub>🤫 Psst! [Strapi is hiring](https://strapi.io/careers).</sub>
