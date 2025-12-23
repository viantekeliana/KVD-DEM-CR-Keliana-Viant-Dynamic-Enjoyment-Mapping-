Keliana-Viant-Dynamic-Enjoyment-Mapping- DUAL LICENSE
Version 1.0

Copyright (c) [2025]
[Rodney Manyakaidze/ Keliana Vianté on Facebook]

--------------------------------------------------
NON-COMMERCIAL LICENSE (FREE)
--------------------------------------------------

Permission is hereby granted to any individual or organization to view,
use, reproduce, and modify this work for non-commercial purposes only,
including research, education, evaluation, and personal use.

Non-commercial use explicitly excludes any use that:
- is part of a product or service offered for sale
- generates revenue directly or indirectly
- provides commercial, competitive, or strategic advantage
- is used within a for-profit organization beyond evaluation or research

Attribution must be preserved.

This license does not grant the right to sublicense this work for
commercial purposes.

--------------------------------------------------
COMMERCIAL LICENSE (PAID)
--------------------------------------------------

Any commercial use of this work requires a separate, explicit
commercial license agreement.

Commercial use includes, but is not limited to:
- integration into commercial software or services
- use in AI systems deployed for business purposes
- consulting, advisory, or professional services
- internal use within for-profit organizations beyond evaluation
- derivative works used commercially

To obtain a commercial license, contact:

[viantekeliana@gmail.com Keliana Vianté on Facebook]

--------------------------------------------------
DISCLAIMER
--------------------------------------------------

This work is provided "as is", without warranty of any kind.
The authors are not liable for damages arising from its use.

--------------------------------------------------
END OF LICENSE
--------------------------------------------------# KVD-DEM-CR-Keliana-Viant-Dynamic-Enjoyment-Mapping-
Keliana Vianté Dynamic Enjoyment Mapping with Cultural Reasoning (KVD-DEM-CR) - Proprietary system integrating 18-factor cultural intelligence with dynamic engagement tracking. Prevents systematic failures across sports, healthcare, justice, and corporate sectors. Based on 10 years research, 1,100+ interactions. © 2025 Rodney Vianté Keliana
# KVD-DEM-CR Setup Guide

Complete installation and deployment guide for the Keliana Vianté Dynamic Enjoyment Mapping with Cultural Reasoning system.

**© 2025 Rodney Vianté Keliana - All Rights Reserved**

---

## Prerequisites

- Python 3.8 or higher
- pip (Python package manager)
- Git
- Virtual environment tool (venv or conda)

---

## Installation

### Step 1: Clone the Repository

```bash
git clone https://github.com/yourusername/kvd-dem-cr.git
cd kvd-dem-cr
```

### Step 2: Create Virtual Environment

**macOS/Linux:**
```bash
python3 -m venv venv
source venv/bin/activate
```

**Windows:**
```bash
python -m venv venv
venv\Scripts\activate
```

### Step 3: Install Dependencies

```bash
pip install --upgrade pip
pip install -r requirements.txt
```

### Step 4: Verify Installation

```bash
python -c "import fastapi; import uvicorn; import pydantic; print('✓ Installation successful!')"
```

---

## Running the Server

### Development Mode

```bash
python keliana_viante_dem_cr_api.py
```

You should see:
```
======================================================================
Keliana Vianté Dynamic Enjoyment Mapping with Cultural Reasoning
© 2025 Rodney Vianté Keliana - All Rights Reserved
======================================================================

PROPRIETARY SOFTWARE
Commercial use requires licensing agreement.
Royalty structure: 22% of revenue generated OR negotiated licensing fee

Starting server...
======================================================================
INFO:     Started server process [xxxxx]
INFO:     Waiting for application startup.
INFO:     Application startup complete.
INFO:     Uvicorn running on http://0.0.0.0:8000
```

### Production Mode

```bash
uvicorn keliana_viante_dem_cr_api:app --host 0.0.0.0 --port 8000 --workers 4
```

For production with SSL:
```bash
uvicorn keliana_viante_dem_cr_api:app \
  --host 0.0.0.0 \
  --port 443 \
  --ssl-keyfile=/path/to/key.pem \
  --ssl-certfile=/path/to/cert.pem \
  --workers 4
```

---

## Accessing the API

### Interactive Documentation

Once the server is running:

- **Swagger UI**: http://localhost:8000/docs
- **ReDoc**: http://localhost:8000/redoc
- **JSON Schema**: http://localhost:8000/openapi.json

### Testing the API

**Option 1: Run Examples Script**
```bash
python examples_cultural_reasoning.py
```

