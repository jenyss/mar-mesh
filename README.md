# MarMesh - AI Marketing Campaign Automation

**Transform your campaign brief into a complete multi-channel marketing campaign in minutes! Just describe your product and budget and let this Google ADK agent handle the rest.**

**Campaign Strategy** - AI researches your market and creates data-driven strategies<br>
**Human Approval** - Review and edit all campaign details before execution  
**Content Creation** - Automatically generates video content for your campaigns<br>
**Multi-Channel Publishing** - Publishes to YouTube, Instagram, TikTok, ... simultaneously  <br>
**Complete Automation** - From brief to live campaign with minimal manual work  <br>

### Perfect For
- **Small businesses** with limited marketing resources
- **Startups** launching new products quickly
- **Agencies** wanting to scale campaign creation
- **Marketers** who want AI to handle the heavy lifting

*Turn hours of campaign planning into minutes of smart automation!*

[![ADK Hackathon](https://img.shields.io/badge/ADK-Hackathon-blue)](https://devpost.com/software/marmesh)

**Hackathon Video**<br>
[![Watch on YouTube](https://img.shields.io/badge/Watch%20on-YouTube-red?logo=youtube&style=for-the-badge)](https://youtu.be/rp_U5jcZ_w8) 

If you have any questions or would like to collaborate, feel free to reach out to me on [LinkedIn](https://www.linkedin.com/in/jenya-stoeva-60477249/). You're more than welcome!

## How It Works
1. **Input:** _Example_ "Launch energy drink Drex, organic ingredients, 100€ budget" & Product image
2. **AI Strategy:** Generates target audience, channels, KPIs, messaging
3. **Your Approval:** Review and tweak the campaign plan
4. **Content Creation:** AI creates promotional video content
5. **Your Final OK:** Approve the creative before it goes live
6. **Auto-Publish:** Deploys across all selected social channels
7. **Data Persistence:** Campaign data stored in the agent's tool_context is automatically saved to a local JSON file for future analytics and reference

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1eVnoC7Tx5cnH_GRy5-_hOsm3s-hdN9Re?usp=sharing)

**MarMesh Generated Video**<br>
[![Watch on YouTube](https://img.shields.io/badge/Watch%20on-YouTube-red?logo=youtube&style=for-the-badge)](https://youtube.com/shorts/S1BcDa-Bf1U?feature=share) 

**Product Image Input:** [drex2](https://github.com/user-attachments/assets/6ea38410-a709-45fc-b1ae-e11ca92c4405)


## Architecture

### Technical Stack
**Core Framework:** Google Agent Development Kit (ADK)<br>
**Marketing Strategy Research:** Gemini, Perplexity<br>
**Prompt Generation:** GPT-4o<br>
**AI Image Generation:** Flux Pro AI<br>
**Video Animation:** Kling 2.1 Master<br>
**Audio Production:** Lyria (Google DeepMind)<br>
**Video Assembly:** FFMPEG<br>
**Multi-Platform Publishing:** YouTube Data API v3, (Instagram Graph API, TikTok API - not implemented)<br>

![MarMesh Architecture](https://github.com/user-attachments/assets/efa97e0e-98b9-4278-b72c-ffc927079184)


### _User Input_

User starts the MarMesh campaign by submitting a product launch brief and product image.

### _Google ADK Sequential Agent_

**Role:** Master Orchestrator & Workflow Controller

**What it does:** Coordinates all campaign agents in sequence to deliver a complete end-to-end marketing automation workflow from initial brief to live multi-channel deployment.

**Process:** Orchestrates the full pipeline: Research → Human Approval → Content Creation → Content Approval → Publishing

**Output:** Complete automated marketing campaign with human checkpoints at critical decision points

*The conductor of your AI marketing orchestra - ensures all agents work together seamlessly to transform your product brief into live campaigns.*

---

## Campaign Advisor Agent

**Role:** Senior Marketing Strategist & Research Coordinator

**What it does:** Takes your product brief and creates a complete, data-driven campaign strategy by researching market trends and synthesizing insights from multiple AI sources.

**Process:**
1. **Research Phase** - Queries both Gemini and Perplexity for market insights, competitor analysis, and strategy recommendations
2. **Synthesis Phase** - Combines all research into a structured campaign plan with target audience, channels, messaging, KPIs, and budget allocation
3. **Validation** - Ensures all critical campaign elements are present before passing to approval

**Output:** Complete campaign strategy ready for human review and approval

*The strategic brain of your marketing automation - transforms basic product info into professional campaign plans backed by AI research.*

---

### _Campaign Approver Agent_

**Role:** Human-in-the-Loop Gateway & Workflow Controller

**What it does:** Creates an interactive approval interface where you can review, edit, and approve the AI-generated campaign strategy before execution.

**Process:**
1. **Display Campaign Form** - Shows editable campaign details including target audience, channels, messaging, budget, and KPIs<br>
2. **Human Review** - Pauses workflow while you review and modify any campaign elements<br>
3. **Approval Gate** - Waits for your "Confirm & Save" or "Reject" decision<br>
4. **Auto-Resume** - Automatically continues workflow after approval with your edited campaign data<br>

**Key Feature:** **Editable Interface** - You can modify target audience, adjust messaging, change channels, or update budget before approving

**Output:** User-approved campaign strategy with any modifications, ready for content creation

*Your quality control checkpoint - ensures every campaign meets your standards before going live.*

---

### _Campaign Content Creator Agent_

**Role:** AI Video Production Studio

**What it does:** Transforms your approved campaign strategy into professional video content using cutting-edge AI tools for image generation, animation, and audio production.

**Process:**
1. **Script Generation** - Creates detailed prompts for visual scenes based on your campaign messaging<br>
2. **Image Creation** - Uses Flux Pro AI to generate high-quality product and lifestyle images<br>
3. **Video Animation** - Animates images into dynamic video scenes with Kling 2.1 Master<br>
4. **Video Assembly** - Concatenates all scenes into a cohesive campaign video<br>
5. **Audio Production** - Generates background music with Lyria<br>
6. **Final Production** - Merges video and audio into broadcast-ready content<br>

**Output:** Complete promotional video file ready for multi-channel publishing

*Your AI creative team - handles the entire video production pipeline from concept to final cut, no video editing skills required.*

---

### _Campaign Content Approver Agent_

**Role:** Creative Quality Control & Publishing Gateway

**What it does:** Displays the AI-generated video content for your final review and approval before it goes live across social channels.

**Process:**
1. **Content Preview** - Shows the completed video with audio in an interactive player<br>
2. **Human Review** - Pauses workflow while you watch and evaluate the creative content<br>
3. **Publishing Decision** - Waits for your "Approve & Publish" or "Reject" choice<br>
4. **Auto-Resume** - Proceeds to publishing after approval or stops workflow if rejected<br>

**Key Feature:** **Video Preview Interface** - Watch the complete campaign video before it's published to ensure quality and brand alignment

**Output:** Approved video content ready for multi-channel distribution, or workflow termination if rejected

*Your final creative checkpoint - ensures every piece of content represents your brand perfectly before going public.*

---

### _Campaign Publisher Agent_

**Role:** Multi-Channel Distribution Engine & Campaign Archive

**What it does:** Takes your approved video content and automatically publishes it across all selected social media channels, then saves a complete record of the campaign.

**Process:**
1. **Channel Detection** - Reads approved campaign data to identify target platforms and generates metadata to maximize content visibility and clarity (YouTube, Instagram, TikTok, etc.)<br>
2. **Multi-Platform Publishing** - Simultaneously uploads video content to all selected channels with platform-optimized settings<br>
3. **Campaign Archival** - Saves complete campaign state and execution data to local JSON files for record-keeping and analytics<br>
4. **Completion Confirmation** - Reports successful publishing with live URLs and campaign summary<br>

**Key Feature:** **One-Click Multi-Channel** - Publishes to multiple platforms simultaneously instead of manual uploads to each platform

**Output:** Live campaign content across all channels plus complete campaign documentation for future reference

*Your distribution powerhouse - turns approved content into live campaigns across the social media ecosystem in seconds.*


## How-To

**Option 1:** Run in Colab

- [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1eVnoC7Tx5cnH_GRy5-_hOsm3s-hdN9Re?usp=sharing)
- Add your API keys in the Colab ```Secrets``` menu: ```PERPLEXITY_SONAR_API_KEY```, ```OPENAI_API_KEY```, ```FAL_KEY```, ```GOOGLE_API_KEY```
- Create an OAuth 2.0 Client in GCP with ```Desktop App``` permissions and add a Test user (if you don't have an user already). Then, create a secret named ```GOOGLE_CLIENT_SECRET``` and set its value to the full contents of your Google ```client_secret.json``` file. Just copy/paste the whole JSON content.
- Define your product campaign brief, upload a product image and pass the path to it in the ```image_path```, then launch the entire AI marketing automation workflow by using **Run all** from the **Runtime** menu. The required dependencies are installed at the beginning of the notebook. **Note: You may need to restart the session.**<br>

  **Input:**<br>
  **`campaign_briefing`** - (**mandatory**) Your product description, key features, motto, and budget<br>
  **`image_path`** - (**mandatory**) Product image file for visual content creation (optional)<br>

  **❗❗❗**
  **Important:** After each approval step, you must manually resume the workflow by executing the `await resume_workflow()` cell provided in the notebook.


**Option 2:** Run Locally

- Clone this repo and open the uploaded notebook in JupyterLab
- Create a .env file with your API keys:
  - ```PERPLEXITY_SONAR_API_KEY```
  - ```OPENAI_API_KEY```
  - ```FAL_KEY```
  - ```GOOGLE_API_KEY```
- Create an OAuth 2.0 Client in GCP with ```Web App``` permissions and add a Test user (if you don’t have one already). Download the ```client_secret.json``` file from Google and provide its path as the value for ```CLIENT_SECRET_FILE```, located above the ```get_authenticated_service()``` function.
- In the last notebook cell, define your product campaign brief and upload a product image, then either run the notebook cells one by one or choose **Run All Cells** from the **Run** menu.<br>

  **Input:**<br>
  **`campaign_briefing`** - (**mandatory**) Your product description, key features, motto, and budget<br>
  **`image_path`** - (**mandatory**) Product image file for visual content creation (optional)<br>
- (Optional) You can update<br>
   `parts=[types.Part(text="Approved. Please continue.")]`<br>
   to<br>
   `parts=[types.Part(text="Approved. Please continue. Do not repeat campaign strategy.")]`<br>
   This helps instruct the agent to proceed without re-generating a generic campaign strategy (which isn’t persisted and is redundant since that step is already complete).

  **❗❗❗**
  **Important:** After each approval step, you must manually resume the workflow by executing the `await resume_workflow()` cell provided in the notebook.
