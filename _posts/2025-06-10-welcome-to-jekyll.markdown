---
layout: posts
title:  "Kubernetes Admission Controllers"
tagline: "Demystifying kubernetes security"
date:   2025-06-21 19:13:27 -0500
tags: [hackathon]
author_profile: true
author: Gunjan
author_profile: true
author: Gunjan
categories: [article]
header:
<<<<<<< HEAD
    overlay_image: https://images.unsplash.com/photo-1574664620916-fb955a65cab3
    teaser: https://images.unsplash.com/photo-1574664620916-fb955a65cab3
    caption: "Photo credit: [**Unsplash: Firosnv. Photography**](https://unsplash.com/@firosnv)"
   
=======
    overlay_image: https://media.licdn.com/dms/image/v2/D5612AQGxibZrUHiLLA/article-cover_image-shrink_720_1280/B56ZcMzhAxGoAI-/0/1748266521622?e=2147483647&amp;v=beta&amp;t=dCrImX_2oh9IVBxqFPJZL1A0M12F6m_aAKNCTMEWStI
    teaser: https://media.licdn.com/dms/image/v2/D5612AQGxibZrUHiLLA/article-cover_image-shrink_720_1280/B56ZcMzhAxGoAI-/0/1748266521622?e=2147483647&amp;v=beta&amp;t=dCrImX_2oh9IVBxqFPJZL1A0M12F6m_aAKNCTMEWStI
    caption: "Kubernetes Security"
>>>>>>> 948fe3a (page)
description: In the world of Kubernetes, Admission Controllers are the silent gatekeepers—ensuring that what enters your cluster complies with the pre-defined set of rules. Lets see what we all need to know to achieve our organization’s standards and best practices before the first pod is even created.
---
<html class="cls-fix-enabled" lang="en">
<head>
</head>
      
 
  

      


    
    
    
    
    
    
 
      

        <div class="details mx-details-container-padding">
          
        
            
    
    
    
    
    
    
    
    
    
    
    
    
    

          
    <figure class="cover-img">
<!---->      <div class="cover-img__image-frame relative w-full overflow-hidden pb-[calc((134/782)*100%)]">
        <div class="cover-img__image-position absolute top-0 right-0 bottom-0 left-0
            ">
            <img class="cover-img__image relative w-full h-full object-cover" src="https://media.licdn.com/dms/image/v2/D5612AQGxibZrUHiLLA/article-cover_image-shrink_720_1280/B56ZcMzhAxGoAI-/0/1748266521622?e=2147483647&amp;v=beta&amp;t=dCrImX_2oh9IVBxqFPJZL1A0M12F6m_aAKNCTMEWStI" fetchpriority="high" data-embed-id="cover-image" alt="Kubernetes Admission Controllers" tabindex="0">
        </div>
      </div>
<!---->    </figure>
  
                  
      <header>
       
      
      </header>
      
              <div data-test-id="article-content-blocks">
<!---->                  

    <div class="article-main__content" data-test-id="publishing-text-block">
        <h3><span class>What are admission controllers?</span><!----></h3>
    </div>
  
<!----><!---->                  

    <div class="article-main__content" data-test-id="publishing-text-block">
        <p>
          <span class>A Kubernetes admission controller can be considered as a piece of code that intercepts API requests, changes the request object or denies the request altogether.</span><!---->
        </p>
    </div>
  
<!----><!---->                  

    <div class="article-main__content" data-test-id="publishing-text-block">
        <p>
          <span class>Admission control mechanisms may be </span><span class="italic">validating</span><span class>, </span><span class="italic">mutating</span><span class>, or both. Mutating controllers may modify the data for the resource being modified; validating controllers may not.</span><!---->
        </p>
    </div>
  
<!----><!---->                  

    <div class="article-main__content" data-test-id="publishing-text-block">
        <h3><span class>Why do we need them?</span><!----></h3>
    </div>
  