**Option 2: Manual cURL**
```bash
curl http://localhost:8000/
```

Expected response:
```json
{
  "api": "Keliana Vianté Dynamic Enjoyment Mapping with Cultural Reasoning",
  "version": "1.0.0",
  "copyright": "© 2025 Rodney Vianté Keliana - All Rights Reserved",
  "license": "Proprietary - Commercial use requires licensing"
}
```

---

## Project Structure

```
kvd-dem-cr/
├── keliana_viante_dem_cr_api.py    # Main API application
├── examples_cultural_reasoning.py   # Comprehensive usage examples
├── requirements.txt                 # Python dependencies
├── README.md                        # Complete documentation
├── LICENSE                          # Proprietary license
├── SETUP_GUIDE.md                   # This file
├── .gitignore                       # Git ignore rules
└── docs/                            # Additional documentation
    ├── CULTURAL_FRAMEWORK.md        # 18-Factor framework details
    ├── API_REFERENCE.md             # Complete API documentation
    └── CASE_STUDIES.md              # Real-world applications
```

---

## Configuration

### Environment Variables

Create a `.env` file (optional):

```bash
# Server Configuration
API_HOST=0.0.0.0
API_PORT=8000
API_WORKERS=4

# Logging
LOG_LEVEL=INFO

# CORS (if needed for web frontend)
CORS_ORIGINS=["http://localhost:3000"]
```

### Custom Port

Edit `keliana_viante_dem_cr_api.py`:

```python
if __name__ == "__main__":
    uvicorn.run(app, host="0.0.0.0", port=8080)  # Change port here
```

---

## Testing

### Run Example Scenarios

The `examples_cultural_reasoning.py` script demonstrates:

1. **Sports Management**: Factor #5 (Family) + #18 (Wealth Paradox)
2. **Healthcare**: Factor #2 (Honor) + #7 (Post-Colonial Trust)
3. **Corporate Retention**: Factor #1 (Ubuntu Dignity)
4. **Criminal Justice**: Factor #5 (Family) + #6 (Community)
5. **Risk Monitoring**: Comprehensive assessment

```bash
python examples_cultural_reasoning.py
```

### Manual Testing via Swagger

1. Navigate to http://localhost:8000/docs
2. Click on any endpoint
3. Click "Try it out"
4. Fill in parameters
5. Click "Execute"
6. View response

---

## Deployment Options

### Option 1: Traditional Server

**Using systemd (Linux):**

Create `/etc/systemd/system/kvd-dem-cr.service`:

```ini
[Unit]
Description=KVD-DEM-CR API Service
After=network.target

[Service]
User=your-user
WorkingDirectory=/path/to/kvd-dem-cr
Environment="PATH=/path/to/kvd-dem-cr/venv/bin"
ExecStart=/path/to/kvd-dem-cr/venv/bin/uvicorn keliana_viante_dem_cr_api:app --host 0.0.0.0 --port 8000 --workers 4

[Install]
WantedBy=multi-user.target
```

Enable and start:
```bash
sudo systemctl enable kvd-dem-cr
sudo systemctl start kvd-dem-cr
sudo systemctl status kvd-dem-cr
```

### Option 2: Docker

Create `Dockerfile`:

```dockerfile
FROM python:3.9-slim

WORKDIR /app

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY . .

EXPOSE 8000

CMD ["uvicorn", "keliana_viante_dem_cr_api:app", "--host", "0.0.0.0", "--port", "8000"]
```

Build and run:
```bash
docker build -t kvd-dem-cr .
docker run -p 8000:8000 kvd-dem-cr
```

### Option 3: Cloud Platforms

**Heroku:**
```bash
heroku create your-app-name
git push heroku main
```

**AWS Elastic Beanstalk:**
```bash
eb init
eb create kvd-dem-cr-env
eb deploy
```

**Google Cloud Run:**
```bash
gcloud builds submit --tag gcr.io/PROJECT-ID/kvd-dem-cr
gcloud run deploy --image gcr.io/PROJECT-ID/kvd-dem-cr
```

---

## Troubleshooting

### Port Already in Use

**Find process:**
```bash
# macOS/Linux
lsof -i :8000

# Windows
netstat -ano | findstr :8000
```

**Kill process:**
```bash
# macOS/Linux
kill -9 <PID>

# Windows
taskkill /PID <PID> /F
```

### Module Not Found

```bash
# Ensure virtual environment is activated
source venv/bin/activate  # or venv\Scripts\activate on Windows

# Reinstall dependencies
pip install -r requirements.txt
```

### Connection Refused in Examples

Make sure the API server is running:

