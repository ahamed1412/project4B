# 🎥 Project 4B – Adaptive Bitrate OTT Streaming with AWS

This project demonstrates how to build a **real-time Adaptive Bitrate (ABR) streaming solution** using AWS MediaConvert, CloudFront, and S3 – similar to how OTT platforms deliver scalable, efficient video content.

---

## ✅ Objective

Create a private video streaming pipeline that delivers multiple quality renditions (360p, 480p, 720p) via HLS, and verify bitrate switching based on network conditions.

---

## 🛠️ Technologies Used

- **Amazon S3** – Secure storage for video input/output
- **AWS MediaConvert** – Transcoded MP4 into HLS with automated ABR
- **Amazon CloudFront** – Content delivery with low latency
- **Origin Access Control (OAC)** – Secures S3 access
- **Video.js** – HTML5 video player with bitrate/resolution overlay
- **Browser DevTools** – Verified rendition switching in real time

---

## 🔁 Workflow

1. 🎞️ Upload `ABRsample.mp4` to a private S3 bucket
2. ⚙️ Run MediaConvert (Automated ABR) → outputs HLS in `/output/`
3. 🌐 Create CloudFront distribution (Origin path = `/output`)
4. 🔐 Configure S3 bucket policy for CloudFront OAC access
5. 🎥 Embed `master.m3u8` into a custom Video.js player
6. 📉 Throttle bandwidth and observe adaptive streaming behavior

---

## 📸 Screenshots

| Screenshot | Description |
|------------|-------------|
| `network_tab_switching.png` | DevTools showing multiple `.m3u8` requests |
| `cloudfront_settings.png` | CloudFront + OAC configuration |
| `bucket_policy.png` | Correct S3 permissions with distribution ARN |

---

## 🔗 Demo Link

[Play the Adaptive Stream](https://d24wb5ukanl8mz.cloudfront.net/index.html)



