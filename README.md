Summary: Email Marketing can be defined as a marketing technique in which businesses stay connected with their customers through emails, making them aware about their new products, updates, important notices related to the products they are using. My problem statement was to use different features of email like email campaign, past communications, etc (from provided data frame) and predict how the cx will response for email. The cx can neglect the email, read it or acknowledge the email. The more the cx acknowledge the email, the sucessful the campaign is. I recieved a data frame with the following column:

Email Id - It contains the email id's of the customers/individuals 
Email Type - There are two categories 1 and 2. We can think of them as marketing emails or important updates, notices like emails regarding the business. 
Subject Hotness Score - It is the email's subject's score on the basis of how good and effective the content is. 
Email Source - It represents the source of the email like sales and marketing or important admin mails related to the product. 
Email Campaign Type - The campaign type of the email. 
Total Past Communications - This column contains the total previous mails from the same source, the number of communications had. 
Customer Location - Contains demographical data of the customer, the location where the customer resides. 
Time Email sent Category - It has three categories 1,2 and 3; the time of the day when the email was sent, we can think of it as morning, evening and night time slots. 
Word Count - The number of words contained in the email. 
Total links - Number of links in the email. 
Total Images - Number of images in the email. 
Email Status - Our target variable which contains whether the mail was ignored, read, acknowledged by the reader.

I started my analysis with checking null values, I filled them up with mean and mode according to it's distribution. During EDA, I also saw the distribution of email neglected, read and acknowledged w.r.t. different continous and categorical features(as mentioned above and in detail in colab). I also plotted detailed graph of distribution.

Further, in next section, I analyzed the corelation between different different features. I also checked the VIF, used IQR stat technique to check outliers and did one-hot encoding before model building as this problem had a number of categorical variable.

In the model building part, I checked that the data was highly embalanced. I used random undersampling and SMOTE technique to create different train data set for different model and checked the model scores for them individually. XGB performed the best, thus I accepted it final model.
