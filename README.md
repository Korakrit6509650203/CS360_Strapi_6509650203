1.อธิบาย Strapi ใน README จากความเข้าใจที่ได้จากการศึกษา
    -เป็นเว็บแอพที่ใช้ในการพัฒนาแอพพลิเคชันที่มีระบบจัดการเนื้อหา (Content Management System หรือ CMS) ที่ยืดหยุ่น ใช้งานง่าย ซึ่งช่วยให้การสร้าง จัดการเนื้อหาบนเว็บ และแอพพลิเคชันต่าง ๆ เป็นเรื่องง่ายขึ้น
    -ความยืดหยุ่น: เนื่องจากเป็น Open Source และใช้ Node.js คุณจึงสามารถปรับแต่งได้ตามความต้องการ
    -ใช้งานง่าย: มี UI ที่เป็นมิตรกับผู้ใช้ และไม่ต้องมีความรู้เชิงลึกเกี่ยวกับการเขียนโปรแกรมเพื่อใช้งาน
    -รองรับการสเกล: สามารถรองรับการขยายตัวได้ดีทำให้เหมาะสำหรับโปรเจคขนาดใหญ่

2.ขั้นตอนการติดตั้ง และนําขึ้นให้บริการโดยใช้ Linux CLI
    -ดูขั้นตอนการติดตั้งผ่านเว็บไซต์ https://docs.strapi.io/dev-docs/installation/cli
    -เริ่มด้วยการพิมพ์ npx create-strapi-app@latest my-project ใน CMD
    -หลังจากนั้น เลือก Quickstart(recommended) ซึ่งค่าเริ่มต้นคือ SQLite DB
    -หลังจากนั้น เลือก skip และรอจนกว่าจะโหลดไฟล์เสร็จ
    -โหลดเสร็จแล้ว strapi จะถูกรันขึ้นหน้าเว็บแอพลิเคชั่น Strapi บนเครื่อง Local ซึ่งไฟล์จะถูกเก็บใน ไดร์ฟ C:\Users\ชื่อหลักในคอม\my-project

3.ความเข้าใจเกี่ยวกับ .gitignore ใน README
    -เป็นไฟล์ที่ใช้ในการควบคุมระบบเวอร์ชัน Git เพื่อบอกให้ Git รู้ว่าควรละเว้น/ไม่สนใจ(ignore) ไฟล์ หรือไดเรกทอรีบางอย่าง
    จากการติดตามการเปลี่ยนแปลง หรือการจัดเก็บใน repository ใน git

4.การใช้ Git
    -ไปที่ https://github.com/ชื่อ git ของตนเอง
    -สร้าง repository ใหม่ อาจตั้งชื่อว่า CS360_Strapi_เลขนักศึกษา
    -กดเลือกสร้างไฟล์ README.md ด้วย
    -จากนั้นเข้าแอพลิเคชั่น gitHub Desktop
    -Login เข้าสู่ระบบรหัสเดียวกับบน web git ให้เรียบร้อย
    -จากนั้นเลือก git clone จาก Repository ของตนที่เพิ่งสร้างขึ้นมา ในที่นี้คือ CS360_Strapi_เลขนักศึกษา
    -จากนั้นกด Show in Explorer หรือคีย์ลัดคือ Ctrl + Shift + F
    -จากนั้น copy โค้ด และโฟลเดอร์ของ Strapi มาใส่ในโฟล์เดอร์ที่เพิ่งเปิดมา
    -จากนั้นกลับมาที่ gitHub Desktop แล้วพิมพ์ข้อความว่านำ Source code Strapi ขึ้น git ตรง Summary(required)
    -จากนั้นกด Commit to main
    -แล้วกด Push origin นำสิ่งที่แก้ไขขึ้นไปบน https://github.com/ชื่อ git ของตนเอง ต่อไป

