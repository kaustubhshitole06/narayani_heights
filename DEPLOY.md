# Deploy to Render.com

## Steps:

1. **Create GitHub Repository**
   - Go to https://github.com/new
   - Create a new repo (e.g., "food-menu-processor")
   - Push your code:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/food-menu-processor.git
   git push -u origin main
   ```

2. **Deploy on Render**
   - Go to https://render.com and sign up
   - Click "New +" → "Web Service"
   - Connect your GitHub repo
   - Configure:
     - **Name**: food-menu-processor
     - **Runtime**: Python 3
     - **Build Command**: `pip install -r requirements.txt`
     - **Start Command**: `uvicorn app:app --host 0.0.0.0 --port $PORT`
   - Add Environment Variable:
     - Key: `GEMINI_API_KEY`
     - Value: Your Gemini API key
   - Click "Create Web Service"

3. **Access Your App**
   - Wait 2-3 minutes for deployment
   - Your app will be live at: `https://your-app-name.onrender.com`

---

# Alternative: Deploy to Railway.app

1. Go to https://railway.app
2. Click "New Project" → "Deploy from GitHub"
3. Select your repo
4. Add environment variable: `GEMINI_API_KEY`
5. Done! Auto-deploys on every push

---

# Alternative: Deploy to Vercel (Serverless)

Not recommended for this app because:
- File uploads need persistent storage
- Gemini API calls may take time

Stick with Render or Railway for best results.