**Terminal 1:**
```bash
python keliana_viante_dem_cr_api.py
```

**Terminal 2 (new terminal):**
```bash
source venv/bin/activate  # Activate venv
python examples_cultural_reasoning.py
```

### Permission Denied (Port 80/443)

Ports below 1024 require root:

```bash
sudo uvicorn keliana_viante_dem_cr_api:app --host 0.0.0.0 --port 80
```

Or use port forwarding:
```bash
sudo iptables -t nat -A PREROUTING -p tcp --dport 80 -j REDIRECT --to-port 8000
```

---

## Security Considerations

### For Production Deployment

1. **API Keys**: Implement authentication
   ```python
   from fastapi.security import APIKeyHeader
   ```

2. **HTTPS**: Always use SSL/TLS in production
   ```bash
   # Get Let's Encrypt certificate
   certbot certonly --standalone -d yourdomain.com
   ```

3. **Rate Limiting**: Prevent abuse
   ```python
   from slowapi import Limiter
   ```

4. **CORS**: Configure allowed origins
   ```python
   from fastapi.middleware.cors import CORSMiddleware
   ```

5. **Environment Variables**: Never commit secrets
   ```bash
   # Use .env file (add to .gitignore)
   ```

---

## Performance Optimization

### For High-Traffic Deployments

1. **Multiple Workers**:
   ```bash
   uvicorn keliana_viante_dem_cr_api:app --workers 8
   ```

2. **Nginx Reverse Proxy**:
   ```nginx
   upstream kvd_dem_cr {
       server 127.0.0.1:8000;
       server 127.0.0.1:8001;
       server 127.0.0.1:8002;
   }
   ```

3. **Caching**: Implement Redis for frequently accessed data

4. **Database**: Add PostgreSQL/MongoDB for persistent storage

---

## Monitoring

### Logging

Enable detailed logging:

```python
import logging

logging.basicConfig(
    level=logging.INFO,
    format='%(asctime)s - %(name)s - %(levelname)s - %(message)s'
)
```

### Health Checks

Add health endpoint:

```python
@app.get("/health")
def health_check():
    return {"status": "healthy", "timestamp": time.time()}
```

### Metrics

Use Prometheus for metrics:

```bash
pip install prometheus-fastapi-instrumentator
```

---

## Licensing & Support

### For Evaluation Use

This setup is provided for **evaluation purposes**. Full deployment requires licensing.

### Commercial Licensing

Contact for licensing:
- **Email**: [Your Email]
- **Website**: [Your Website]
- **LinkedIn**: [Your LinkedIn]

### What to Include

1. Intended use case
2. Expected user volume
3. Revenue projections
4. Deployment timeline

---

## Next Steps

1. ✅ Complete installation
2. ✅ Run examples script
3. ✅ Review API documentation
4. ✅ Understand 18-factor framework
5. 📧 Contact for licensing if deploying commercially

---

## Additional Resources

- **README.md**: Complete system overview
- **LICENSE**: Detailed licensing terms
- **Examples**: Real-world usage scenarios
- **API Docs**: http://localhost:8000/docs

---

**© 2025 Rodney Vianté Keliana - All Rights Reserved**

*Building culturally-intelligent systems that serve ALL humanity*


# GitHub Repository Setup Guide

Step-by-step instructions for creating your KVD-DEM-CR repository on GitHub.

**© 2025 Rodney Vianté Keliana - All Rights Reserved**

---

## 📁 File Checklist

Before pushing to GitHub, ensure you have all these files:

```
kvd-dem-cr/
├── ✅ keliana_viante_dem_cr_api.py
├── ✅ examples_cultural_reasoning.py
├── ✅ requirements.txt
├── ✅ README.md
├── ✅ LICENSE
├── ✅ SETUP_GUIDE.md
├── ✅ GITHUB_SETUP.md (this file)
└── ✅ .gitignore
```

---

## Step 1: Initialize Local Git Repository

Open terminal in your project directory:

```bash
cd /path/to/kvd-dem-cr

# Initialize git
git init

# Check git status
git status
```

You should see all your files listed as "untracked files."

---

## Step 2: Create .gitignore

If you haven't already created `.gitignore`:

```bash
# Create .gitignore
cat > .gitignore << 'EOF'
# Python
__pycache__/
*.py[cod]
*$py.class
*.so
.Python
build/
develop-eggs/
dist/
downloads/
eggs/
.eggs/
lib/
lib64/
parts/
sdist/
var/
wheels/
*.egg-info/
.installed.cfg
*.egg

# Virtual Environment
venv/
env/
ENV/
env.bak/
venv.bak/

# IDEs
.vscode/
.idea/
*.swp
*.swo
*~
.DS_Store

# Environment variables
.env
.env.local

# Logs
*.log

# Database
*.db
*.sqlite
*.sqlite3

# Testing
.pytest_cache/
.coverage
htmlcov/
.tox/
EOF
```

