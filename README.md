# Module15_AmazonAWS

Instructions
This section divides the Challenge instructions into the following three steps:

Configure the initial robo advisor

Build and test the robo advisor

Enhance the robo advisor with an Amazon Lambda function

Step 1: Configure the Initial Robo Advisor
In this section, you create the robo advisor bot and add an intent with its corresponding slots. To do so, complete the following steps:

Sign in to your AWS Management Console, and then create a new custom Amazon Lex bot (Links to an external site.). Use the following criteria:

Bot name: RoboAdvisor

Language: English (US)

Output voice: Salli

Session timeout: 5 minutes

Sentiment analysis: No

COPPA: No

Advanced options: No

All other options: The default value

Add a new intent, and name it recommendPortfolio.

Configure sample utterances as follows (you can add more utterances if you want):

I want to save money for my retirement

I'm {age} and I would like to invest for my retirement

I'm ​{age} and I want to invest for my retirement

I want the best option to invest for my retirement

I'm worried about my retirement

I want to invest for my retirement

I would like to invest for my retirement

Create four slots, as the following image specifies:

A table specifies the name, slot type, and prompt for each of the four slots.

IMPORTANT
Remember to mark all the slots as required, as the following image shows:

A screenshot depicts the Required checkbox selected for each of the four slots.

Move to the “Confirmation prompt” section, and then set the following messages:

Confirm: Thanks, now I will look for the best investment portfolio for you.

Cancel: I will be pleased to assist you in the future.

Step 2: Build and Test the Robo Advisor
In this section, you build and test your robo advisor. To do so, complete the following steps:

To build your bot, click the Build button (in the upper-right corner of the page).

When the build finishes, test it in the “Test bot” pane. The following animation shows a sample test conversation:

An animation depicts testing the bot.

In the preceding animation, a user starts a dialogue with the robo advisor. The dialogue is as follows:

 User: I want to invest for my retirement

 Robo advisor: Thank you for trusting me to help, could you please give me your name?

 User: Arturo

 Robo advisor: How old are you?

 User: 42

 Robo advisor: How much do you want to invest?
 
 User: 4000

 Robo advisor: What level of investment risk would you like to take? (None, Low, Medium, High)

 User: Low
 
 Robo advisor: Thanks, now I will look for the best investment portfolio for you.
Record a video or create an animated GIF of the working bot.

HINT
Step 3: Enhance the Robo Advisor with an Amazon Lambda Function
In this section, you create an Amazon Lambda function to validate the data that a user supplies during a conversation with the robo advisor. To do so, complete the following steps:

Create a new Lambda function from scratch, and name it recommendPortfolio. Choose Python 3.7 as the runtime programming language.

In the online code editor, delete the AWS-generated default lines of code, and then paste in the provided starter code from lambda_function.py.

Complete the recommend_portfolio function by adding the following validation rules:

The value of age should be greater than zero and less than 65.

The value of investment_amount should be greater than or equal to 5000.

Complete the starter code so that once the intent is fulfilled, the bot responds with an investment recommendation based on the selected risk level, as follows:

None: “100% bonds (AGG), 0% equities (SPY)”

Low: “60% bonds (AGG), 40% equities (SPY)”

Medium: “40% bonds (AGG), 60% equities (SPY)”

High: “20% bonds (AGG), 80% equities (SPY)”

HINT
When you finish coding your Lambda function, test it by using the provided test events.

After successfully testing your code, open the Amazon Lex console, and then navigate to the recommendPortfolio bot configuration. Integrate your new Lambda function into the bot by selecting it in the “Lambda initialization and validation” and “Fulfillment” sections.

Build your bot, and then test it with both valid and invalid data for the slots.

Record a video or create an animated GIF of the working bot.

Requirements
Step 1: Configure the Initial Robo Advisor (25 points)
To receive all points, you must:

Create a new custom Amazon Lex bot named RoboAdvisor, and add a new intent named recommendPortfolio. (10 points)

Configure some sample utterances. (5 points)

Create and configure slots. (5 points)

Configure the “Confirmation prompt” section. (5 points)

Step 2: Build and Test the Robo Advisor (20 points)
To receive all points, you must:

Successfully build and test the robo advisor, and either record a video or create an animated GIF of the working bot. (20 points)
Step 3: Enhance the Robo Advisor with an Amazon Lambda Function (55 points)
To receive all points, you must:

Create a new Lambda function from scratch named recommendPortfolio, and use Python 3.7 as the runtime programming language. (5 points)

Complete the recommend_portfolio function by adding the requested validation rules. (15 points)

Successfully implement the investment recommendations evidenced by the accuracy of the bot’s response. (15 points)

Integrate the Lambda function into the robo advisor bot, and either record a video or create an animated GIF of the working bot. (20 points)

Submission
To submit your Challenge assignment, click Submit, and then provide the URL of your GitHub repository for grading.