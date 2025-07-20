# 🪟 Installing ZIN on Windows

Follow these steps to get started with ZIN Engine on a Windows system.

## 📥 Step 1: Download the ZIP

1. Go to the [Releases page](https://github.com/zin-engine/zin-engine/releases)
2. Download the latest **`.zip`** file for Windows
3. Extract the ZIP to a desired location (for example: `C:/zin-engine`)

After extraction, the folder will look like this:

```

C:/zin-engine/
├── zin.exe
├── favicon.ico
└── public/
├── assets/
└── views/

```

## 🛠 Step 2: Add ZIN to Your System PATH

To run `zin` from any folder in Command Prompt:

1. Press `Windows + R`, type `sysdm.cpl`, and hit **Enter**
2. In the System Properties window:
   - Go to the **Advanced** tab
   - Click **Environment Variables**
3. Under **System variables**, select `Path` and click **Edit**
4. Click **New**, and add the folder path where `zin.exe` is extracted  
   _(e.g. `C:\zin-engine`)_
5. Click **OK** on all windows to save

Now, you can run `zin` from **any folder** in CMD ✨

## 🚀 Step 3: Run ZIN

Let's say you're working on a site at:

```

E:/projects/my-demo-site/

````

To start the ZIN engine here:

### ✅ Method 1 (Recommended)

1. Open **Command Prompt**
2. Change to your project folder:
3. 
```sh
   cd E:\projects\my-demo-site
````

3. Run ZIN:

 ```sh
 zin
 ```

🔹 This will start the server at:
`http://localhost:9001`


### ⚙️ Method 2 (Manual full command)

If you didn't add ZIN to your system PATH, or want more control:

Open CMD and run:

```sh
C:\zin-engine\zin.exe -p 3001 -r "E:/projects/my-demo-site"
```

🔸 This will start ZIN manually on port 3001 and point it to your project folder.



## 🧪 Verify Setup

Once ZIN is running, open a browser and go to:

```
http://localhost:9001
```

You should see your website loading!


## ✅ What’s Next?

* [Create your first ZIN webpage →](../MyWebPage.md)
* [Understand ZIN tags and features →](../Tags/)


Need help? Open an [issue](https://github.com/zin-engine/zin-engine/issues) or reach out in the community.