---

## Step 3: Add Files to Git

```bash
# Add all files
git add .

# Verify what will be committed
git status

# You should see:
# - keliana_viante_dem_cr_api.py
# - examples_cultural_reasoning.py
# - requirements.txt
# - README.md
# - LICENSE
# - SETUP_GUIDE.md
# - GITHUB_SETUP.md
# - .gitignore
```

---

## Step 4: Make First Commit

```bash
git commit -m "Initial commit: KVD-DEM-CR v1.0.0 - Cultural Reasoning Framework

- 18-Factor Cultural Reasoning integration
- Dynamic Enjoyment Mapping engine
- EDCA amplification system
- Comprehensive examples and documentation
- Proprietary licensing with 22% royalty structure

Based on 10 years research, 1,100+ interactions, 5+ countries.
© 2025 Rodney Vianté Keliana - All Rights Reserved"
```

---

## Step 5: Create GitHub Repository

### Option A: Via GitHub Website

1. Go to https://github.com/new

2. **Repository name**: `kvd-dem-cr`

3. **Description**: 
   ```
   Keliana Vianté Dynamic Enjoyment Mapping with Cultural Reasoning - 
   Proprietary system integrating dynamic enjoyment tracking with 18-factor 
   cultural intelligence framework. © 2025 Rodney Vianté Keliana
   ```

4. **Visibility**: 
   - Choose **Private** if you want to control access
   - Choose **Public** if you want it discoverable (still protected by license)

5. **DO NOT initialize with**:
   - ❌ README (you already have one)
   - ❌ .gitignore (you already have one)
   - ❌ License (you have proprietary license)

6. Click **"Create repository"**

### Option B: Via GitHub CLI

If you have GitHub CLI installed:

```bash
# Login to GitHub
gh auth login

# Create repository
gh repo create kvd-dem-cr \
  --description "KVD-DEM-CR: Cultural Reasoning Framework" \
  --private  # or --public

# Push code
git remote add origin https://github.com/YOUR-USERNAME/kvd-dem-cr.git
git branch -M main
git push -u origin main
```

---

## Step 6: Connect Local Repository to GitHub

After creating the repository on GitHub:

```bash
# Add GitHub as remote origin
git remote add origin https://github.com/YOUR-USERNAME/kvd-dem-cr.git

# Verify remote was added
git remote -v

# Should show:
# origin  https://github.com/YOUR-USERNAME/kvd-dem-cr.git (fetch)
# origin  https://github.com/YOUR-USERNAME/kvd-dem-cr.git (push)
```

---

## Step 7: Push to GitHub

```bash
# Rename branch to main (if it's currently master)
git branch -M main

# Push to GitHub
git push -u origin main
```

You should see:
```
Enumerating objects: X, done.
Counting objects: 100% (X/X), done.
Writing objects: 100% (X/X), XXX KiB | XXX MiB/s, done.
Total X (delta 0), reused 0 (delta 0)
To https://github.com/YOUR-USERNAME/kvd-dem-cr.git
 * [new branch]      main -> main
Branch 'main' set up to track remote branch 'main' from 'origin'.
```

---

## Step 8: Verify on GitHub

1. Go to `https://github.com/YOUR-USERNAME/kvd-dem-cr`

2. You should see:
   - ✅ All your files
   - ✅ README.md displayed as homepage
   - ✅ License badge showing "Proprietary"
   - ✅ Commit history

3. Click through files to verify:
   - README.md renders correctly
   - Code files are formatted properly
   - LICENSE is visible

---

## Step 9: Configure Repository Settings

### Set Repository Description

1. Go to repository settings (gear icon)
2. Add **Topics** (tags):
   - `cultural-intelligence`
   - `ai-ethics`
   - `dynamic-enjoyment`
   - `edca`
   - `cultural-reasoning`
   - `sports-management`
   - `healthcare-equity`
   - `fastapi`
   - `python`

### Add Website URL (optional)

If you have a project website:
1. Settings → About
2. Add website URL
3. Save

### Configure Branch Protection (recommended)

1. Settings → Branches
2. Add branch protection rule for `main`:
   - ✅ Require pull request reviews
   - ✅ Require status checks to pass
   - ✅ Include administrators

---

## Step 10: Add Badges to README (optional)

