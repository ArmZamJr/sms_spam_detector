# sms_spam_detector
Module 21 Challenge

### sms_text_classification_solutions.ipynb
## Build a Pipeline with the vectorizer and SVM model.
```#  Build a pipeline using `TfidfVectorizer()`, without `stopwords='english`, and `LinearSVC()`.
text_clf = Pipeline([('tfidf', TfidfVectorizer()),('clf', LinearSVC()),])

# Fit the model to the transformed data.
text_clf.fit(X_train, y_train)```

### gradio_sms_text_classification.ipynb
```Help from Gemini
# Create a sms_app that takes a textbox for the inputs and has a textbox for the output.  
# Povide labels for each textbox. 
#sms_app = gr.Interface(fn=sms_prediction, inputs="text", outputs="text")
interface = gr.Interface(
    fn=sms_prediction,
    inputs="text",
    outputs="text",
    title="SMS Spam Detection",
    description="Please enter an SMS message below to determine if it is spam or not."
)


    
# Launch the app.
sms_app.launch()
```
