# 📦 MP Police Question Packets (GitHub + jsDelivr CDN)

इस फोल्डर में आप जितने चाहें उतने मॉक टेस्ट और चेप्टर वाइज प्रश्न रख सकते हैं।

## 🌐 यह कैसे काम करता है?
1. **Zero Database / Zero Hosting Cost:** आपको कोई Firebase या MySQL डेटाबेस नहीं चाहिए।
2. **On-Demand Chunked Streaming:** 
   - जब छात्र ऐप में किसी टेस्ट (जैसे `mp-police-mock-01` या `vip-mock-series-15`) पर क्लिक करेगा, सिर्फ तभी उस टेस्ट का छोटा पैकेट jsDelivr CDN से डाउनलोड होगा।
   - सारा डेटा एक साथ लोड होकर ऐप को धीमा नहीं करेगा।
3. **Offline Caching:**
   - एक बार डाउनलोड होने के बाद प्रश्न फोन की मेमोरी (`AsyncStorage`) में सुरक्षित हो जाते हैं। अगली बार इंटरनेट न होने पर भी टेस्ट तुरंत खुलेगा!

## 🚀 नया टेस्ट या प्रश्न कैसे जोड़ें?
बस `packets/` फोल्डर में एक नई JSON फाइल बनाएं:
उदाहरण: `packets/mock_test_03.json`:
```json
[
  {
    "id": "q1",
    "topicId": "mock_test_03",
    "question": "मध्य प्रदेश का सबसे बड़ा राष्ट्रीय उद्यान कौन सा है?",
    "options": ["कान्हा किसली", "बांधवगढ़", "पन्ना", "सतपुड़ा"],
    "correctAnswer": "कान्हा किसली",
    "explanation": "कान्हा किसली राष्ट्रीय उद्यान 940 वर्ग किमी में फैला मध्य प्रदेश का सबसे बड़ा पार्क है।",
    "difficulty": "Easy"
  }
]
```

फिर GitHub पर `git push` कर दें।
jsDelivr CDN अपने आप इसे दुनिया भर में सुपर-फास्ट स्पीड में ऐप तक पहुंचा देगा!
URL पैटर्न:
`https://cdn.jsdelivr.net/gh/edupluscreation/mppolice@main/packets/<packetId>.json`