<!----><!---->                  

    <div class="article-main__content" data-test-id="publishing-text-block">
        <p>
          <span class>
      <ul>
        
    <li><span class="font-[700]">Security</span><!----></li>
    <li><span class="font-[700]">Policy enforcement</span><!----></li>
    <li><span class="font-[700]">Customisation</span><!----></li>
    <li><span class="font-[700]">Compliance</span><!----></li>

      </ul>
  </span><!---->
        </p>
    </div>
  
<!----><!---->                  

    <div class="article-main__content" data-test-id="publishing-text-block">
          <h2 data-test-id="pulse-publishing-h1">
            <span class>Admission Webhook Controllers Lifecycle </span><!---->
          </h2>
    </div>
  
<!----><!---->                  

    <div class="article-main__content" data-test-id="publishing-text-block">
        <p>
          <span class>When a request reaches the API, it goes through several stages, illustrated below.</span><!---->
        </p>
    </div>
  
<!----><!---->                  

    <div class="article-main__content" data-test-id="publishing-text-block">
        <p>
          <!----><br>
        </p>
    </div>
  
<!----><!---->                  
    

    
      <div class="flex flex-col mt-2" data-test-id="publishing-image-block" rel="ugc">
        
      <figure>
        <img alt="Admission control phases" class="lazy-load block w-full" data-delayed-url="https://media.licdn.com/dms/image/v2/D5612AQFEXlf0Tyx9Bw/article-inline_image-shrink_1500_2232/B56ZcMwlNvGoAU-/0/1748265752396?e=2147483647&amp;v=beta&amp;t=TFDoN23pJh7uDHR3c6NFk4BMp94BDddZYaKFiAQZXrU">
          <figcaption class="mt-[0.8rem] text-center text-sm font-normal text-color-text-low-emphasis" data-test-id="publishing-image-block-caption">
            <span class>Kubernetes Admission control phases</span><!---->
          </figcaption>
      </figure>
    
      </div>
  
  
<!----><!---->                  

    <div class="article-main__content" data-test-id="publishing-text-block">
          <h2 data-test-id="pulse-publishing-h1">
            <!----><br>
          </h2>
    </div>
  
<!----><!---->                  

    <div class="article-main__content" data-test-id="publishing-text-block">
          <h2 data-test-id="pulse-publishing-h1">
            <span class>How do I turn on/off an admission controller?</span><!---->
          </h2>
    </div>
  
<!----><!---->                  

    <div class="article-main__content" data-test-id="publishing-text-block">
        <p>
          <span class>
      <ol>
        
    <li><span class>Assume that you want to enable NamespaceLifecycle admission controller.</span><!----></li>
    <li><span class>Open and edit the file given below.</span><!----></li>

      </ol>
  </span><!---->
        </p>
    </div>
  
<!----><!---->                  

    <div class="article-main__content" data-test-id="publishing-text-block">
        
    <pre class="my-4 mx-0 block overflow-x-auto whitespace-pre rounded-md bg-color-background-container-dark-tint p-4 font-mono text-md font-normal leading-open text-color-text-on-dark"><span class>controlplane:~$ cat /etc/kubernetes/manifests/kube-apiserver.yaml
apiVersion: v1
kind: Pod
metadata:
  annotations:
    kubeadm.kubernetes.io/kube-apiserver.advertise-address.endpoint: 172.30.1.2:6443
  creationTimestamp: null
  labels:
    component: kube-apiserver
    tier: control-plane
  name: kube-apiserver
  namespace: kube-system
spec:
  containers:
  - command:
    - kube-apiserver
    - --advertise-address=172.30.1.2
    - --allow-privileged=true
    - --authorization-mode=Node,RBAC
    - --client-ca-file=/etc/kubernetes/pki/ca.crt
    - --enable-admission-plugins=NodeRestriction,LimitRanger,Priority
    - --enable-bootstrap-token-auth=true
    - --etcd-cafile=/etc/kubernetes/pki/etcd/ca.crt
    - --etcd-certfile=/etc/kubernetes/pki/apiserver-etcd-client.crt
    - --etcd-keyfile=/etc/kubernetes/pki/apiserver-etcd-client.key
    - --etcd-servers=https://127.0.0.1:2379        </span></pre>
  
          </div>
  
