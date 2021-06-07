# Uploading files & images

**Error:**

```text
radiopanel-api | [Nest] 1   - 06/07/2021, 8:13:53 PM   [ExceptionsHandler] EACCES: permission denied, open '/home/node/uploads/0f37081b-97ad-4aeb-a844-b1640e0c3205.png' +200447ms
radiopanel-api | Error: EACCES: permission denied, open '/home/node/uploads/0f37081b-97ad-4aeb-a844-b1640e0c3205.png'
radiopanel-api |     at Object.openSync (fs.js:462:3)
radiopanel-api |     at Object.writeFileSync (fs.js:1384:35)
radiopanel-api |     at StorageController.upload (/home/node/dist/src/modules/storage/controllers/storage.controller.js:59:26)
radiopanel-api |     at /home/node/node_modules/@nestjs/core/router/router-execution-context.js:37:29
radiopanel-api |     at processTicksAndRejections (internal/process/task_queues.js:97:5)
radiopanel-app | 179.43.169.181 - - [07/Jun/2021:20:14:10 +0000] "GET / HTTP/1.1" 200 2411 "-" "Mozilla/5.0 (X11; Linux i686; rv:10.0) Gecko/20100101 Firefox/10.0"
```

**Solution:**

Make sure your `uploads` directory has the correct permissions, assign ownership of the folder to your docker user & group or if you're just running a development environment you can use`chmod -R 777 uploads`

