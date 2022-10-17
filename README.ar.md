# 💬 نقاش: Kubernetes للمبتدئين

```text
Dauer:      1h 30min - 2h
Niveau:     Einsteiger (keine Vorkenntnisse notwendig)
Zielgruppe: Docker-User, die Kubernetes nutzen wollen
Sprache:    Deutsch
Author:     André Lademann <vergissberlin@gmail.com>
```

## الهدف من الحديث

في نهاية الحديث ، سوف تظهر كيف يمكنك التعامل بشكل أساسي مع Kubernetes. يمكنك نشر وتوسيع حاويات Docker في Kubernetes. يمكنك إعداد وإدارة مجموعات Kubernetes.

## المتطلبات

-   [ ] كمبيوتر محمول مثبت عليه Docker
-   [ ] حساب Docker Hub
-   [ ] حساب جيثب
-   [ ] (اختياري) Kubernetes Cluster
-   [ ] (optional) Google Cloud Account
-   [ ] (اختياري) Google Cloud SDK
-   [ ] (اختياري) Google Cloud Shell

إذا لم تستوف جميع النقاط ، فلا توجد مشكلة. معا سنحقق النقاط التي لم تحققها.

* * *

## مصلحات

### كوبرنيتيس

Kubernetes عبارة عن نظام أساسي مفتوح المصدر لأتمتة نشر التطبيقات المعبأة في حاويات وتوسيع نطاقها وإدارتها.

#### حاوية Kubernetes

حاوية Kubernetes هي نسخة قابلة للتنفيذ من صورة Docker. الحاوية هي بيئة معزولة تتكون من عدد من الطبقات. تحتوي كل طبقة على مجموعة من التعليمات التي يتم تنفيذها عند إنشاء الحاوية. إذا كانت الحاوية تحتوي على طبقات متعددة ، فسيتم استخدام الطبقة الأخيرة كقاعدة ويتم إضافة الطبقات السابقة كتراكب.

#### القرون Kubernetes

الكبسولة عبارة عن مجموعة من حاوية واحدة أو أكثر تعمل معًا وتشترك في نفس موارد التخزين والشبكة. الكبسولة هي أصغر وحدة يمكن إنشاؤها وإدارتها في Kubernetes.

#### خدمات Kubernetes

الخدمة عبارة عن تجريد يمثل مجموعة من الكبسولات كمجموعة منطقية. تسمح الخدمات للقرون بالعثور على بعضها والتحدث مع بعضها البعض دون معرفة البودات ببعضها البعض. يمكن أيضًا استخدام الخدمات لتوزيع البودات عبر مجموعة.

#### عقد Kubernetes

العقدة هي آلة افتراضية أو فعلية تقوم بتشغيل كبسولات Kubernetes. يمكن للعقدة تشغيل حجرة واحدة أو أكثر.

### مجموعات Kubernetes

المجموعة عبارة عن مجموعة من العقد تعمل معًا لتشغيل التطبيقات ذات الحاويات. تتكون المجموعة من عقدة رئيسية واحدة على الأقل والعديد من العقد العاملة.

## تشابك الايدى

# ورشة عمل - من Docker إلى Kubernetes

## كوبرنيتيس

### MiniKube مقابل Docker Desktop و Rancher Desktop و Kind

هناك عدة طرق لتثبيت Kubernetes محليًا. سنركز على تثبيت MiniKube هنا.

Möchtest Du mehr über die jeweiligen Vor- und Nachteile erfahren, kannst Du gerne [هنا](https://itnext.io/goodbye-docker-desktop-hello-minikube-3649f2a1c469)قرأ.

#### سطح المكتب Docker

-   التثبيت المحلي لـ Kubernetes
-   التثبيت المحلي لـ Docker
-   استخدام صور Docker
-   إدارة Kubernetes عبر Docker Desktop
-   يحدد لاحقًا

##### تثبيت Docker Desktop

1.  تركيب[سطح المكتب Docker](https://www.docker.com/products/docker-desktop)

#### رانشر سطح المكتب

-   التثبيت المحلي لـ Kubernetes
-   التثبيت المحلي لـ Docker
-   يحدد لاحقًا

#### البشع

-   التثبيت المحلي لـ Kubernetes
-   يحدد لاحقًا

##### تثبيت برنامج MiniKube

1.  تركيب[البشع](https://minikube.sigs.k8s.io/docs/start/)
2.  تكوين الاختصار لـ minikube في shell (على سبيل المثال`alias minikube="minikube.exe"`)
3.  تركيب[kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/)
4.  تكوين الاختصار لـ kubectl في shell (على سبيل المثال`alias kubectl="kubectl.exe"`)

##### بدء مجموعة Kubernetes

1.  ابدأ مجموعة Kubernetes باستخدام`minikube start`

##### لوحة تحكم Kubernetes

1.  ابدأ تشغيل Kubernetes Dashboard باستخدام`minikube dashboard`

### إطلاق جراب

1.  إنشاء جراب مع`kubectl run hello-world --image=hello-world`
2.  فحص الجراب مع`kubectl get pods`
3.  الاستخراج من القرون مع`kubectl get deployments`
4.  تعليمات للقرون ذات`kubectl describe pods`

* * *

## الحد الأدنى

في هذه المقالة تناولنا أساسيات Docker و Kubernetes. لقد رأينا كيف يتم استخدام Docker لإنشاء الحاويات وإدارتها. لقد رأينا أيضًا كيف يتم استخدام Kubernetes لإدارة التطبيقات المعبأة في حاويات. لقد رأينا أيضًا كيف يعمل Docker و Kubernetes معًا.