<!----><!---->                  

    <div class="article-main__content" data-test-id="publishing-text-block">
        <p>
          <span class>3. Add this controller where plugins are list using --enable-admission-plugins. Similarly, to disable the same, pass the names in parameter --disable-admission-plugins.</span><!---->
        </p>
    </div>
  
<!----><!---->                  

    <div class="article-main__content" data-test-id="publishing-text-block">
        
    <pre class="my-4 mx-0 block overflow-x-auto whitespace-pre rounded-md bg-color-background-container-dark-tint p-4 font-mono text-md font-normal leading-open text-color-text-on-dark"><span class>apiVersion: v1
kind: Pod
metadata:
  annotations:
    kubeadm.kubernetes.io/kube-apiserver.advertise-address.endpoint: 172.30.1.2:6443
  creationTimestamp: null
  labels:
    component: kube-apiserver
    tier: control-plane
  name: kube-apiserver
  namespace: kube-system
spec:
  containers:
  - command:
    - kube-apiserver
    - --advertise-address=172.30.1.2
    - --allow-privileged=true
    - --authorization-mode=Node,RBAC
    - --client-ca-file=/etc/kubernetes/pki/ca.crt
    - --enable-admission-plugins=NodeRestriction,LimitRanger,Priority,NamespaceLifecycle
    - --enable-bootstrap-token-auth=true
    - --etcd-cafile=/etc/kubernetes/pki/etcd/ca.crt
    - --etcd-certfile=/etc/kubernetes/pki/apiserver-etcd-client.crt
    - --etcd-keyfile=/etc/kubernetes/pki/apiserver-etcd-client.key
    - --etcd-servers=https://127.0.0.1:2379
   -- INSERT --         </span></pre>
  
          </div>
  
<!----><!---->                  

    <div class="article-main__content" data-test-id="publishing-text-block">
        <p>
          <!----><br>
        </p>
    </div>
  
<!----><!---->                  

    <div class="article-main__content" data-test-id="publishing-text-block">
          <h2 data-test-id="pulse-publishing-h1">
            <span class>Examples </span><!---->
          </h2>
    </div>
  
<!----><!---->                  

    <div class="article-main__content" data-test-id="publishing-text-block">
        <p>
          <span class>** To refer the complete list, visit </span><span class><a href="https://www.linkedin.com/redir/redirect?url=https%3A%2F%2Fkubernetes%2Eio%2Fdocs%2Freference%2Faccess-authn-authz%2Fadmission-controllers%2F%23what-does-each-admission-controller-do&amp;urlhash=4qby&amp;trk=article-ssr-frontend-pulse_little-text-block" target="_blank" data-tracking-control-name="article-ssr-frontend-pulse_little-text-block" data-tracking-will-navigate data-test-link>Compiled-in admission controllers<!----></a></span><!---->
        </p>
    </div>
  
<!----><!---->                  
    <hr data-test-id="publishing-divider-block" class="my-[3.2rem] mx-auto h-[1px] border-0 bg-black-a16">
  
<!----><!---->                  

    <div class="article-main__content" data-test-id="publishing-text-block">
        <h3><span class>AlwaysPullImages</span><!----></h3>
    </div>
  
<!----><!---->                  

    <div class="article-main__content" data-test-id="publishing-text-block">
        <p>
          <span class>This admission controller modifies every new Pod to force the image pull policy to Always. This is useful in a multitenant cluster so that users can be assured that their private images can only be used by those who have the credentials to pull them.</span><!---->
        </p>
    </div>
  
<!----><!---->                  

    <div class="article-main__content" data-test-id="publishing-text-block">
        <h3><span class>CertificateApproval</span><!----></h3>
    </div>
  
