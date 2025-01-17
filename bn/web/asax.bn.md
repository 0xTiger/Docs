{
  "date": "2019-10-11",
  "keywords": [
    "asax",
    "asax file",
    "asax file format",
    "asax file type",
    "file",
    "type",
    "what is an asax file"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "ASAX - ASP.NET সার্ভার অ্যাপ্লিকেশন ফাইল",
  "description": "একটি ASAX ফাইল এবং APIগুলি কী যা ASAX ফাইলগুলি তৈরি এবং খুলতে পারে তা জানতে শিখুন৷",
  "linktitle": "ASAX",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-asax-bn"
    }
  },
  "lastmod": "2021-06-07"
}

## একটি ASAX ফাইল কি?

.asax এক্সটেনশন সহ একটি ফাইল হল ASP.NET অ্যাপ্লিকেশন দ্বারা ব্যবহৃত একটি ফাইল যা সার্ভারের পাশে থাকে। এটিতে ASP.NET বা HTTP মডিউল দ্বারা উত্থাপিত অ্যাপ্লিকেশন-স্তর এবং সেশন-স্তরের ইভেন্টগুলির প্রতিক্রিয়া করার জন্য কোড রয়েছে৷ অ্যাপ্লিকেশন লঞ্চ বা বন্ধ হয়ে গেলে কিছু ইভেন্ট পরিচালনা করাও এতে অন্তর্ভুক্ত থাকে। ASAX ফাইলগুলি ঐচ্ছিক এবং গ্লোবাল লেভেলে অ্যাপ্লিকেশন-লেভেল ইভেন্ট এবং ত্রুটিগুলি পরিচালনা করতে ওয়েব অ্যাপ্লিকেশনগুলিতে শুধুমাত্র একটি ASAX ফাইল যুক্ত করা হয়৷ ASPX পৃষ্ঠাগুলির বিপরীতে, ASAX ফাইলগুলিতে অ্যাপ্লিকেশনটির কার্যকারিতা বাস্তবায়নের জন্য কোনো কোড থাকে না।

## ASAX ফাইল ফরম্যাট

ASAX ফাইলগুলি প্লেইন টেক্সট ফাইল ফরম্যাটে লেখা হয় এবং মানুষের পঠনযোগ্য। সর্বাধিক ব্যবহৃত ASAX ফাইল হল Global.asax যা একটি ASP.NET অ্যাপ্লিকেশনের রুট ডিরেক্টরিতে থাকে। ব্যবহারকারীদের এই ফাইলের কোড ডাউনলোড বা দেখতে নিষেধ করতে ওয়েব সার্ভারগুলি এই ফাইলে যেকোন ইনকামিং কল প্রত্যাখ্যান করার জন্য কনফিগার করা হয়েছে৷

### Global.ASAX - ASAX ফাইল ফরম্যাটের একটি উদাহরণ

একটি একক ASAX ফাইল একাধিক বিভাগ নিয়ে গঠিত যা অ্যাপ্লিকেশন-স্তরের ইভেন্টগুলি পরিচালনা করার জন্য লেখা হয়। এগুলো নিম্নরূপ।

 * **অ্যাপ্লিকেশন নির্দেশাবলী** - অ্যাপ্লিকেশন নির্দেশাবলী হল এমন ট্যাগ যা Global.asax ফাইল প্রক্রিয়া করার সময় ASP.NET পার্সার দ্বারা ব্যবহার করা ঐচ্ছিক অ্যাপ্লিকেশন-নির্দিষ্ট সেটিংস সংজ্ঞায়িত করতে ব্যবহৃত হয়। এই নির্দেশিকাগুলি Global.asax ফাইলের শুরুতে অবস্থিত এবং অনুসরণ হিসাবে সংজ্ঞায়িত করা হয়েছে।

```
<%@ নির্দেশিক বৈশিষ্ট্য=মান [অ্যাট্রিবিউট=মান … ]%>
```
 * **কোড ঘোষণা ব্লক** - কোড-ঘোষণা ব্লকগুলি সার্ভার কোডের বিভাগগুলিকে সংজ্ঞায়িত করতে ব্যবহার করা হয় যেগুলি ASP.NET অ্যাপ্লিকেশন ফাইলগুলিতে এমবেড করা হয়।<script> blocks marked with a runat=server attribute. The following example shows how you can define event-handling logic for the EnterBtn_Click event.

```
<html>
  <script language="C#" runat="server">
      void EnterBtn_Click(Object Src, EventArgs E) {
          Message.Text = "Hi " + Name.Text + ", welcome to ASP.NET!";
  }
  </script>

  <body>
   <form runat="server">
    Enter your name: <asp:textbox id="Name" runat=server/>
                     <asp:button text="Enter" Onclick="EnterBtn_Click" runat="server"/>
        <p>
        <asp:label id="Message" runat=server/>
    </form>
  </body>
</html>
```
 * **কোড রেন্ডার ব্লক** - এগুলি ইনলাইন কোড বা এক্সপ্রেশনগুলিকে সংজ্ঞায়িত করে যা পৃষ্ঠাটি রেন্ডার করার সময় কার্যকর হয়। কোড রেন্ডার ব্লকের দুটি শৈলীর মধ্যে ইনলাইন কোড এবং ইনলাইন এক্সপ্রেশন রয়েছে। পূর্বেরটি স্বয়ংসম্পূর্ণ লাইন বা কোডের ব্লকগুলিকে সংজ্ঞায়িত করতে ব্যবহৃত হয়, যখন পার্শ্বীয়টি লিখন পদ্ধতিতে কল করার জন্য একটি শর্টকাট হিসাবে ব্যবহৃত হয়।

## তথ্যসূত্র

 * [HTTP হ্যান্ডলার এবং HTTP মডিউল ওভারভিউ](https://msdn.microsoft.com/en-us/library/bb398986(v=vs.100))
 * [Global.asax Syntax](https://learn.microsoft.com/en-us/previous-versions/dotnet/netframework-4.0/2027ewzw(v=vs.100))