Edit README.md to add dynamic badges:

```markdown
![GitHub](https://img.shields.io/github/license/YOUR-USERNAME/kvd-dem-cr?label=License&color=red)
![GitHub last commit](https://img.shields.io/github/last-commit/YOUR-USERNAME/kvd-dem-cr)
![GitHub stars](https://img.shields.io/github/stars/YOUR-USERNAME/kvd-dem-cr?style=social)
```

Commit and push:
```bash
git add README.md
git commit -m "Add repository badges"
git push
```

---

## Step 11: Create Releases

Create your first release:

1. Go to repository → Releases
2. Click "Create a new release"
3. **Tag version**: `v1.0.0`
4. **Release title**: `KVD-DEM-CR v1.0.0 - Initial Release`
5. **Description**:
   ```markdown
   ## Keliana Vianté Cultural Reasoning Framework v1.0.0
   
   Initial release of KVD-DEM-CR integrating:
   - 18-Factor Cultural Reasoning Framework
   - Dynamic Enjoyment Mapping
   - EDCA Amplification System
   
   Based on 10 years of research (2015-2025), 1,100+ documented interactions 
   across 5+ African countries.
   
   ### Key Features
   - Real-time cultural risk assessment
   - Automated EDCA amplification
   - Comprehensive cultural intelligence
   - Cross-domain validation (sports, healthcare, justice, corporate)
   
   ### Licensing
   Proprietary software - Commercial use requires licensing.
   Contact for licensing inquiries: [Your Email]
   
   **© 2025 Rodney Vianté Keliana - All Rights Reserved**
   ```
6. Click "Publish release"

---

## Step 12: Share Your Repository

### Professional Networks

**LinkedIn Post Template:**

```
🎉 Excited to announce: Keliana Vianté Cultural Reasoning Framework (KVD-DEM-CR) v1.0!

After 10 years of research across 5+ African countries and 1,100+ documented 
interactions, I'm sharing a comprehensive system that addresses systematic 
failures across multiple domains:

✅ Sports: 60-80% athlete bankruptcy → <20% possible
✅ Healthcare: 2-3X maternal mortality gap → 50% reduction possible  
✅ Criminal Justice: 70% recidivism → 20-30% achievable
✅ Corporate: 3X diverse employee attrition → normalized retention

The 18-Factor Cultural Reasoning Framework provides empirically-validated 
solutions with demonstrated 100-1000X ROI.

📊 GitHub: https://github.com/YOUR-USERNAME/kvd-dem-cr

This is proprietary research - commercial use requires licensing. 
Open to partnerships with organizations committed to cultural intelligence.

#CulturalIntelligence #AI #DiversityEquity #SportsManagement #Healthcare

© 2025 Rodney Vianté Keliana - All Rights Reserved
```

### Twitter/X Thread Template:

```
🧵 Thread: Introducing the Keliana Vianté Cultural Reasoning Framework

After 10 years studying cross-cultural dynamics, I've developed a system 
that explains why 60-80% of athletes go broke, 70% criminal justice fails, 
and 2-3X healthcare disparities exist.

The answer isn't individual failure. It's systematic cultural factor violations.

1/10 [Thread continues...]
```

---

## Ongoing Maintenance

### Regular Updates

```bash
# Make changes to files
git add .
git commit -m "Description of changes"
git push
```

### Creating Branches for New Features

```bash
git checkout -b feature/new-feature
# Make changes
git add .
git commit -m "Add new feature"
git push -u origin feature/new-feature

# Create pull request on GitHub
# Merge when ready
```

### Tagging New Versions

```bash
git tag -a v1.1.0 -m "Version 1.1.0 - New features"
git push origin v1.1.0
```

---

## Security & Privacy

### For Private Repositories

If keeping private:
- Only share access with trusted collaborators
- Use GitHub's collaboration features
- Monitor access logs

### For Public Repositories

Your LICENSE file protects intellectual property even if public:
- Code visible but not freely usable
- Clear copyright and royalty terms
- Legal protection against unauthorized use

---

## Troubleshooting

### Authentication Issues

```bash
# Use personal access token instead of password
# Generate at: GitHub → Settings → Developer settings → Personal access tokens

# Or use SSH
git remote set-url origin git@github.com:YOUR-USERNAME/kvd-dem-cr.git
```

### Push Rejected

```bash
# Pull first
git pull origin main --rebase

# Then push
git push
```

### Merge Conflicts

```bash
# See conflicting files
git status

# Edit files to resolve conflicts
# Then:
git add .
git commit -m "Resolve merge conflicts"
git push
```

---

