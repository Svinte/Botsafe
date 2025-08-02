<section style="display: flex; gap: 8px; justify-content: flex-end;">
    <img src="https://raw.githubusercontent.com/github/explore/main/topics/vue/vue.png" alt="Vue.js" height="24" />
    <img src="https://raw.githubusercontent.com/github/explore/main/topics/typescript/typescript.png" alt="TypeScript" height="24" />
</section>


# Botsafe
Scripts to prevent Web scraping

---

## How it defends data?
Botsafe breaks link content into array of letters. The data is stored into HTML link element via data attribute named ``data-botsafe``. Browser turns link data into working link using JavaScript.

This kind of approach defends link data from Crawlers that:
1. Have JavaScript disabled for security reasons.
2. Run after DOM load before Botsafe starts.
3. Are not used to crawl this kind of data.

### Against AI crawlers
We add noise into the array so regular AI cannot detect the pattern of the array. By default i2 and i5 are random noise.

### Other defending tools.
Botsafe allows every kind of HTML5 eventlistener to trigger Botsafe. You can change triggering method using link element ``data-reassemble-on`` -attribute.

After finishing raessembling the Botsafe removes it's attributes not including botsafe classname.
