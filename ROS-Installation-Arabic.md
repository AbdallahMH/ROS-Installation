## <h1 dir='rtl' align='right'>🤖  شرح تثبيت (نظام تشغيل الروبوت (ROS noetic)  على نظام الأوبينتو (Ubuntu 20.04) </h1>

<p dir='rtl' align='right'> بادئ ذي بدء، يجب علينا التأكد من بعض الأمور قبل الشروع في تثبيت نظام تشغيل الروبوت (ROS noetic) </p>
<p dir='rtl' align='right'>  تأكد من إصدار توزيعة الأوبينتو، يجب أن يكون نفس الإصدار هذا (Ubuntu 20.04). </p>


<blockquote> <p dir='rtl' align='right'> تستطيع التأكد من الإصدار عن طريق كتابة الأمر التالي في سطر الأوامر  <code> lsb_release -a</code>  </p> </blockquote> 


<p dir='rtl' align='right'>  قم بتهيئة توزيعة الأوبينتو للسماح بـ
  <code>"restricted"و"universe" و"multiverse</code> 🔗 <a href="https://help.ubuntu.com/community/Repositories/Ubuntu"> اتّبع هذا الشرح </a>
</p>

    
-------------------------------------

### <h1 dir='rtl' align='right'> افتح سطر الأوامر في الأوبينتو واتّبع الخطوات التالية: </h1>

##  <h2 dir='rtl' align='right'>📝 1. إعداد ملف source.list </h2>

<p dir='rtl' align='right'> قم بإضافة الأمر التالي للسماح لجهازك بالتحميل من <code>packages.ros.org</code>. </p>

<p dir='rtl'> <code>
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'.
  </code> </p>
    
-------------------------------------
## <h2 dir="rtl"> 🔑 2. إعداد المفاتيح </h2>
<p dir="rtl"> أضف الأمر التالي في سطر الأوامر:
 <br>
 <code>
sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
</code>
</p>  
    
-------------------------------------
## <h2 dir="rtl"> 📥 3. تثبيت نظام تشغيل الروبوت </h2>
<p dir="rtl"> بداية، تأكّد من تحديث حزمة الديبيان، عن طريق الأمر: <br> <code> sudo apt update </code> </p>
<p dir="rtl"> والآن قم باختيار النسخة التي تريد تثبيتها: <p dir="rtl">

<p dir="rtl"> 1-تثبيت نسخة سطح المكتب الكاملة(يُنصح بها): كل برامج سطح مكتب بالإضافة إلى محاكاة ثنائية وثلاثية الأبعاد وحزم تصوّريّة ثنائية وثلاثية الأبعاد.
  <br>
 <code>
sudo apt install ros-noetic-desktop-full
 </code>
</p>

 <p dir="rtl"> 2.تثبيت نسخة سطح المكتب: كل مافي نسخة 'ROS-BASE' بالإضافة إلى أدوات مثل، 'rqt' & 'rviz'
  <br>
 <code>
sudo apt install ros-noetic-desktop
 </code>
  </p>

<p dir="rtl"> 3.نسخة 'ROS-BASE' الهيكل العظمي للنظام تشغيل الروبوت؛ مكتبات البناء والاتصال. بدون أدوات الواجهة الرسومية.
 <br>
 <code>
sudo apt install ros-noetic-ros-base
</code>
</p>
    
-------------------------------------
## <h2 dir="rtl"> 💻 4. إعداد البيئة </h2>
<p dir="rtl">
يجب عليك كتابة الأمر التالي كل مرّة عند تشغيل سطر الأوامر لتستخدم نظام تشغيل الروبوت:
<br> <code>
source /opt/ros/noetic/setup.bash
</code>
</p>

<p dir="rtl"> لكن من المفيد أن يتم تنفيذ ذلك الأمر بشكلٍ مؤتمت عند فتح سطر الأوامر.
مفسّر سطر الأوامر (Bash)
<br>
  
<code>
echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc </code> <br> <code>
source ~/.bashrc
  </code>
  <br>
  </p>
  <p dir="rtl"> مترجم للأوامر في نظام تشغيل يونكس (Zsh)
  <br>
    <code>
      echo "source /opt/ros/noetic/setup.zsh" >> ~/.zshrc </code> <br> <code>
source ~/.zshrc
</code>
</p>
    
-------------------------------------
## <h2 dir="rtl"> ☑️ قائمة الأعمال </h2>

<p dir="rtl">
 مٌبارك انتهينا من تثبيت نظام تشغيل الروبوت.
  <br>
  <b> لمراجعة أعمالنا </b>
  <br>
  ✅ تثبيت أوبينتو 20.04 (Ubuntu 20.04)
  <br>
  ✅ تثبيت نظام تشغيل الروبوت (ROS Noetic)
  <br>
  ❎ اختبار نظام التشغيل ومراجعة الشروحات.
</p>
<p dir="rtl"> للبدء بتنفيذ آخر عمل من القائمة، أنصح بالاطلاع على المرجع الرسمي لنظام تشغيل الروبوت  🔗 <a href="http://wiki.ros.org/ROS/Tutorials"> ROS offical Tutorials </a> </p>