<!----><!---->                  

    <div class="article-main__content" data-test-id="publishing-text-block">
        <p>
          <span class>This admission controller observes requests to approve CertificateSigningRequest resources and performs additional authorization checks to ensure the approving user has permission to </span><span class="font-[700]">approve</span><span class> certificate requests with the spec.signerName requested on the CertificateSigningRequest resource.</span><!---->
        </p>
    </div>
  
<!----><!---->                  

    <div class="article-main__content" data-test-id="publishing-text-block">
        <h3><span class>DefaultIngressClass</span><!----></h3>
    </div>
  
<!----><!---->                  

    <div class="article-main__content" data-test-id="publishing-text-block">
        <p>
          <span class>This admission controller observes creation of Ingress objects that do not request any specific ingress class and automatically adds a default ingress class to them.</span><!---->
        </p>
    </div>
  
<!----><!---->                  

    <div class="article-main__content" data-test-id="publishing-text-block">
        <h3><span class>DefaultStorageClass</span><!----></h3>
    </div>
  
<!----><!---->                  

    <div class="article-main__content" data-test-id="publishing-text-block">
        <p>
          <span class>This admission controller observes creation of PersistentVolumeClaim objects that do not request any specific storage class and automatically adds a default storage class to them.</span><!---->
        </p>
    </div>
  
<!----><!---->                  

    <div class="article-main__content" data-test-id="publishing-text-block">
        <h3><span class>EventRateLimit</span><!----></h3>
    </div>
  
<!----><!---->                  

    <div class="article-main__content" data-test-id="publishing-text-block">
        <p>
          <span class>This admission controller mitigates the problem where the API server gets flooded by requests to store new Events. The cluster admin can specify event rate limits by following specs under </span><span class><a href="https://www.linkedin.com/redir/redirect?url=https%3A%2F%2Fkubernetes%2Eio%2Fdocs%2Freference%2Fconfig-api%2Fapiserver-eventratelimit%2Ev1alpha1%2F&amp;urlhash=7mAH&amp;trk=article-ssr-frontend-pulse_little-text-block" target="_blank" data-tracking-control-name="article-ssr-frontend-pulse_little-text-block" data-tracking-will-navigate data-test-link>https://kubernetes.io/docs/reference/config-api/apiserver-eventratelimit.v1alpha1/<!----></a></span><!---->
        </p>
    </div>
  
<!----><!---->                  

    <div class="article-main__content" data-test-id="publishing-text-block">
        
    <pre class="my-4 mx-0 block overflow-x-auto whitespace-pre rounded-md bg-color-background-container-dark-tint p-4 font-mono text-md font-normal leading-open text-color-text-on-dark"><span class>apiVersion: eventratelimit.admission.k8s.io/v1alpha1
kind: Configuration
limits:
  - type: Namespace
    qps: 50
    burst: 100
    cacheSize: 2000
  - type: User
    qps: 10
    burst: 50        </span></pre>
  
          </div>
  
<!----><!---->                  

    <div class="article-main__content" data-test-id="publishing-text-block">
        <h3><span class>NamespaceAutoProvision</span><!----></h3>
    </div>
  
<!----><!---->                  

    <div class="article-main__content" data-test-id="publishing-text-block">
        <p>
          <span class>This admission controller examines all incoming requests on namespaced resources and checks if the referenced namespace does exist. It creates a namespace if it cannot be found.</span><!---->
        </p>
    </div>
  
<!----><!---->                  

    <div class="article-main__content" data-test-id="publishing-text-block">
          <h2 data-test-id="pulse-publishing-h1">
            <span class>Dynamic Admission Control</span><!---->
          </h2>
    </div>
  
<!----><!---->                  

    <div class="article-main__content" data-test-id="publishing-text-block">
        <p>
          <span class>In addition to the inbuilt admission plugins can be developed as extensions a nd run as webhooks configured at runtime. As we saw some pre-configured admission controllers, we can either create them from scratch as well as explore amazing gatekeeper functionality provided by OPA (Open Policy Agent).OPA can enforce policies such as:</span><!---->
        </p>
    </div>
  
