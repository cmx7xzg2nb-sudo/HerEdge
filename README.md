=# HerEdge
Finance Career Orientation Quiz
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Finance Career Orientation Quiz</title>
    <style>
        body { font-family: Arial, sans-serif; background-color: #f4f4f4; color: #333; }
        h1 { text-align: center; }
        form { max-width: 600px; margin: auto; background: #fff; padding: 20px; border-radius: 5px; }
        .question { margin-bottom: 15px; }
        .results { display: none; padding: 20px; background: #e7f7e7; }
        #share { display: none; margin-top: 20px; }
    </style>
</head>
<body>
    <h1>Finance Career Orientation Quiz</h1>
    <form id="quizForm">
        <div class="question">
            <label>1. What is your primary career interest?</label><br>
            <select name="interest">
                <option value="investment">Investment Analyst</option>
                <option value="banking">Investment Banking</option>
                <option value="consulting">Financial Consulting</option>
                <option value="accounting">Accounting</option>
            </select>
        </div>
        <div class="question">
            <label>2. What is your current level of education?</label><br>
            <select name="education">
                <option value="highschool">High School</option>
                <option value="bachelor">Bachelor's Degree</option>
                <option value="master">Master's Degree</option>
                <option value="phd">PhD</option>
            </select>
        </div>
        <div class="question">
            <label>3. How would you rate your analytical skills?</label><br>
            <select name="analyticalSkills">
                <option value="excellent">Excellent</option>
                <option value="good">Good</option>
                <option value="average">Average</option>
                <option value="poor">Poor</option>
            </select>
        </div>
        <div class="question">
            <label>4. Do you have experience with financial modeling?</label><br>
            <select name="financialModeling">
                <option value="yes">Yes</option>
                <option value="no">No</option>
            </select>
        </div>
        <div class="question">
            <label>5. Which role do you envision yourself in 5 years?</label><br>
            <select name="futureRole">
                <option value="seniorAnalyst">Senior Analyst</option>
                <option value="manager">Manager</option>
                <option value="executive">Executive</option>
                <option value="entrepreneur">Entrepreneur</option>
            </select>
        </div>
        <div class="question">
            <label>6. Are you skilled in using Excel?</label><br>
            <select name="excelSkills">
                <option value="excellent">Excellent</option>
                <option value="good">Good</option>
                <option value="average">Average</option>
                <option value="poor">Poor</option>
            </select>
        </div>
        <div class="question">
            <label>7. How comfortable are you with public speaking?</label><br>
            <select name="publicSpeaking">
                <option value="veryComfortable">Very Comfortable</option>
                <option value="comfortable">Comfortable</option>
                <option value="neutral">Neutral</option>
                <option value="uncomfortable">Uncomfortable</option>
            </select>
        </div>
        <div class="question">
            <label>8. What motivates you to work in finance?</label><br>
            <select name="motivation">
                <option value="money">Financial Gain</option>
                <option value="passion">Passion for Finance</option>
                <option value="helpOthers">Helping Others</option>
                <option value="prestige">Prestige of the Job</option>
            </select>
        </div>
        <div class="question">
            <label>9. How do you view risk in financial decisions?</label><br>
            <select name="riskView">
                <option value="calculated">Calculated Risks</option>
                <option value="avoid">Avoid Risks</option>
                <option value="embrace">Embrace Risks</option>
                <option value="uncertain">Uncertain</option>
            </select>
        </div>
        <div class="question">
            <label>10. How well do you handle stress?</label><br>
            <select name="stressHandling">
                <option value="excellent">Excellent</option>
                <option value="good">Good</option>
                <option value="average">Average</option>
                <option value="poor">Poor</option>
            </select>
        </div>
        <div class="question">
            <label>11. Do you enjoy working in teams?</label><br>
            <select name="teamWork">
                <option value="yes">Yes</option>
                <option value="no">No</option>
            </select>
        </div>
        <div class="question">
            <label>12. What is your preferred work environment?</label><br>
            <select name="workEnvironment">
                <option value="corporate">Corporate Setting</option>
                <option value="startup">Startup Environment</option>
                <option value="remote">Remote Work</option>
                <option value="flexible">Flexible Work Environment</option>
            </select>
        </div>
        <div class="question">
            <label>13. Have you taken any finance-related certifications?</label><br>
            <select name="certifications">
                <option value="yes">Yes</option>
                <option value="no">No</option>
            </select>
        </div>
        <div class="question">
            <label>14. Would you like to pursue further education?</label><br>
            <select name="furtherEducation">
                <option value="yes">Yes</option>
                <option value="no">No</option>
            </select>
        </div>
        <div class="question">
            <label>15. Are you interested in networking opportunities?</label><br>
            <select name="networking">
                <option value="yes">Yes</option>
                <option value="no">No</option>
            </select>
        </div>
        <button type="button" onclick="calculateResults()">Submit</button>
    </form>
    <div class="results" id="results"></div>
    <div id="share">
        <h3>Share Your Results:</h3>
        <a id="twitterShare" href="#">Share on Twitter</a><br>
        <a id="facebookShare" href="#">Share on Facebook</a>
    </div>
    <script>
        function calculateResults() {
            const form = document.getElementById('quizForm');
            const resultsDiv = document.getElementById('results');
            let recommendations = [];

            // Sample recommendations based on selections
            if (form.interest.value === 'investment') {
                recommendations.push('Consider roles such as Investment Analyst or Portfolio Manager.');
            } else if (form.interest.value === 'banking') {
                recommendations.push('Explore Investment Banking positions or Mortgage Advising.');
            } else if (form.interest.value === 'consulting') {
                recommendations.push('Look into Financial Consultant roles or Advisory Services.');
            } else if (form.interest.value === 'accounting') {
                recommendations.push('Accountancy roles or Forensic Accounting might suit you.');
            }

            // Display score or result
            resultsDiv.innerHTML = '<h2>Your Career Recommendations:</h2><p>' + recommendations.join('\n') + '</p>';
            resultsDiv.style.display = 'block';
            document.getElementById('share').style.display = 'block';

            // Social sharing links
            const shareUrl = window.location.href;
            document.getElementById('twitterShare').href = 'https://twitter.com/share?url=' + encodeURIComponent(shareUrl) + '&text=Check%20out%20my%20Finance%20Career%20Quiz%20results!';
            document.getElementById('facebookShare').href = 'https://www.facebook.com/sharer/sharer.php?u=' + encodeURIComponent(shareUrl);
        }
    </script>
</body>
</html>