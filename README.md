
**GOAL**
Sentiment analysis on IMDb movie reviews

**SCRAPING METHOD**
1. Open IMDb review page (https://www.imdb.com/title/tt2527336/reviews/?ref_=tt_ururv_genai_sm)
2. Press 'Show All' button to load all reviews
3. Run command to open all spoilers

```
    const spoilerButtons = document.querySelectorAll('.review-spoiler-button');
    spoilerButtons.forEach(button => {
        button.click();
    });
    console.log(`Clicked ${spoilerButtons.length} spoiler button(s).`);
```

4. Open inspector
5. Right click <html> and copy InnerHTML
6. Paste to .html file and save
7. Parse HTML file with BeautifulSoup4
8. Get title, content, and rating from reviews
9. Save to csv

**SENTIMENT ANAYLSIS METHOD**
Scenario 1
- Model: Random Forest
- Feature Extraction: TF-IDF
- Training: 70/30

Scenario 2
- Model: Support Vector Machine (SVM)
- Feature Extraction: TF-IDF
- Training: 80/20

Scenario 3
- Model: Deep Learning (LTSM)
- Feature Extraction: Word2Vec
- Training: 70/30