# Laboratory 7 Command Checklist

Run these commands in KillerCoda in order.

## 1. Host baseline

```bash
free -h
df -h /
top
```

Press `q` to exit `top`.

## 2. Create and start Nginx

```bash
docker run -d --name client-website -p 8080:80 nginx
```

Verify that it is running:

```bash
docker ps
```

## 3. Generate traffic

```bash
curl http://localhost:8080
curl http://localhost:8080
curl http://localhost:8080
curl http://localhost:8080/hidden-admin-page
```

## 4. View logs

```bash
docker logs client-website
```

Look for three `200` responses and one `404` response.

## 5. View metrics

```bash
docker stats
```

Record the exact CPU percentage and memory usage shown for `client-website`. Press `Ctrl+C` to stop the live display.

## 6. Git setup

From the root of your existing repository:

```bash
mkdir -p Laboratory-07-Cloud-Operations-Engineer/screenshots
cd Laboratory-07-Cloud-Operations-Engineer
touch README.md system-baseline-report.md container-observability.md reflection.md
```

After adding your screenshots and Markdown files:

```bash
cd ..
git add Laboratory-07-Cloud-Operations-Engineer
git commit -m "Complete Laboratory Activity 7 - Cloud Operations Engineer"
git push
```