5.การนําเว็บแอปพลิเคชัน Strapi ขึ้นให้บริการบน AWS EC2 และการสาธิตการเข้าใช้งานกับ TA
    -เข้าเว็บไซต์ https://ap-southeast-2.console.aws.amazon.com/ec2 และทำการ Login เข้าสู่ระบบของตนให้เรียบร้อย
    -กด Instances จากแถบด้านซ้ายของเว็บไซต์
    -กดสร้าง Launch an instance ใหม่ อาจตั้งชื่อ My Linux Server
    -เลือก Instance type ตัวที่มี CPU ตั้งแต่ 2 ตัวขึ้นไป เพื่อให้สามารถ run code Strapi ได้รวดเร็วขึ้น
    -ตั้งชื่อ Key pair (login) เป็นอะไรก็ได้
    -กำหนด Configure storage เป็น 32 GiB gp3
    -ส่วนที่เหลือให้เลือกตาม Default ที่เว็บกำหนดมาได้เลย
    -และหลังจากนั้นกดสร้าง Launch instance ได้เลย
    -จากนั้นกดเข้าไปที่ Instance ID จากเครื่อง EC2 ที่เพิ่งสร้างเมื่อกี้นี้
    -จากนั้นเลื่อนลงมากดแถบ Security
    -จากนั้นกดเข้าไป Security groups
    -จากนั้นเลื่อนลงมากด Edit inbound rules
    -จากนั้นกด Add rule เปลี่ยน Port range เป็น 1337 และเพิ่ม CIDR blocks เป็น Anywhere 0.0.0.0/0
    -และอย่าลืมที่จะกด Save rules
    -จากนั้นกดกลับมาหน้า Instances และกดเข้าไปที่ Instance ID จากเครื่อง EC2 ที่เพิ่งสร้าง
    -จากนั้นกด Connect
    -เลือกกดแถบ SSH client
    -กด copy source code ที่ Example: ssh -i "ชื่อ Key pair ที่ตั้งขึ้น.pem" ec2-user@ec2-3-27-221-154.ap-southeast-2.compute.amazonaws.com
    -จากนั้นเข้า Command Line ไปโฟลเดอร์ที่มีคีย์ Key pair ในการ Login เข้าสู่ระบบ
    -จากนั้น paste source code ที่ copy มาลงไป
    -เมื่อเข้าสู่เครื่อง AWS EC2 แล้วให้ทำการ setup ตามสไลด์เรียนในคาบ https://drive.google.com/file/d/1ieGH-FQt0AlVNogiEq1nPOEEOuupgr-I/view
   
   ++Installing Node.js and Git on CentOS/RHEL-based Systems
    -Step 1: Update the System
        sudo yum update -y
    -Step 2: Install Node.js
        ● First, install the required build tools:
            sudo yum groupinstall 'Development Tools' -y
        ● Then, install Node.js:
            curl -fsSL https://rpm.nodesource.com/setup_20.x | sudo bash -
            sudo yum install -y nsolid
    -Step 3: Verify Node.js Installation
        node -v
        npm -v
    -Step 4: Install Git
        sudo yum install -y git
    -Step 5: Verify Git Installation
        git --version

   ++Setting up a Node.js project
    -Step 1: Create a new directory for your project
        mkdir simple-node-app
        cd simple-node-app
    -Step 2: Initialize a Node.js project
        npm init -y
        This command creates a package.json file with default settings.
    -Step 3: Create a new file named app.js
        nano app.js
    -Step 4: Add the following code in app.js
        const http = require('http');

        const server = http.createServer((req, res) => {
        res.statusCode = 200;
        res.setHeader('Content-Type', 'text/plain');
        res.end('Hello, World!\n');
        });
        
        const PORT = process.env.PORT || 3000;
        server.listen(PORT, () => {
        console.log(`Server running at http://localhost:${PORT}/`);
        });
    -Step 5: Run the application to verify it works
        node app.js
    -Step 6: Since there's no GUI, use curl in another terminal to test the server
        curl http://localhost:3000
        You should see the output: Hello, World!
        Stop the server with Ctrl + C.
    
   ++Git repo setup and workflow
    -Step 1: Initialize a new Git repository in your project directory
        git init
        This creates a hidden .git directory, indicating that Git is now
        tracking changes in your project.
    -Step 2: Check the status of your repository
        git status
        You should see that app.js and package.json are untracked files.
    -Step 3: Stage all files for the first commit
        git add .
    -Step 4: Commit the staged files
        git commit -m "Initial commit: Add Node.js web server"
    -Step 5: Check the commit history
        git log
        You should see your initial commit listed.
    -Step 6: Modify app.js to change the message
        res.end('Hello, Git from EC2!\n');
    -Step 7: Check the status of your repository
        git status
        Git will show that app.js has been modified.
    -Step 8: Stage and commit the change
        git add app.js
        git commit -m "Update message in app.js"
    -Step 9: View the commit history
        git log
        You should see both commits in the history.
        At this point, students should have a functioning Git repository on their EC2 instance containing a simple Node.js web application with a few commits that track changes in the application.

   ++Run the Node.js application in the background
    -Step 1: Install pm2 to manage the Node.js process
        sudo npm install -g pm2
    -Step 2: Start the application with pm2
        pm2 start app.js
    -Step 3: Save the pm2 process list so it starts on reboot
        pm2 save
        pm2 startup
    -Step 4: Stop the Web server with pm2
        pm2 stop app.js
    
   ++Modify the server to be publicly accessible
    -Step 1: Update app.js to listen on all network interfaces
        server.listen(PORT, '0.0.0.0', () => {
        console.log(`Server running at http://localhost:${PORT}/`);
        });
    -Step 2: Modify the Security Group of your EC2 instance to allow traffic into the PORT

    -หลังจากทำการ set up เบื้องต้นเสร็จไปแล้ว ให้พิมพ์ git clone https://github.com/ชื่อ git/ชื่อ repository
    -cd เข้าไปในโฟลเดอร์นั้น
    -พิมพ์ npm run develop
    -หลังจากนั้นก็รอสร้างไฟล์เว็บแอพลิเคชั่น Strapi เสร็จ
    -จากนั้นเข้า Google พิมพ์ http://3.27.221.154:1337 ก็จะขึ้นเว็บแอพลิเคชั่น Strapi เรียบร้อย
    
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
