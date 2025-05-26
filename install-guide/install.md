# 🚀 Infra Automation Class: Fun Multi-OS Install Guide! 🤖

Welcome, infrastructure heroes! 🦸‍♂️🦸‍♀️

Today we're gearing up your system with the mission-critical tools to deploy apps like a pro. 💻✨

> **Note:** This guide is for **Linux** 🐧 and **macOS** 🍏 users. If you're on Windows... well, may the containers be ever in your favor! 🪟😂

---

## 🐳 Rancher Desktop (K8s v1.30.12)

**This will install your local Kubernetes powerhouse. ⚡️**

1. **Download Rancher Desktop:** [https://rancherdesktop.io](https://rancherdesktop.io) ⬇️
2. **Install & launch Rancher Desktop** 🚀
3. **Select Kubernetes version:** `v1.30.12` during setup ☸️
4. **Enable Admin access** to let Rancher manage your cluster resources 🔑

### Verify your setup ✅
Run these commands to check your installation:
```sh
docker --version
kubectl version
```
You should see Docker and Kubernetes version info. 🐳☸️

---
## 🐙 Set Up Your GitHub Account & Demo Repo (and log in to GHCR)

Before we dive into automation, let's get your GitHub ready for action!

1. **Create a GitHub account:** If you don't have one, sign up at [github.com](https://github.com/).
2. **Create a new demo repository:** This will be used for class exercises. Name it something fun!
3. **Install Git:**
   ```sh
   sudo apt-get install git   # Linux
   brew install git           # macOS
   ```
4. **Clone your new repo locally:**
   ```sh
   git clone https://github.com/<your-username>/<your-demo-repo>.git
   cd <your-demo-repo>
   ```
5. **Log in to GitHub Container Registry (GHCR):**
   - Generate a [GitHub Personal Access Token](https://github.com/settings/tokens?type=beta) with `write:packages` and `read:packages` permissions.
   - Save this token, you'll also need it later!
   - Log in with Docker:
     ```sh
     export CR_PAT=YOUR_TOKEN
     echo $CR_PAT | docker login ghcr.io -u <your-username> --password-stdin
     ```
   - This will let you push and pull container images later in the class!


> _Don't worry if this doesn't make sense yet—just get set up, and it will all click soon!_

---

## 🌍 Terraform CLI

**Terraform your infrastructure planet! 🌎**

1. **Install Terraform:** Follow the official guide: https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli 📦
2. **Verify installation:**
```sh
terraform -help
```
You should see the Terraform help output. 🏗️

---

# 🛠️ Troubleshooting Rancher Desktop Installation
- **Restart first:** If something's not working, try restarting Rancher Desktop and your computer. 🔄
- **Virtualization:** Ensure virtualization is enabled in your BIOS/firmware (especially on Linux). Without it, containers won't run! 🧬
- **Permissions:** On macOS, grant Rancher Desktop the necessary permissions if prompted. 🛡️
- **Check logs:** Use the Rancher Desktop UI to view logs for more details on errors. 📋
- **Official docs:** Consult the [Rancher Desktop docs](https://docs.rancherdesktop.io/) for platform-specific help. 📖
- **Search smarter:** Still stuck? Search online or ask Perplexity (https://www.perplexity.ai/) for quick, AI-powered troubleshooting. 🤖
- **Last resort:** Uninstall and reinstall Rancher Desktop if all else fails. 🧹

---

> "With great clusters comes great responsibility." 🕸️