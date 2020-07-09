---
title: "My Feedback about CKA and CKAD"
date: 2020-07-08T06:00:15+06:00
hero: /assets/images/cka-ckad-feedback/kubernetes-cka-ckad.png
author:
  name: Ismail KABOUBI
  image: /assets/images/avatar.png
categories:
- cka-ckad-feedback

---

I recently had the opportunity to pass Certified Kubernetes Application Developer Exam as a beta tester, one month before I’ve passed the Certified Kubernetes Administrator Exam.

The two exams are hand-on performance-based. So, I’ve practiced Kubernetes for a period before passing them. CKA and CKAD exams are managed by CNCF (Cloud Native Computing Foundation) and cost me $300 per exam. To register for CKA and CKAD exam, you need to create an account in cncf.io plateform and purchase a $300 vouchers.

## Certifications

![certs](/assets/images/cka-ckad-feedback/cka-ckad.png)

## Training

As I said, the two exams are hand-on based labs. Practicing Kubernetes was my primary focus. I had the chance to adpot k8s in the company where I worked since the version 1.2 of Kubernetes.

I first started by the Scalable Microservices with Kubernetes training instructed by Kelsey Hightower and Carter Morgan from Google. Despite the fact that the training was not very advanced, but I found it very useful as good beginning to discover the tool.

After that, I’ve tried to install a Kubernetes cluster on Amazon Web Services. Meanwhile, the are no automatic tool like kops or kube-aws to install the cluster automatically by launching a set of command lines. Although it was a little bit complicated, I very appreciated the experience because I learned the core components of the tool and how to configure separately.

When I changed the company in mid-2017, I had not only the opportunity to have access to the CNCF official training for the CKA exam, but also I participated to rewarding missions to put in place Kubernetes in different platforms from bare metal to cloud solutions.

To sum up, this is my path to prepare the CKA and CKAD certifications:

* [Scalable Microservices with Kubernetes (free).](https://www.udacity.com/course/scalable-microservices-with-kubernetes--ud615)
* [Introduction to Kubernetes by the Linux foundation on EDX (free).](https://www.edx.org/course/introduction-to-kubernetes)
* [Kubernetes Fundamentals (paid).](https://www.cncf.io/certification/training/)
* [Kuberntes The Hard Way by Kelsey Hightower(free).](https://github.com/kelseyhightower/kubernetes-the-hard-way)
* [Documentation kubernetes.io (free).](https://kubernetes.io)

## CKA Exam

You can take the CKA exam from any qualifying computer, anywhere there connected to internet, almost any time. The passing score of the exam is 74%.

There are six clusters that comprise the exam environment. To switch between clusters, we can use :

```bash
kubectl config use-context <cluster>
```

![cka-clusters](/assets/images/cka-ckad-feedback/cka-clusters.png)

There are 24 problems/questions with different weight. You have root access to all servers of all clusters so you are in some ways responsible for what you do.

The exam plateform is powered by examslocal.com. Copy paste to external software are not permitted. Only 2 tabs of your browser are permitted, one for the exam platform and one for kubernetes.io documentation.

The exam lasts 3 hours, I found it very challenging and well-made. Although you have root access to all servers, the 70% of the exam was made to use only kubectl command line and the 30% to debug and install kubernetes control plane components. For the debugging part, Kubernetes the Hard Way was a good advantage to accomplish these problems.

Because 3 hours are short, I’ve put a personal time limit of 8 minutes per question, I strongly advice you to put a time limit per question. I spent for some questions 1 minute to solve the problem and some time 8 minutes.

The embedded note is very useful to copy paste from it. Use it as you can.

## CKAD Exam

As the CKA exam, the CKAD is local exam that you can pass it from your computer with internet access. The passing score is 66% and you have only 2 hours to pass it.

There are 4 clusters described as bellow.

![ckad-clusters](/assets/images/cka-ckad-feedback/ckad-clusters.png)

My training path was the same as CKA. Same platfrom, same technical environment. The CKAD exam was more complicated than the CKA because of the lack of time but also it was challenging and well made as the CKA.

I felt that I can pass the CKAD exam without additional training the only thing i’ve done was looking to the curriculum repository in Github and i’ve noticed that i’m already mastering 90% of the exam objectives.
