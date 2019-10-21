---
chapter: परिचय
title: परिचय
lang: hi
layout: exercise
---

Sonic Pi एक ओपन-सोर्स प्रोग्रामिंग वातावरण है, जिसे नई ध्वनियों को बनाने की प्रक्रिया के माध्यम से प्रोग्रामिंग अवधारणाओं का पता लगाने और सिखाने के लिए डिज़ाइन किया गया है। यह कैम्ब्रिज कंप्यूटर प्रयोगशाला विश्वविद्यालय में Sam Aaron  द्वारा बनाई गई सभी के लिए एक नि: शुल्क लाइव कोडिंग synth है। आप Sonic Pi का उपयोग Canons से लेकर Dubstep तक, शास्त्रीय और समकालीन शैलियों में कार्यक्रम, रचना और प्रदर्शन करने के लिए कर सकते हैं।

यह ट्यूटोरियल आपको मूल बातें और Sonic Pi के बारे में बताता है। इस ट्यूटोरियल के अंत में आप कुछ ऐसा बना पाएंगे:

{% include player.html filepath="/assets/audio/groove.mp3" %}

या इस तरह का कुछ:

{% include player.html filepath="/assets/audio/amen.mp3" %}

Sonic Pi सब की खोज है। कोई गलती नहीं हैं, केवल खोजें हैं। और सबसे बढ़कर, यह मज़ेदार है। इसलिए इसे याद रखें: मज़े करें, अन्वेषण करें और दूर हैक करें!

## Sonic Pi खोलें

यदि आपके पास Sonic Pi स्थापित नहीं है, तो <a href="http://sonic-pi.net/">sonic-pi.net</a>पर जाएं, Sonic Pi को डाउनलोड और इंस्टॉल करें। यह Windows, OS X और Linux ऑपरेटिंग सिस्टम के लिए उपलब्ध है।

इसके बाद, Sonic Pi को आग दें! आइए देखें कि यह कैसा दिखता है।

यह Sonic Pi इंटरफ़ेस है; इसकी तीन मुख्य खिड़कियाँ हैं। आपका कोड लिखने के लिए सबसे बड़ा है, और हम इसे programming panel कहते हैं। एक log panel भी है जो आपके प्रोग्राम के बारे में जानकारी दिखाता है क्योंकि यह चलता है। जब आप विंडो के शीर्ष पर सहायता बटन पर क्लिक करते हैं, तो तीसरा पैनल मदद दस्तावेज प्रदर्शित करता है। इसमें Sonic Pi प्रोग्रामिंग के लिए भाषा के बारे में जानकारी के साथ-साथ विभिन्न synth, नमूने, और बहुत कुछ शामिल हैं। ऐसे बहुत सारे रेडी-टू-गो उदाहरण हैं जिन्हें आप आजमा सकते हैं और उपयोग कर सकते हैं!

<img src="{{ "/assets/img/interface_hi.png" | prepend: site.baseurl}}">
<p class="center"><small><i>Sonic Pi interface</i></small></p>

## एक नोट खेलो

नोट चलाने के लिए Sonic Pi प्रोग्रामिंग के साथ शुरू करते हैं। `Buffer 0` टैब चुनें और टाइप करें:

{% highlight ruby %}
play 60
{% endhighlight %}

ऊपरी बाएँ कोने से **Run** दबाएं। क्या आप एक बीप सुन सकते हैं?

विभिन्न मूल्यों का प्रयास करें। उदाहरण के लिए लिखें `play 50` या `play 70`.  ध्वनि कैसे बदलती है?

अब `pley 60` लिखने का प्रयास करें और run पर क्लिक करें। क्या होता है?

> यह आपके कोड में बग का एक उदाहरण है। बाद की गतिविधियों में, यदि त्रुटि पैनल पाठ प्रदर्शित करता है तो आपको पता चल जाएगा कि आपके पास एक बग है जिसे आपको ठीक करने की आवश्यकता है। यह हो सकता है कि आपने किसी शब्द को `play` की तरह गलत किया हो।

आपके द्वारा उपयोग किए गए नंबर _MIDI नोट_  हैं। MIDI एक उपयोगी तरीका है रचना करना और अपने नोट्स को जल्दी से जांचने और उनके मूल्य को कम करके उन्हें समायोजित करना (अपने नोट को कम करना) या इसे बढ़ाना, (पिच को उच्च बनाना) के लिए एक उपयोगी उपकरण है। Sonic Pi MIDI नोट संख्या (0 और 127 के बीच का मान) और पारंपरिक संगीत संकेतन (जैसे: `:C4`, `:Eb3` या `:G5`) से परिचित है।