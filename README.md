# MarMesh - AI Marketing Campaign Automation

**Transform your campaign brief into a complete multi-channel marketing campaign in minutes! Just describe your product and budget - our AI agents handle the rest.**

[![Watch on YouTube](https://img.shields.io/badge/Watch%20on-YouTube-red?logo=youtube&style=for-the-badge)](https://www.youtube.com/watch?v=KklDjV3atjY)


If you have any questions or would like to collaborate, feel free to reach out to me on [LinkedIn](https://www.linkedin.com/in/jenya-stoeva-60477249/). You're more than welcome!

## For Marketers, By Marketers
✅ **Campaign Strategy** - AI researches your market and creates data-driven strategies  
✅ **Human Approval** - Review and edit all campaign details before execution  
✅ **Content Creation** - Automatically generates video content for your campaigns  
✅ **Multi-Channel Publishing** - Publishes to YouTube, Instagram, TikTok, ... simultaneously  
✅ **Complete Automation** - From brief to live campaign with minimal manual work  

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

## How-To

**Option 1:** Run in Colab

- [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1jUIkSO9a671dizPYFAsAWTbCP8VYXi3W)
- Add your API keys in the Colab ```Secrets``` menu: ```PERPLEXITY_SONAR_API_KEY```, ```OPENAI_API_KEY```
- Ask about your idea in the last notebook cell, then either run the cells one by one or choose **Run all** from the **Runtime** menu. The required dependencies are installed at the beginning of the notebook.

```
# idea = "AI‑based evaluation of product novelty in the innovation lifecycle"
# idea = "Mint cholocate invention"
# idea = "Planting pot which can be adjusted to different sizes, to get smaller or bigger depending on the need of the plant to be planted."
# idea = "Overlaying Perplexity research data on a visualization"
# idea = "An invention that can stop all worlf wars."
# idea = "An invention that can judge the craziness of an idea."
# idea = "Was it already discovered that when you press your finger on a tomato a visible fingerprint is left."

idea = "An invention that can judge the craziness of an idea."
fig = process_idea_novelty_visualization(idea)
```

**Option 2:** Run Locally

- Clone this repo and open the uploaded notebook in Jupyter or VSCode
- Create a .env file with your API keys:
  - ```PERPLEXITY_SONAR_API_KEY```
  - ```OPENAI_API_KEY```
- Ask about your idea in the last notebook cell, then either run the notebook cells one by one or choose **Run All Cells** from the **Run** menu. 