<!----><!---->                  

    <div class="article-main__content" data-test-id="publishing-text-block">
        <p>
          <span class>
      <ul>
        
    <li><span class>Requiring specific labels on all resources.</span><!----></li>
    <li><span class>Ensuring that container images come from a trusted registry.</span><!----></li>
    <li><span class>Preventing the creation of conflicting Ingress objects.</span><!----></li>

      </ul>
  </span><!---->
        </p>
    </div>
  
<!----><!---->                  

    <div class="article-main__content" data-test-id="publishing-text-block">
        <h3><span class>Working Example</span><!----></h3>
    </div>
  
<!----><!---->                  

    <div class="article-main__content" data-test-id="publishing-text-block">
        <p>
          <span class>Suppose you want to ensure all the deployments in your cluster have a certain label for the team deploying that object. Follow below steps to make that work using OPA.</span><!---->
        </p>
    </div>
  
<!----><!---->                  

    <div class="article-main__content" data-test-id="publishing-text-block">
        
    <pre class="my-4 mx-0 block overflow-x-auto whitespace-pre rounded-md bg-color-background-container-dark-tint p-4 font-mono text-md font-normal leading-open text-color-text-on-dark"><span class>controlplane:~$ k apply -f - &lt;&lt; EOF
&gt;    apiVersion: templates.gatekeeper.sh/v1beta1
   kind: ConstraintTemplate
   metadata:
     name: teamid
   spec:
     crd:
       spec:
         names:
           kind: TeamId
     targets:
       - target: admission.k8s.gatekeeper.sh
         rego: |
           package team_id_label
           default allow := false

           allow {
               input.review.object.metadata.labels.team_id
           }

           violation[{"msg": msg}] {
               not allow
               msg := "The team_id label is required"
           }
EOF
constrainttemplate.templates.gatekeeper.sh/teamid created        </span></pre>
  
          </div>
  
<!----><!---->                  

    <div class="article-main__content" data-test-id="publishing-text-block">
        <p>
          <span class>Create the corresponding constraint object in order to apply the policy.</span><!---->
        </p>
    </div>
  
<!----><!---->                  

    <div class="article-main__content" data-test-id="publishing-text-block">
        
    <pre class="my-4 mx-0 block overflow-x-auto whitespace-pre rounded-md bg-color-background-container-dark-tint p-4 font-mono text-md font-normal leading-open text-color-text-on-dark"><span class>controlplane:~$ k apply -f - &lt;&lt; EOF
&gt;    apiVersion: constraints.gatekeeper.sh/v1beta1
   kind: TeamId
   metadata:
     name: require-team-id
   spec:
     match:
       kinds:
         - apiGroups: ["*"]
           kinds: ["*"]
EOF
teamid.constraints.gatekeeper.sh/require-team-id created        </span></pre>
  
          </div>
  
<!----><!---->                  

    <div class="article-main__content" data-test-id="publishing-text-block">
        <p>
          <span class>Test the deployment for above policies.</span><!---->
        </p>
    </div>
  
<!----><!---->                  

    <div class="article-main__content" data-test-id="publishing-text-block">
        
    <pre class="my-4 mx-0 block overflow-x-auto whitespace-pre rounded-md bg-color-background-container-dark-tint p-4 font-mono text-md font-normal leading-open text-color-text-on-dark"><span class>controlplane:~$ k apply -f - &lt;&lt;EOF
&gt;    apiVersion: apps/v1
   kind: Deployment
   metadata:
     name: test-deployment
   spec:
     replicas: 1
     selector:
       matchLabels:
         app: test
     template:
       metadata:
         labels:
           app: test
       spec:
         containers:
         - name: nginx
           image: nginx
EOF
Error from server (Forbidden): error when creating "STDIN": admission webhook "validation.gatekeeper.sh" denied the request: [require-team-id] The team_id label is required        </span></pre>
  
          </div>
  
<!---->              </div>
<!----><!----><!----><!----><!---->          
  

  
<!---->            

