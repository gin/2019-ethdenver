# Aave: Bounty 5
Bounty 5 Overview: UX – Test ETHLend & Bless us with your Feedback

---

## Environment
(Latest versions as of 2019-02-16)  

__ETHLend version:__  
BAIJI V0.4 ALPHA

__Google Chrome version:__  
Desktop = Version 72.0.3626.109 (Official Build) (64-bit)  
Mobile = Version 72.0.3626.105

__MetaMask version:__  
6.0.1

---

## Feedback

### 01
__Page:__  
/signup

__Problem & User Story:__  
Dropdown menu is too narrow.  
Searching for "United State" took several tries. I searched for "USA", "America", then "United States".

![alt text][01-signup-dropdown-menu]

---

### 02
__Page:__  
/createwallet

__Problem & User Story:__  
Spacing in description text is off when window width is lower than 768px.  
When I looked at the "/createwallet" page on my phone (Galaxy S9+) on Chrome mobile browser, the spacing is off. Other popular phones where the resolution is lower than 768px when on Chrome mobile browser includes iPhoneX (375px), Pixel2 (411px), Pixel 2XL (411px).

![alt text][02-createwallet-responsive-spacing-on-mobile =411x]

![alt text][02-createwallet-responsive-767]

---

### 03
__Page:__  
/borrowcreate  
1. Fill out form
2. Click on "Overview" button, and wait for modal to be visible
3. Mouse over or click on the fa-question-circle icon next to "Collateral Safetiness"

Expect tooltip with additional information about "Collateral Safetiness"

__Problem & User Story:__  
The "Your Loan Detail" modal's fa-question-circle icon does not provide information to user.
When I mouse hover over (or click) the fa-question-circle icon, I expect additional information similar to other pages on ETHLend.

![alt text][03-borrowcreate-your-loan-detail-modal-fa-question-circle]

---

### 04
__Page:__  
/home  
1. Click on "Lend" button
2. Click on "Create" button  

Expect not to restart from the beginning

__Problem & User Story:__  
The "Create" button here might not make sense.  
Maybe remove this button, and reword this section to something like "You can fulfill a borrower's loan request at the marketplace".  
Or keep the button but create webpages for creating loan offers. This is uncommon though. P2P lending platforms like Lending Club, Prosper, SoFi does not do this probably because trade volume is not high enough where doing it like an exchange (bid/ask model) makes sense. 

![alt text][04-home-lend]

---

### 05
__Page:__  
/borrowcreate
1. Fill out form with a very small amount of collateral, and "DAI" or "LEND" as loan currency 
e.g. collateral = 0.0001ETH or 0.001ETH or 0.01ETH or 0.1ETH or 1ETH
2. Click on "Proceed" button
3. Fill out the form  
e.g. duration = 30days or 60days, monthly interest = 0.25% or 0.5%
4. Click on "Overview" button
5. Click on "Create" button

__Problem & User Story:__  
At the end of this user flow, there is an error message saying there is not enough funds in user's wallet to complete this action even though there is enough in MetaMask (Tried using Main Ethererum Network, and Rinkeby Test Network).  
I'm not sure what is causing this error. I tried several different the parameters (in the e.g. listed above), and tried using other user flow paths.

---

### 06
__Page:__  
/borrowcreate

__General feedback:__  
The main functionality is contained inside a visually small div (e.g. create-loan-control) instead of using the entire height of user's browser. This increases the amount of scrolling that user has to do. Decreasing this leads to better UX. Other pages in ETHLend are good, making this page's create-loan-control div inconsistent with the other pages.

Bad
![alt text][06-borrowcreate-scroll-bad]
vs  
Good
![alt text][06-offer-scroll-good]

---

### 07
__Page:__  
Most pages

__General feedback:__   
When window width is 991px or lower, the menu (Header div) is collapsed. This is good. However, there is only 1 action ("New Loan Request") under the "Action" menu. Moving "New Loan Request" up one level could reduce a click.

<=991px
![alt text][07-most-pages-menu-single-item-bad]
vs  
\>992px
![alt text][07-most-pages-menu-single-item-good]

---

### 0
__Page:__  
/

__Problem & User Story:__  
.

![alt text][]














[01-signup-dropdown-menu]: ./img/01-signup-dropdown-menu.png

[02-createwallet-responsive-767]: ./img/02-createwallet-responsive-767.png
[02-createwallet-responsive-spacing-on-mobile]: ./img/02-createwallet-responsive-spacing-on-mobile.jpg
[03-borrowcreate-your-loan-detail-modal-fa-question-circle]: ./img/03-borrowcreate-your-loan-detail-modal-fa-question-circle.png

[04-home-lend]: ./img/04-home-lend.png

[06-borrowcreate-scroll-bad]: ./img/06-borrowcreate-scroll-bad.png
[06-offer-scroll-good]: ./img/06-offer-scroll-good.png

[07-most-pages-menu-single-item-bad]:  ./img/07-most-pages-menu-single-item-bad.png
[07-most-pages-menu-single-item-good]:  ./img/07-most-pages-menu-single-item-good.png