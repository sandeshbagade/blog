---
layout: post
title: Using mutt to send a few hundred of emails using python script
date: 2017-02-21T23:32:00.000Z
published: true
tags:
  - python
categories:
  - python
---

So this was my first encounter with the powerful email client MUTT. According to the official website of MUTT, "All web clients sucks but this one sucks less". This is the best way to explain something.

**GitHub repository for the code:**

[https://github.com/singh1114/csiMuttScript](https://github.com/singh1114/csiMuttScript)

So, let's go through the build-up and share the story of WHY I decided to write use MUTT client.

## What was the reason to use MUTT

So I went to my friend's room in the hostel and he was asking his roommate to send emails to a list of people. He had the database of the students with him for which he was going to use to send the emails.

He told me that he has the database of the registered student for some event and all the data is present in a CSV format. He gave the database to his roommate and asked him to send the email to each one of them. I asked him about the procedure that he was going to follow. Very sincerely he told me that he will pick all of the emails one by one and send them the email.

I laughed to this as I knew there were more than a hundred people in the list. I knew that if he went forward by following this procedure he might not be able to complete it till morning. So I asked him to allow me to do the work for him. I assured him that I will write a program that will complete the work faster.

So he gave me the database and I started working on it. The first and very obvious thing that can come to someone's mind is that we can convert the database into CSV(comma-separated values) file and import it using google sheets which allows direct importing of contacts from CSV file.

I asked my friend and he said that they don't want everyone to know about each other's email ID.

He told me that what he wants to do is that he can send the email in a loop. So that the privacy of each member is preserved.

I remembered that my mentor used to talk about MUTT, using which we can send emails through the terminal and if we can do something using the terminal, we can configure it according to our needs.

So, I went forward to install MUTT and started reading about it. Finally, I found a great article that I followed during the build process. The following link will take you to the article.

[http://nickdesaulniers.github.io/blog/2016/06/18/mutt-gmail-ubuntu/](http://nickdesaulniers.github.io/blog/2016/06/18/mutt-gmail-ubuntu/)

After that, I wrote a small program in python that can read each line of CSV file and differentiate between all the values in the file and store the email in a variable. First of all, I searched about how to execute bash commands in a python program. "subprocess" was the solution to my problem so I imported it.

I tested it by sending a few emails to my friends. It worked fine. Then I wrote another file and asked my friend about the content that he wanted to send to the list. He told me a few things and I used my open source capabilities to write the content (Collaborating in a big project is initiated by a good conversation).

I tested the script and found that for every mail we have to tell the system that whatever we were doing was correct and we want to go forward. So there was a lot of pressing "Enter" key. I wanted to remove that too but wasn't able to in the time. I explain to my friend how to carry out the procedure as I was in no mood of doing all those clicks.

When he ended up sending all the emails. I found the solution and corrected the single character in my file. This commit shows the way in which I solved the problem.

[Mutt script commit](https://github.com/singh1114/csiMuttScript/commit/75f2eccb6928fdb3994390283ebe205cf17d4bbb)
