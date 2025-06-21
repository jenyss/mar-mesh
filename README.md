# MarMesh - AI Marketing Campaign Automation

**Transform your campaign brief into a complete multi-channel marketing campaign in minutes! Just describe your product and budget and let this Google ADK agent handle the rest.**

[![Watch on YouTube](https://img.shields.io/badge/Watch%20on-YouTube-red?logo=youtube&style=for-the-badge)](https://www.youtube.com/watch?v=KklDjV3atjY) **Hackathon Video**

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1eVnoC7Tx5cnH_GRy5-_hOsm3s-hdN9Re?usp=sharing)

[![Watch on YouTube](https://img.shields.io/badge/Watch%20on-YouTube-red?logo=youtube&style=for-the-badge)](https://youtube.com/shorts/a98-OUanNHs?feature=share) **Generated Video**

If you have any questions or would like to collaborate, feel free to reach out to me on [LinkedIn](https://www.linkedin.com/in/jenya-stoeva-60477249/). You're more than welcome!

**Campaign Strategy** - AI researches your market and creates data-driven strategies<br>
**Human Approval** - Review and edit all campaign details before execution  
**Content Creation** - Automatically generates video content for your campaigns<br>
**Multi-Channel Publishing** - Publishes to YouTube, Instagram, TikTok, ... simultaneously  <br>
**Complete Automation** - From brief to live campaign with minimal manual work  <br>

## How It Works
1. **Input:** _Example_ "Launch energy drink Drex, organic ingredients, 100€ budget"
2. **AI Strategy:** Generates target audience, channels, KPIs, messaging
3. **Your Approval:** Review and tweak the campaign plan
4. **Content Creation:** AI creates promotional video content
5. **Your Final OK:** Approve the creative before it goes live
6. **Auto-Publish:** Deploys across all selected social channels

## Perfect For
- **Small businesses** with limited marketing resources
- **Startups** launching new products quickly
- **Agencies** wanting to scale campaign creation
- **Marketers** who want AI to handle the heavy lifting

*Turn hours of campaign planning into minutes of smart automation!*


## Architecture

![MarMesh Architecture](https://github.com/user-attachments/assets/b50302a8-1c7d-454d-a560-129fbe3c57b2)

### _User Input_

User starts the MarMesh campaign by submitting a product launch brief and product image.

### _Google ADK Sequential Agent_

**Role:** Master Orchestrator & Workflow Controller

**What it does:** Coordinates all campaign agents in sequence to deliver a complete end-to-end marketing automation workflow from initial brief to live multi-channel deployment.

**Process:** Orchestrates the full pipeline: Research → Human Approval → Content Creation → Content Approval → Publishing

**Output:** Complete automated marketing campaign with human checkpoints at critical decision points

*The conductor of your AI marketing orchestra - ensures all agents work together seamlessly to transform your product brief into live campaigns.*

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
5. **Audio Production** - Generates professional voiceover and background music with Lyria<br>
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
4. **Auto-Resume** - Automatically proceeds to publishing after approval or stops workflow if rejected<br>

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
3. **Campaign Archival** - Saves complete campaign state and execution data to local JSON files for record-keeping<br>
4. **Completion Confirmation** - Reports successful publishing with live URLs and campaign summary<br>

**Key Feature:** **One-Click Multi-Channel** - Publishes to multiple platforms simultaneously instead of manual uploads to each platform

**Output:** Live campaign content across all channels plus complete campaign documentation for future reference

*Your distribution powerhouse - turns approved content into live campaigns across the social media ecosystem in seconds.*


## How-To

**Option 1:** Run in Colab

- [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1eVnoC7Tx5cnH_GRy5-_hOsm3s-hdN9Re?usp=sharing)
- Add your API keys in the Colab ```Secrets``` menu: ```PERPLEXITY_SONAR_API_KEY```, ```OPENAI_API_KEY```, ```FAL_KEY```, ```GOOGLE_API_KEY```
- Ask ChatGPT how publish video on YouTube, then create secret with name: ```GOOGLE_CLIENT_SECRET``` and as value: copy/paste the content of your google ```client_secret.json``` file.
- Define your product campaign brief and upload a product image, then launch the entire AI marketing automation workflow by using **Run all** from the **Runtime** menu. The required dependencies are installed at the beginning of the notebook.<br>

  **Input:**<br>
  **`campaign_briefing`** - (**mandatory**) Your product description, key features, motto, and budget<br>
  **`image_path`** - (**mandatory**) Product image file for visual content creation (optional)<br>


**Option 2:** Run Locally

- Clone this repo and open the uploaded notebook in JupyterLab
- Create a .env file with your API keys:
  - ```PERPLEXITY_SONAR_API_KEY```
  - ```OPENAI_API_KEY```
  - ```FAL_KEY```
  - ```GOOGLE_API_KEY```
- Ask ChatGPT how publish video on YouTube, then pass its path of your google ```client_secret.json``` file as value to ```CLIENT_SECRET_FILE```, located above the ```get_authenticated_service()```
- In the last notebook cell, define your product campaign brief and upload a product image, then either run the notebook cells one by one or choose **Run All Cells** from the **Run** menu.
  **Input Required:**<br>
  **`campaign_briefing`** - (**mandatory**) Your product description, key features, motto, and budget<br>
  **`image_path`** - (**mandatory**) Product image file for visual content creation (optional)<br>
