---
layout: posts
title:  "Part 3: How to win at a hackathon"
tagline: "Casting the 'Dots'wide and far"
date:   2023-06-21 19:13:27 -0500
tags: [hackathon]
author_profile: true
author: Leigh Stewardson
author_profile: true
author: Leigh Stewardson
categories: [article]
header:
    overlay_image: https://images.unsplash.com/photo-1574664620916-fb955a65cab3
    teaser: https://images.unsplash.com/photo-1574664620916-fb955a65cab3
    caption: "Photo credit: [**Unsplash: Firosnv. Photography**](https://unsplash.com/@firosnv)"
description: This series of articles explores how to win at a hackathon even if you don't win the hackathon itself. The third post explores how to build on your momentum and push your hackathon ideas out into the world.
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
  
<!---->    </article>
  
<!---->            
    
    

      <code id="ugcPostUrl" style="display: none"><!--"https://www.linkedin.com/feed/update/urn:li:ugcPost:7332776075300691968"--></code>
      <code id="ugcPost" style="display: none"><!--"urn:li:ugcPost:7332776075300691968"--></code>
      
    
      <code id="disableLinkedinShareRedirectLink" style="display: none"><!--true--></code>
      <code id="ugcPostUrn" style="display: none"><!--"urn:li:ugcPost:7332776075300691968"--></code>
      <code id="signInUrl" style="display: none"><!--"https://www.linkedin.com/signup/cold-join?session_redirect=%2Fpulse%2Fkubernetes-admission-controllers-gunjan-k-b68gc%2F%3FtrackingId%3DZakURyclRUCJxJ3f9IbXzA%253D%253D"--></code>

<!---->  
    <div class="article-social-activity z-[201]
        x-social-activity-wrapper xs:sticky bottom-0 flex justify-center border-t-1 border-solid border-color-border-faint bg-color-background-container
        " data-impression-id="article-ssr-frontend-pulse_x-social-details">
<!---->      <div class="x-social-activity social-details x-social-activity-left flex flex-wrap w-full max-w-x-article-width-small justify-between lg:max-w-x-article-width">
        <div class="flex x-social-activity-left flex-wrap">
          
    
    
    
    
    
    
    
    
    
    

    
    
    

    <code id="i18n_reaction_selection_state" style="display: none"><!--"%reactionType% %selectionState%"--></code>

    <div class="reactions-menu flex flex-row relative items-center justify-center select-none [-webkit-user-select:none] pointer-events-auto" data-feed-control="article-ssr-frontend-x-article_x-social-details_like-toggle_reactions-cta">
        <a class="reactions-menu__link text-color-text social-action-bar__button relative h-6 cursor-pointer w-full" href="https://www.linkedin.com/signup/cold-join?session_redirect=%2Fpulse%2Fkubernetes-admission-controllers-gunjan-k-b68gc%2F%3FtrackingId%3DZakURyclRUCJxJ3f9IbXzA%253D%253D&amp;trk=article-ssr-frontend-pulse_x-social-details_like-toggle_like-cta" target="_blank" data-tracking-control-name="article-ssr-frontend-pulse_x-social-details_like-toggle_reactions-cta" data-parent-urn="urn:li:ugcPost:7332776075300691968" data-tracking-will-navigate data-feed-control="article-ssr-frontend-x-article_x-social-details_like-toggle_reactions-cta">
          

<!---->    <div class="like-button-default flex flex-row items-center ">
      <icon class="social-action-bar__icon" data-svg-class-name="social-action-bar__icon--svg" data-delayed-url="https://static.licdn.com/aero-v1/sc/h/3djuegvxjnk75fm1bl5ugf342">
      </icon>
      <span class="social-action-bar__button-text">Like</span>
    </div>

        </a>
    </div>
      <template id="selected-reaction">
        <div>
            
  <div class="selected-reaction--LIKE flex flex-row items-center">
    <img class="inline-block align-middle relative w-3 h-3 mr-1 babybear:mr-0 mb-0.5" alt="Like" aria-hidden="true" data-delayed-url="https://static.licdn.com/aero-v1/sc/h/3tsxb73co15a9ze36f0y0vmng">
    <span class="social-action-bar__button-text">Like</span>
  </div>

            
  <div class="selected-reaction--PRAISE flex flex-row items-center">
    <img class="inline-block align-middle relative w-3 h-3 mr-1 babybear:mr-0 mb-0.5" alt="Celebrate" aria-hidden="true" data-delayed-url="https://static.licdn.com/aero-v1/sc/h/5tec0l9hykk5gezv56e7coyow">
    <span class="social-action-bar__button-text">Celebrate</span>
  </div>

            
  <div class="selected-reaction--APPRECIATION flex flex-row items-center">
    <img class="inline-block align-middle relative w-3 h-3 mr-1 babybear:mr-0 mb-0.5" alt="Support" aria-hidden="true" data-delayed-url="https://static.licdn.com/aero-v1/sc/h/7savup3gmhirulv2h5v8snx2x">
    <span class="social-action-bar__button-text">Support</span>
  </div>

            
  <div class="selected-reaction--EMPATHY flex flex-row items-center">
    <img class="inline-block align-middle relative w-3 h-3 mr-1 babybear:mr-0 mb-0.5" alt="Love" aria-hidden="true" data-delayed-url="https://static.licdn.com/aero-v1/sc/h/f4lj1wks3jt476fe5defirzg9">
    <span class="social-action-bar__button-text">Love</span>
  </div>

            
  <div class="selected-reaction--INTEREST flex flex-row items-center">
    <img class="inline-block align-middle relative w-3 h-3 mr-1 babybear:mr-0 mb-0.5" alt="Insightful" aria-hidden="true" data-delayed-url="https://static.licdn.com/aero-v1/sc/h/br7ludovnq3n7137fvqsqwljx">
    <span class="social-action-bar__button-text">Insightful</span>
  </div>

            
  <div class="selected-reaction--ENTERTAINMENT flex flex-row items-center">
    <img class="inline-block align-middle relative w-3 h-3 mr-1 babybear:mr-0 mb-0.5" alt="Funny" aria-hidden="true" data-delayed-url="https://static.licdn.com/aero-v1/sc/h/6ga7ypv66xprsgreohwklur3y">
    <span class="social-action-bar__button-text">Funny</span>
  </div>

        </div>
      </template>
  
  
            <div class="relative flex select-none flex-row items-center justify-center">
              <a class="social-action-bar__button !rounded-none " href="https://www.linkedin.com/signup/cold-join?session_redirect=%2Fpulse%2Fkubernetes-admission-controllers-gunjan-k-b68gc%2F%3FtrackingId%3DZakURyclRUCJxJ3f9IbXzA%253D%253D&amp;trk=article-ssr-frontend-pulse_comment-cta" data-tracking-control-name="article-ssr-frontend-pulse_x-social-details_comment-cta" data-tracking-will-navigate>
                <icon class="social-action-bar__icon" data-svg-class-name="social-action-bar__icon--svg" data-delayed-url="https://static.licdn.com/aero-v1/sc/h/1p9aa0o2ms48w7ipecq9amsti">
                </icon>
                <span class="social-action-bar__button-text">
                  Comment
                </span>
              </a>
            </div>
          
      

    
    
    
    

    <code id="i18n_copy_cta_message_success" style="display: none"><!--"Link copied to clipboard."--></code>
    <code id="i18n_copy_cta_message_error" style="display: none"><!--"Something went wrong while copying to clipboard."--></code>

    

    

    <div class="collapsible-dropdown flex items-center relative hyphens-auto social-share inline-block relative select-none x-social-share " data-share-message="Share" data-share-url="https://www.linkedin.com/pulse/kubernetes-admission-controllers-gunjan-k-b68gc?utm_source=share&amp;utm_medium=guest_desktop" data-feed-control="article-ssr-frontend-x-article_x-social-details_social-share-intent_social-share_main_button" data-feed-action-category="EXPAND" data-feed-action-type="openShareMenu">
<!---->
        <ul class="collapsible-dropdown__list hidden container-raised absolute w-auto overflow-y-auto flex-col items-stretch z-1 bottom-[100%] top-auto" role="menu" tabindex="-1">
          
        
  <li role="presentation">
    <button data-tracking-control-name="article-ssr-frontend-pulse_x-social-details_social-share-intent_social-share_copy" class="social-share__item social-share-item" data-share-service="copy" role="menuitem">
      <icon class="social-share__item-icon" data-delayed-url="https://static.licdn.com/aero-v1/sc/h/aup4g97pdky3ff73gv9lyhjvx"></icon>
      <span class="social-share__item-text pl-1">Copy</span>
    </button>
  </li>


        
  <li role="presentation">
    <button data-tracking-control-name="article-ssr-frontend-pulse_x-social-details_social-share-intent_social-share_linkedin" class="social-share__item social-share-item" data-share-service="linkedin" role="menuitem">
      <icon class="social-share__item-icon" data-delayed-url="https://static.licdn.com/aero-v1/sc/h/2uoxvguhsfspfnmr6tvfuyw4y" data-svg-class-name="text-color-text"></icon>
      <span class="social-share__item-text pl-1">LinkedIn</span>
    </button>
  </li>

          
  <li role="presentation">
    <button data-tracking-control-name="article-ssr-frontend-pulse_x-social-details_social-share-intent_social-share_facebook" class="social-share__item social-share-item" data-share-service="facebook" role="menuitem">
      <icon class="social-share__item-icon" data-delayed-url="https://static.licdn.com/aero-v1/sc/h/5xkjpykqkamtr6skk0vodqwd2"></icon>
      <span class="social-share__item-text pl-1">Facebook</span>
    </button>
  </li>

          
  <li role="presentation">
    <button data-tracking-control-name="article-ssr-frontend-pulse_x-social-details_social-share-intent_social-share_twitter" class="social-share__item social-share-item" data-share-service="twitter" role="menuitem">
      <icon class="social-share__item-icon" data-delayed-url="https://static.licdn.com/aero-v1/sc/h/4bmfmbwr1b97362o29qmjo1zj"></icon>
      <span class="social-share__item-text pl-1">Twitter</span>
    </button>
  </li>

<!---->      
        </ul>

          
        <button aria-expanded="false" class="social-share__button social-share__button-square
            social-share-button social-action-bar__button
            
            
            social-share-button--square
            " aria-label data-tracking-control-name="article-ssr-frontend-pulse_x-social-details_social-share-intent_social-share_main_button">
          <icon class="social-share__button-icon " data-delayed-url="https://static.licdn.com/aero-v1/sc/h/852gyy4s01pfis5qf9k99s6d2" data-svg-class-name="social-share-button-icon social-action-bar__icon--svg "></icon>
            <span class="social-share__button-text-square
                social-action-bar__button-text
                ">
              Share
            </span>
        </button>
      
    </div>
  
  
  
        </div>
          
    
    
    
    
    
    
    
    
    
    
    
    
    

    <code id="i18n_reaction_singular" style="display: none"><!--"%numReactions% Reaction"--></code>
    <code id="i18n_reactions_plural" style="display: none"><!--"%numReactions% Reactions"--></code>

      <div class="flex items-center font-sans text-sm babybear:text-xs" data-sap-comment-urn="urn:li:ugcPost:7332776075300691968">
            
      <a href="https://www.linkedin.com/signup/cold-join?session_redirect=%2Fpulse%2Fkubernetes-admission-controllers-gunjan-k-b68gc%2F%3FtrackingId%3DZakURyclRUCJxJ3f9IbXzA%253D%253D&amp;trk=article-ssr-frontend-pulse_x-social-details_likes-count_social-actions-reactions" target="_blank" data-tracking-control-name="article-ssr-frontend-pulse_x-social-details_likes-count_social-actions-reactions" data-tracking-will-navigate class="flex items-center font-normal text-color-text-low-emphasis no-underline visited:text-color-text-low-emphasis  my-1" aria-label="4 Reactions" data-test-id="social-actions__reactions" data-id="social-actions__reactions" data-num-reactions="4" data-singular="%numReactions%" data-plural="%numReactions%" data-entity-urn="urn:li:ugcPost:7332776075300691968" tabindex="0">
        
                    <img alt data-reaction-type="LIKE" data-delayed-url="https://static.licdn.com/aero-v1/sc/h/bn39hirwzjqj18ej1fkz55671" height="16px" width="16px">

              <span aria-hidden="true" class="font-normal ml-0.5" data-test-id="social-actions__reaction-count">
                    4
              </span>
            
      </a>
  
                  <code id="social-actions__reaction-image-APPRECIATION" style="display: none"><!--"https://static.licdn.com/aero-v1/sc/h/cyfai5zw4nrqhyyhl0p7so58v"--></code>
<!----><!---->                  <code id="social-actions__reaction-image-EMPATHY" style="display: none"><!--"https://static.licdn.com/aero-v1/sc/h/asiqslyf4ooq7ggllg4fyo4o2"--></code>
                  <code id="social-actions__reaction-image-ENTERTAINMENT" style="display: none"><!--"https://static.licdn.com/aero-v1/sc/h/22ifp2etz8kb9tgjqn65s9ics"--></code>
<!---->                  <code id="social-actions__reaction-image-INTEREST" style="display: none"><!--"https://static.licdn.com/aero-v1/sc/h/a0e8rff6djeoq8iympcysuqfu"--></code>
                  <code id="social-actions__reaction-image-LIKE" style="display: none"><!--"https://static.licdn.com/aero-v1/sc/h/bn39hirwzjqj18ej1fkz55671"--></code>
                  <code id="social-actions__reaction-image-MAYBE" style="display: none"><!--"https://static.licdn.com/aero-v1/sc/h/cryzkreqrh52ja5bc6njlrupa"--></code>
                  <code id="social-actions__reaction-image-PRAISE" style="display: none"><!--"https://static.licdn.com/aero-v1/sc/h/2tzoeodxy0zug4455msr0oq0v"--></code>
<!----><!----><!----><!---->      </div>
  
      </div>
    </div>
      <div class="comments__container">
        
    
    
    

    <div class="comments">
<!---->
      
<!---->        
<!---->    </div>
  
      </div>
      

    
    
    
    
    
    

    <p class="feed-cta-banner__text border-t-1 border-color-surface-border border-solid p-3 text-center text-md text-color-text-low-emphasis">
        To view or add a comment, <a href="https://www.linkedin.com/signup/cold-join?session_redirect=%2Fpulse%2Fkubernetes-admission-controllers-gunjan-k-b68gc%2F%3FtrackingId%3DZakURyclRUCJxJ3f9IbXzA%253D%253D&trk=article-ssr-frontend-pulse_x-social-details_feed-cta-banner-cta" target="" aria-label="To view or add a comment, sign in" data-tracking-control-name="article-ssr-frontend-pulse_x-social-details_feed-cta-banner-cta" data-tracking-will-navigate="true" class="feed-cta-banner__link link">sign in</a>
    </p>
  
  
               
    

    
    <section class="core-section-container
        my-3 stacked-articles">
<!---->
          
            <h2 class="core-section-container__title section-title">
              More articles by Gunjan K.
            </h2>
         
        
<!---->
      <div class="core-section-container__content break-words">
        
          
    
    
    
    

    
    
    

      <ul class="show-more-less__list show-more-less__list--no-hidden-elems" data-impression-id="article-ssr-frontend-pulse_show-more-less">
        
          <li>
            
    
    
    
    

    
    
    
      <div class="base-card relative w-full hover:no-underline focus:no-underline
        base-card--link
         base-main-card flex flex-wrap py-2 pr-2 babybear:pr-0
        
        base-main-card--link
        babybear:py-1 main-article-card">
        

        <a class="base-card__full-link absolute top-0 right-0 bottom-0 left-0 p-0 z-[2] outline-offset-[4px]" href="https://www.linkedin.com/pulse/dynamodb-serverless-database-discovery-gunjan-khatter-fjycc" data-tracking-control-name="article-ssr-frontend-pulse" data-tracking-will-navigate>
          
          <span class="sr-only">
              
          
        DynamoDB: serverless database discovery
      
      
          </span>
        </a>

      
          <div class="base-main-card__media relative w-[228px] block overflow-hidden flex-shrink-0 rounded-md
              
              h-[129px] babybear:w-[105px] babybear:h-[59px]">
            
        <img class="h-full" data-delayed-url="https://media.licdn.com/dms/image/v2/D5612AQHCVAv1roGUeg/article-cover_image-shrink_600_2000/article-cover_image-shrink_600_2000/0/1733761216182?e=2147483647&amp;v=beta&amp;t=7RFi9wKTFMcvaAkSc2MPD2oplDB7ktk7XeT3v2fK77c" alt>
      
<!---->          </div>

        <div class="base-main-card__info self-center ml-1 flex-1 relative break-words papabear:min-w-0 mamabear:min-w-0 babybear:w-full
            article-card-social-actions">
              <div class="body-text text-color-text-low-emphasis base-main-card__metadata mb-0 babybear:mb-0 babybear:-mt-0.5">
                
          <span class="body-text text-color-text-low-emphasis base-main-card__metadata-item babybear:text-xs">Dec 10, 2024</span>
<!---->      
              </div>
          <h3 class="base-main-card__title font-sans text-[18px] font-bold text-color-text overflow-hidden
              
              babybear:text-sm
              base-main-card__title--link">
            
        DynamoDB: serverless database discovery
      
          </h3>
          

<!---->
                <p class="base-main-card__description body-text text-color-text -mt-0.5">
                  
          Introduction DynamoDB is a fully-managed, NoSQL database service hosted by AWS that offers incredible scalability; that…
      
                </p>

<!---->            
          
        
    
    
    
    
    
    
    
    
    
    
    
    
    

    <code id="i18n_reaction_singular" style="display: none"><!--"%numReactions% Reaction"--></code>
    <code id="i18n_reactions_plural" style="display: none"><!--"%numReactions% Reactions"--></code>

      <div class="flex items-center font-sans text-sm babybear:text-xs -mt-1">
            
      <div class="flex items-center font-normal text-color-text-low-emphasis no-underline visited:text-color-text-low-emphasis  my-1" aria-label="2 Reactions" data-separate-ctas="false" data-test-id="social-actions__reactions" data-id="social-actions__reactions" data-num-reactions="2" data-singular="%numReactions%" data-plural="%numReactions%" tabindex="0">
        
                    <img alt data-reaction-type="LIKE" data-delayed-url="https://static.licdn.com/aero-v1/sc/h/bn39hirwzjqj18ej1fkz55671" height="16px" width="16px">

              <span aria-hidden="true" class="font-normal ml-0.5" data-test-id="social-actions__reaction-count">
                    2
              </span>
            
      </div>
  
                  <code id="social-actions__reaction-image-APPRECIATION" style="display: none"><!--"https://static.licdn.com/aero-v1/sc/h/cyfai5zw4nrqhyyhl0p7so58v"--></code>
<!----><!---->                  <code id="social-actions__reaction-image-EMPATHY" style="display: none"><!--"https://static.licdn.com/aero-v1/sc/h/asiqslyf4ooq7ggllg4fyo4o2"--></code>
                  <code id="social-actions__reaction-image-ENTERTAINMENT" style="display: none"><!--"https://static.licdn.com/aero-v1/sc/h/22ifp2etz8kb9tgjqn65s9ics"--></code>
<!---->                  <code id="social-actions__reaction-image-INTEREST" style="display: none"><!--"https://static.licdn.com/aero-v1/sc/h/a0e8rff6djeoq8iympcysuqfu"--></code>
                  <code id="social-actions__reaction-image-LIKE" style="display: none"><!--"https://static.licdn.com/aero-v1/sc/h/bn39hirwzjqj18ej1fkz55671"--></code>
                  <code id="social-actions__reaction-image-MAYBE" style="display: none"><!--"https://static.licdn.com/aero-v1/sc/h/cryzkreqrh52ja5bc6njlrupa"--></code>
                  <code id="social-actions__reaction-image-PRAISE" style="display: none"><!--"https://static.licdn.com/aero-v1/sc/h/2tzoeodxy0zug4455msr0oq0v"--></code>
<!----><!----><!----><!---->      </div>
  
      
      
        </div>

<!---->      
    
      </div>
  
  
  
  
  
          </li>
          <li>
            
    
    
    
    

    
    
    
      <div class="base-card relative w-full hover:no-underline focus:no-underline
        base-card--link
         base-main-card flex flex-wrap py-2 pr-2 babybear:pr-0
        
        base-main-card--link
        babybear:py-1 main-article-card">
        

        <a class="base-card__full-link absolute top-0 right-0 bottom-0 left-0 p-0 z-[2] outline-offset-[4px]" href="https://www.linkedin.com/pulse/how-implement-ci-cd-your-azure-project-gunjan-khatter-nih6c" data-tracking-control-name="article-ssr-frontend-pulse" data-tracking-will-navigate>
          
          <span class="sr-only">
              
          
        How to Implement CI CD in your Azure Project
      
      
          </span>
        </a>

      
          <div class="base-main-card__media relative w-[228px] block overflow-hidden flex-shrink-0 rounded-md
              
              h-[129px] babybear:w-[105px] babybear:h-[59px]">
            
        <img class="h-full" data-delayed-url="https://media.licdn.com/dms/image/v2/D5612AQEulrRQOtWKuw/article-cover_image-shrink_600_2000/article-cover_image-shrink_600_2000/0/1732520962755?e=2147483647&amp;v=beta&amp;t=krmBPggd4xA6ahl9gGlH8pc_2Hzk1XloJrewVJeGg4w" alt>
      
<!---->          </div>

        <div class="base-main-card__info self-center ml-1 flex-1 relative break-words papabear:min-w-0 mamabear:min-w-0 babybear:w-full
            article-card-social-actions">
              <div class="body-text text-color-text-low-emphasis base-main-card__metadata mb-0 babybear:mb-0 babybear:-mt-0.5">
                
          <span class="body-text text-color-text-low-emphasis base-main-card__metadata-item babybear:text-xs">Nov 25, 2024</span>
<!---->      
              </div>
          <h3 class="base-main-card__title font-sans text-[18px] font-bold text-color-text overflow-hidden
              
              babybear:text-sm
              base-main-card__title--link">
            
        How to Implement CI CD in your Azure Project
      
          </h3>
          

<!---->
                <p class="base-main-card__description body-text text-color-text -mt-0.5">
                  
          PRE REQUISITES Create Azure Subscription Azure Resource Groups for your environments Create AKS using console, cli or…
      
                </p>

<!---->            
          
        
    
    
    
    
    
    
    
    
    
    
    
    
    

    <code id="i18n_reaction_singular" style="display: none"><!--"%numReactions% Reaction"--></code>
    <code id="i18n_reactions_plural" style="display: none"><!--"%numReactions% Reactions"--></code>

      <div class="flex items-center font-sans text-sm babybear:text-xs -mt-1">
            
      <div class="flex items-center font-normal text-color-text-low-emphasis no-underline visited:text-color-text-low-emphasis  my-1" aria-label="5 Reactions" data-separate-ctas="false" data-test-id="social-actions__reactions" data-id="social-actions__reactions" data-num-reactions="5" data-singular="%numReactions%" data-plural="%numReactions%" tabindex="0">
        
                    <img alt data-reaction-type="LIKE" data-delayed-url="https://static.licdn.com/aero-v1/sc/h/bn39hirwzjqj18ej1fkz55671" height="16px" width="16px">

              <span aria-hidden="true" class="font-normal ml-0.5" data-test-id="social-actions__reaction-count">
                    5
              </span>
            
      </div>
  
                  <code id="social-actions__reaction-image-APPRECIATION" style="display: none"><!--"https://static.licdn.com/aero-v1/sc/h/cyfai5zw4nrqhyyhl0p7so58v"--></code>
<!----><!---->                  <code id="social-actions__reaction-image-EMPATHY" style="display: none"><!--"https://static.licdn.com/aero-v1/sc/h/asiqslyf4ooq7ggllg4fyo4o2"--></code>
                  <code id="social-actions__reaction-image-ENTERTAINMENT" style="display: none"><!--"https://static.licdn.com/aero-v1/sc/h/22ifp2etz8kb9tgjqn65s9ics"--></code>
<!---->                  <code id="social-actions__reaction-image-INTEREST" style="display: none"><!--"https://static.licdn.com/aero-v1/sc/h/a0e8rff6djeoq8iympcysuqfu"--></code>
                  <code id="social-actions__reaction-image-LIKE" style="display: none"><!--"https://static.licdn.com/aero-v1/sc/h/bn39hirwzjqj18ej1fkz55671"--></code>
                  <code id="social-actions__reaction-image-MAYBE" style="display: none"><!--"https://static.licdn.com/aero-v1/sc/h/cryzkreqrh52ja5bc6njlrupa"--></code>
                  <code id="social-actions__reaction-image-PRAISE" style="display: none"><!--"https://static.licdn.com/aero-v1/sc/h/2tzoeodxy0zug4455msr0oq0v"--></code>
<!----><!----><!----><!---->      </div>
  
      
      
        </div>

<!---->      
    
      </div>
  
  
  
  
  
          </li>
      
      </ul>
  
  
        
      </div>
    </section>
  
  
          
      
        </div>
      </section>
      <section class="right-rail papabear:w-right-rail-width papabear:ml-column-gutter mamabear:max-w-[790px] mamabear:px-mobile-container-padding babybear:max-w-[790px] babybear:px-mobile-container-padding">
        
        
<!----><!----><!----><!---->              
    
    
    

    
      <section class="aside-section-container mb-4 content-hub-topics">

            <h2 class="aside-section-container__title section-title">
              Explore topics
            </h2>

<!---->
        <div class="aside-section-container__content break-words">
          
        <ul class="career-advice-hub-topics__list">
            <li class="career-advice-hub-topics__list-item mb-1">
              <a href="https://www.linkedin.com/pulse/topics/sales-s5/" data-tracking-control-name="article-ssr-frontend-pulse_content-hub-topic" data-tracking-will-navigate class="btn-sm btn-secondary flex w-fit mr-1 mb-1 hover:no-underline">
                Sales
              </a>
            </li>
            <li class="career-advice-hub-topics__list-item mb-1">
              <a href="https://www.linkedin.com/pulse/topics/marketing-s2461/" data-tracking-control-name="article-ssr-frontend-pulse_content-hub-topic" data-tracking-will-navigate class="btn-sm btn-secondary flex w-fit mr-1 mb-1 hover:no-underline">
                Marketing
              </a>
            </li>
            <li class="career-advice-hub-topics__list-item mb-1">
              <a href="https://www.linkedin.com/pulse/topics/it-services-s57547/" data-tracking-control-name="article-ssr-frontend-pulse_content-hub-topic" data-tracking-will-navigate class="btn-sm btn-secondary flex w-fit mr-1 mb-1 hover:no-underline">
                IT Services
              </a>
            </li>
            <li class="career-advice-hub-topics__list-item mb-1">
              <a href="https://www.linkedin.com/pulse/topics/business-administration-s50111/" data-tracking-control-name="article-ssr-frontend-pulse_content-hub-topic" data-tracking-will-navigate class="btn-sm btn-secondary flex w-fit mr-1 mb-1 hover:no-underline">
                Business Administration
              </a>
            </li>
            <li class="career-advice-hub-topics__list-item mb-1">
              <a href="https://www.linkedin.com/pulse/topics/hr-management-s50359/" data-tracking-control-name="article-ssr-frontend-pulse_content-hub-topic" data-tracking-will-navigate class="btn-sm btn-secondary flex w-fit mr-1 mb-1 hover:no-underline">
                HR Management
              </a>
            </li>
            <li class="career-advice-hub-topics__list-item mb-1">
              <a href="https://www.linkedin.com/pulse/topics/engineering-s166/" data-tracking-control-name="article-ssr-frontend-pulse_content-hub-topic" data-tracking-will-navigate class="btn-sm btn-secondary flex w-fit mr-1 mb-1 hover:no-underline">
                Engineering
              </a>
            </li>
            <li class="career-advice-hub-topics__list-item mb-1">
              <a href="https://www.linkedin.com/pulse/topics/soft-skills-s2976/" data-tracking-control-name="article-ssr-frontend-pulse_content-hub-topic" data-tracking-will-navigate class="btn-sm btn-secondary flex w-fit mr-1 mb-1 hover:no-underline">
                Soft Skills
              </a>
            </li>
          <li class="career-advice-hub-topics__list-item mb-1">
            <a href="https://www.linkedin.com/pulse/topics/home/" data-tracking-control-name="article-ssr-frontend-pulse_content-hub-topic" data-tracking-will-navigate class="btn-sm btn-secondary-emphasis flex w-fit mr-[6px] mb-1 hover:no-underline" aria-label="See All, Explore topics">
              See All
            </a>
          </li>
        </ul>
      
        </div>
      </section>
  
  
          
      
      </section>
    </main>

      <div class="pre-footer ">
        
        
<!---->          
      
      </div>

    

    
    
    
    
    
    
    
    
    
    
    
    
    
    

    
    
    
    
    
    
    
    
    

    
    
    
    

    <footer class="li-footer bg-transparent w-full ">
      <ul class="li-footer__list flex flex-wrap flex-row items-start justify-start w-full h-auto min-h-[50px] my-[0px] mx-auto py-3 px-2 papabear:w-[1128px] papabear:p-0">
        
  <li class="li-footer__item font-sans text-xs text-color-text-solid-secondary flex flex-shrink-0 justify-start p-1 relative w-50% papabear:justify-center papabear:w-auto">
        
          <span class="sr-only">LinkedIn</span>
          <icon class="li-footer__copy-logo text-color-logo-brand-alt inline-block self-center h-[14px] w-[56px] mr-1" data-delayed-url="https://static.licdn.com/aero-v1/sc/h/5mebydpuuijm3uhv1q375inqh"></icon>
          <span class="li-footer__copy-text flex items-center">&copy; 2025</span>
        
  </li>

        
  <li class="li-footer__item font-sans text-xs text-color-text-solid-secondary flex flex-shrink-0 justify-start p-1 relative w-50% papabear:justify-center papabear:w-auto">
        <a class="li-footer__item-link flex items-center font-sans text-xs font-bold text-color-text-solid-secondary hover:text-color-link-hover focus:text-color-link-focus" href="https://about.linkedin.com?trk=d_flagship2_pulse_read_footer-about" data-tracking-control-name="d_flagship2_pulse_read_footer-about" data-tracking-will-navigate>
          
          About
        
        </a>
  </li>

        
  <li class="li-footer__item font-sans text-xs text-color-text-solid-secondary flex flex-shrink-0 justify-start p-1 relative w-50% papabear:justify-center papabear:w-auto">
        <a class="li-footer__item-link flex items-center font-sans text-xs font-bold text-color-text-solid-secondary hover:text-color-link-hover focus:text-color-link-focus" href="https://www.linkedin.com/accessibility?trk=d_flagship2_pulse_read_footer-accessibility" data-tracking-control-name="d_flagship2_pulse_read_footer-accessibility" data-tracking-will-navigate>
          
          Accessibility
        
        </a>
  </li>

        
  <li class="li-footer__item font-sans text-xs text-color-text-solid-secondary flex flex-shrink-0 justify-start p-1 relative w-50% papabear:justify-center papabear:w-auto">
        <a class="li-footer__item-link flex items-center font-sans text-xs font-bold text-color-text-solid-secondary hover:text-color-link-hover focus:text-color-link-focus" href="https://www.linkedin.com/legal/user-agreement?trk=d_flagship2_pulse_read_footer-user-agreement" data-tracking-control-name="d_flagship2_pulse_read_footer-user-agreement" data-tracking-will-navigate>
          
          User Agreement
        
        </a>
  </li>

        
  <li class="li-footer__item font-sans text-xs text-color-text-solid-secondary flex flex-shrink-0 justify-start p-1 relative w-50% papabear:justify-center papabear:w-auto">
        <a class="li-footer__item-link flex items-center font-sans text-xs font-bold text-color-text-solid-secondary hover:text-color-link-hover focus:text-color-link-focus" href="https://www.linkedin.com/legal/privacy-policy?trk=d_flagship2_pulse_read_footer-privacy-policy" data-tracking-control-name="d_flagship2_pulse_read_footer-privacy-policy" data-tracking-will-navigate>
          
          Privacy Policy
        
        </a>
  </li>

<!---->        
  <li class="li-footer__item font-sans text-xs text-color-text-solid-secondary flex flex-shrink-0 justify-start p-1 relative w-50% papabear:justify-center papabear:w-auto">
        <a class="li-footer__item-link flex items-center font-sans text-xs font-bold text-color-text-solid-secondary hover:text-color-link-hover focus:text-color-link-focus" href="https://www.linkedin.com/legal/cookie-policy?trk=d_flagship2_pulse_read_footer-cookie-policy" data-tracking-control-name="d_flagship2_pulse_read_footer-cookie-policy" data-tracking-will-navigate>
          
          Cookie Policy
        
        </a>
  </li>

        
  <li class="li-footer__item font-sans text-xs text-color-text-solid-secondary flex flex-shrink-0 justify-start p-1 relative w-50% papabear:justify-center papabear:w-auto">
        <a class="li-footer__item-link flex items-center font-sans text-xs font-bold text-color-text-solid-secondary hover:text-color-link-hover focus:text-color-link-focus" href="https://www.linkedin.com/legal/copyright-policy?trk=d_flagship2_pulse_read_footer-copyright-policy" data-tracking-control-name="d_flagship2_pulse_read_footer-copyright-policy" data-tracking-will-navigate>
          
          Copyright Policy
        
        </a>
  </li>

        
  <li class="li-footer__item font-sans text-xs text-color-text-solid-secondary flex flex-shrink-0 justify-start p-1 relative w-50% papabear:justify-center papabear:w-auto">
        <a class="li-footer__item-link flex items-center font-sans text-xs font-bold text-color-text-solid-secondary hover:text-color-link-hover focus:text-color-link-focus" href="https://brand.linkedin.com/policies?trk=d_flagship2_pulse_read_footer-brand-policy" data-tracking-control-name="d_flagship2_pulse_read_footer-brand-policy" data-tracking-will-navigate>
          
          Brand Policy
        
        </a>
  </li>

          
  <li class="li-footer__item font-sans text-xs text-color-text-solid-secondary flex flex-shrink-0 justify-start p-1 relative w-50% papabear:justify-center papabear:w-auto">
        <a class="li-footer__item-link flex items-center font-sans text-xs font-bold text-color-text-solid-secondary hover:text-color-link-hover focus:text-color-link-focus" href="https://www.linkedin.com/psettings/guest-controls?trk=d_flagship2_pulse_read_footer-guest-controls" data-tracking-control-name="d_flagship2_pulse_read_footer-guest-controls" data-tracking-will-navigate>
          
            Guest Controls
          
        </a>
  </li>

        
  <li class="li-footer__item font-sans text-xs text-color-text-solid-secondary flex flex-shrink-0 justify-start p-1 relative w-50% papabear:justify-center papabear:w-auto">
        <a class="li-footer__item-link flex items-center font-sans text-xs font-bold text-color-text-solid-secondary hover:text-color-link-hover focus:text-color-link-focus" href="https://www.linkedin.com/legal/professional-community-policies?trk=d_flagship2_pulse_read_footer-community-guide" data-tracking-control-name="d_flagship2_pulse_read_footer-community-guide" data-tracking-will-navigate>
          
          Community Guidelines
        
        </a>
  </li>

        
<!---->
          
          
  <li class="li-footer__item font-sans text-xs text-color-text-solid-secondary flex flex-shrink-0 justify-start p-1 relative w-50% papabear:justify-center papabear:w-auto">
        
              

    
    

    

    

    <div class="collapsible-dropdown collapsible-dropdown--footer collapsible-dropdown--up flex items-center relative hyphens-auto language-selector z-2">
<!---->
        <ul class="collapsible-dropdown__list hidden container-raised absolute w-auto overflow-y-auto flex-col items-stretch z-1 bottom-[100%] top-auto" role="menu" tabindex="-1">
          
          <li class="language-selector__item" role="presentation">
            <!-- Adding aria-label to both the li and the button because screen reader focus goes to button on desktop and li on mobile-->
            <button aria-label="العربية (Arabic)" class="font-sans text-xs link block py-[5px] px-2 w-full hover:cursor-pointer hover:bg-color-action hover:text-color-text-on-dark focus:bg-color-action focus:text-color-text-on-dark
                language-selector__link !font-regular" data-tracking-control-name="language-selector-ar_AE" data-locale="ar_AE" role="menuitem" lang="ar_AE">
                العربية (Arabic)
            </button>
          </li>
          <li class="language-selector__item" role="presentation">
            <!-- Adding aria-label to both the li and the button because screen reader focus goes to button on desktop and li on mobile-->
            <button aria-label="বাংলা (Bangla)" class="font-sans text-xs link block py-[5px] px-2 w-full hover:cursor-pointer hover:bg-color-action hover:text-color-text-on-dark focus:bg-color-action focus:text-color-text-on-dark
                language-selector__link !font-regular" data-tracking-control-name="language-selector-bn_IN" data-locale="bn_IN" role="menuitem" lang="bn_IN">
                বাংলা (Bangla)
            </button>
          </li>
          <li class="language-selector__item" role="presentation">
            <!-- Adding aria-label to both the li and the button because screen reader focus goes to button on desktop and li on mobile-->
            <button aria-label="Čeština (Czech)" class="font-sans text-xs link block py-[5px] px-2 w-full hover:cursor-pointer hover:bg-color-action hover:text-color-text-on-dark focus:bg-color-action focus:text-color-text-on-dark
                language-selector__link !font-regular" data-tracking-control-name="language-selector-cs_CZ" data-locale="cs_CZ" role="menuitem" lang="cs_CZ">
                Čeština (Czech)
            </button>
          </li>
          <li class="language-selector__item" role="presentation">
            <!-- Adding aria-label to both the li and the button because screen reader focus goes to button on desktop and li on mobile-->
            <button aria-label="Dansk (Danish)" class="font-sans text-xs link block py-[5px] px-2 w-full hover:cursor-pointer hover:bg-color-action hover:text-color-text-on-dark focus:bg-color-action focus:text-color-text-on-dark
                language-selector__link !font-regular" data-tracking-control-name="language-selector-da_DK" data-locale="da_DK" role="menuitem" lang="da_DK">
                Dansk (Danish)
            </button>
          </li>
          <li class="language-selector__item" role="presentation">
            <!-- Adding aria-label to both the li and the button because screen reader focus goes to button on desktop and li on mobile-->
            <button aria-label="Deutsch (German)" class="font-sans text-xs link block py-[5px] px-2 w-full hover:cursor-pointer hover:bg-color-action hover:text-color-text-on-dark focus:bg-color-action focus:text-color-text-on-dark
                language-selector__link !font-regular" data-tracking-control-name="language-selector-de_DE" data-locale="de_DE" role="menuitem" lang="de_DE">
                Deutsch (German)
            </button>
          </li>
          <li class="language-selector__item" role="presentation">
            <!-- Adding aria-label to both the li and the button because screen reader focus goes to button on desktop and li on mobile-->
            <button aria-label="Ελληνικά (Greek)" class="font-sans text-xs link block py-[5px] px-2 w-full hover:cursor-pointer hover:bg-color-action hover:text-color-text-on-dark focus:bg-color-action focus:text-color-text-on-dark
                language-selector__link !font-regular" data-tracking-control-name="language-selector-el_GR" data-locale="el_GR" role="menuitem" lang="el_GR">
                Ελληνικά (Greek)
            </button>
          </li>
          <li class="language-selector__item" role="presentation">
            <!-- Adding aria-label to both the li and the button because screen reader focus goes to button on desktop and li on mobile-->
            <button aria-label="English (English) selected" class="font-sans text-xs link block py-[5px] px-2 w-full hover:cursor-pointer hover:bg-color-action hover:text-color-text-on-dark focus:bg-color-action focus:text-color-text-on-dark
                language-selector__link--selected" data-tracking-control-name="language-selector-en_US" data-locale="en_US" role="menuitem" lang="en_US">
                <strong>English (English)</strong>
            </button>
          </li>
          <li class="language-selector__item" role="presentation">
            <!-- Adding aria-label to both the li and the button because screen reader focus goes to button on desktop and li on mobile-->
            <button aria-label="Español (Spanish)" class="font-sans text-xs link block py-[5px] px-2 w-full hover:cursor-pointer hover:bg-color-action hover:text-color-text-on-dark focus:bg-color-action focus:text-color-text-on-dark
                language-selector__link !font-regular" data-tracking-control-name="language-selector-es_ES" data-locale="es_ES" role="menuitem" lang="es_ES">
                Español (Spanish)
            </button>
          </li>
          <li class="language-selector__item" role="presentation">
            <!-- Adding aria-label to both the li and the button because screen reader focus goes to button on desktop and li on mobile-->
            <button aria-label="فارسی (Persian)" class="font-sans text-xs link block py-[5px] px-2 w-full hover:cursor-pointer hover:bg-color-action hover:text-color-text-on-dark focus:bg-color-action focus:text-color-text-on-dark
                language-selector__link !font-regular" data-tracking-control-name="language-selector-fa_IR" data-locale="fa_IR" role="menuitem" lang="fa_IR">
                فارسی (Persian)
            </button>
          </li>
          <li class="language-selector__item" role="presentation">
            <!-- Adding aria-label to both the li and the button because screen reader focus goes to button on desktop and li on mobile-->
            <button aria-label="Suomi (Finnish)" class="font-sans text-xs link block py-[5px] px-2 w-full hover:cursor-pointer hover:bg-color-action hover:text-color-text-on-dark focus:bg-color-action focus:text-color-text-on-dark
                language-selector__link !font-regular" data-tracking-control-name="language-selector-fi_FI" data-locale="fi_FI" role="menuitem" lang="fi_FI">
                Suomi (Finnish)
            </button>
          </li>
          <li class="language-selector__item" role="presentation">
            <!-- Adding aria-label to both the li and the button because screen reader focus goes to button on desktop and li on mobile-->
            <button aria-label="Français (French)" class="font-sans text-xs link block py-[5px] px-2 w-full hover:cursor-pointer hover:bg-color-action hover:text-color-text-on-dark focus:bg-color-action focus:text-color-text-on-dark
                language-selector__link !font-regular" data-tracking-control-name="language-selector-fr_FR" data-locale="fr_FR" role="menuitem" lang="fr_FR">
                Français (French)
            </button>
          </li>
          <li class="language-selector__item" role="presentation">
            <!-- Adding aria-label to both the li and the button because screen reader focus goes to button on desktop and li on mobile-->
            <button aria-label="हिंदी (Hindi)" class="font-sans text-xs link block py-[5px] px-2 w-full hover:cursor-pointer hover:bg-color-action hover:text-color-text-on-dark focus:bg-color-action focus:text-color-text-on-dark
                language-selector__link !font-regular" data-tracking-control-name="language-selector-hi_IN" data-locale="hi_IN" role="menuitem" lang="hi_IN">
                हिंदी (Hindi)
            </button>
          </li>
          <li class="language-selector__item" role="presentation">
            <!-- Adding aria-label to both the li and the button because screen reader focus goes to button on desktop and li on mobile-->
            <button aria-label="Magyar (Hungarian)" class="font-sans text-xs link block py-[5px] px-2 w-full hover:cursor-pointer hover:bg-color-action hover:text-color-text-on-dark focus:bg-color-action focus:text-color-text-on-dark
                language-selector__link !font-regular" data-tracking-control-name="language-selector-hu_HU" data-locale="hu_HU" role="menuitem" lang="hu_HU">
                Magyar (Hungarian)
            </button>
          </li>
          <li class="language-selector__item" role="presentation">
            <!-- Adding aria-label to both the li and the button because screen reader focus goes to button on desktop and li on mobile-->
            <button aria-label="Bahasa Indonesia (Indonesian)" class="font-sans text-xs link block py-[5px] px-2 w-full hover:cursor-pointer hover:bg-color-action hover:text-color-text-on-dark focus:bg-color-action focus:text-color-text-on-dark
                language-selector__link !font-regular" data-tracking-control-name="language-selector-in_ID" data-locale="in_ID" role="menuitem" lang="in_ID">
                Bahasa Indonesia (Indonesian)
            </button>
          </li>
          <li class="language-selector__item" role="presentation">
            <!-- Adding aria-label to both the li and the button because screen reader focus goes to button on desktop and li on mobile-->
            <button aria-label="Italiano (Italian)" class="font-sans text-xs link block py-[5px] px-2 w-full hover:cursor-pointer hover:bg-color-action hover:text-color-text-on-dark focus:bg-color-action focus:text-color-text-on-dark
                language-selector__link !font-regular" data-tracking-control-name="language-selector-it_IT" data-locale="it_IT" role="menuitem" lang="it_IT">
                Italiano (Italian)
            </button>
          </li>
          <li class="language-selector__item" role="presentation">
            <!-- Adding aria-label to both the li and the button because screen reader focus goes to button on desktop and li on mobile-->
            <button aria-label="עברית (Hebrew)" class="font-sans text-xs link block py-[5px] px-2 w-full hover:cursor-pointer hover:bg-color-action hover:text-color-text-on-dark focus:bg-color-action focus:text-color-text-on-dark
                language-selector__link !font-regular" data-tracking-control-name="language-selector-iw_IL" data-locale="iw_IL" role="menuitem" lang="iw_IL">
                עברית (Hebrew)
            </button>
          </li>
          <li class="language-selector__item" role="presentation">
            <!-- Adding aria-label to both the li and the button because screen reader focus goes to button on desktop and li on mobile-->
            <button aria-label="日本語 (Japanese)" class="font-sans text-xs link block py-[5px] px-2 w-full hover:cursor-pointer hover:bg-color-action hover:text-color-text-on-dark focus:bg-color-action focus:text-color-text-on-dark
                language-selector__link !font-regular" data-tracking-control-name="language-selector-ja_JP" data-locale="ja_JP" role="menuitem" lang="ja_JP">
                日本語 (Japanese)
            </button>
          </li>
          <li class="language-selector__item" role="presentation">
            <!-- Adding aria-label to both the li and the button because screen reader focus goes to button on desktop and li on mobile-->
            <button aria-label="한국어 (Korean)" class="font-sans text-xs link block py-[5px] px-2 w-full hover:cursor-pointer hover:bg-color-action hover:text-color-text-on-dark focus:bg-color-action focus:text-color-text-on-dark
                language-selector__link !font-regular" data-tracking-control-name="language-selector-ko_KR" data-locale="ko_KR" role="menuitem" lang="ko_KR">
                한국어 (Korean)
            </button>
          </li>
          <li class="language-selector__item" role="presentation">
            <!-- Adding aria-label to both the li and the button because screen reader focus goes to button on desktop and li on mobile-->
            <button aria-label="मराठी (Marathi)" class="font-sans text-xs link block py-[5px] px-2 w-full hover:cursor-pointer hover:bg-color-action hover:text-color-text-on-dark focus:bg-color-action focus:text-color-text-on-dark
                language-selector__link !font-regular" data-tracking-control-name="language-selector-mr_IN" data-locale="mr_IN" role="menuitem" lang="mr_IN">
                मराठी (Marathi)
            </button>
          </li>
          <li class="language-selector__item" role="presentation">
            <!-- Adding aria-label to both the li and the button because screen reader focus goes to button on desktop and li on mobile-->
            <button aria-label="Bahasa Malaysia (Malay)" class="font-sans text-xs link block py-[5px] px-2 w-full hover:cursor-pointer hover:bg-color-action hover:text-color-text-on-dark focus:bg-color-action focus:text-color-text-on-dark
                language-selector__link !font-regular" data-tracking-control-name="language-selector-ms_MY" data-locale="ms_MY" role="menuitem" lang="ms_MY">
                Bahasa Malaysia (Malay)
            </button>
          </li>
          <li class="language-selector__item" role="presentation">
            <!-- Adding aria-label to both the li and the button because screen reader focus goes to button on desktop and li on mobile-->
            <button aria-label="Nederlands (Dutch)" class="font-sans text-xs link block py-[5px] px-2 w-full hover:cursor-pointer hover:bg-color-action hover:text-color-text-on-dark focus:bg-color-action focus:text-color-text-on-dark
                language-selector__link !font-regular" data-tracking-control-name="language-selector-nl_NL" data-locale="nl_NL" role="menuitem" lang="nl_NL">
                Nederlands (Dutch)
            </button>
          </li>
          <li class="language-selector__item" role="presentation">
            <!-- Adding aria-label to both the li and the button because screen reader focus goes to button on desktop and li on mobile-->
            <button aria-label="Norsk (Norwegian)" class="font-sans text-xs link block py-[5px] px-2 w-full hover:cursor-pointer hover:bg-color-action hover:text-color-text-on-dark focus:bg-color-action focus:text-color-text-on-dark
                language-selector__link !font-regular" data-tracking-control-name="language-selector-no_NO" data-locale="no_NO" role="menuitem" lang="no_NO">
                Norsk (Norwegian)
            </button>
          </li>
          <li class="language-selector__item" role="presentation">
            <!-- Adding aria-label to both the li and the button because screen reader focus goes to button on desktop and li on mobile-->
            <button aria-label="ਪੰਜਾਬੀ (Punjabi)" class="font-sans text-xs link block py-[5px] px-2 w-full hover:cursor-pointer hover:bg-color-action hover:text-color-text-on-dark focus:bg-color-action focus:text-color-text-on-dark
                language-selector__link !font-regular" data-tracking-control-name="language-selector-pa_IN" data-locale="pa_IN" role="menuitem" lang="pa_IN">
                ਪੰਜਾਬੀ (Punjabi)
            </button>
          </li>
          <li class="language-selector__item" role="presentation">
            <!-- Adding aria-label to both the li and the button because screen reader focus goes to button on desktop and li on mobile-->
            <button aria-label="Polski (Polish)" class="font-sans text-xs link block py-[5px] px-2 w-full hover:cursor-pointer hover:bg-color-action hover:text-color-text-on-dark focus:bg-color-action focus:text-color-text-on-dark
                language-selector__link !font-regular" data-tracking-control-name="language-selector-pl_PL" data-locale="pl_PL" role="menuitem" lang="pl_PL">
                Polski (Polish)
            </button>
          </li>
          <li class="language-selector__item" role="presentation">
            <!-- Adding aria-label to both the li and the button because screen reader focus goes to button on desktop and li on mobile-->
            <button aria-label="Português (Portuguese)" class="font-sans text-xs link block py-[5px] px-2 w-full hover:cursor-pointer hover:bg-color-action hover:text-color-text-on-dark focus:bg-color-action focus:text-color-text-on-dark
                language-selector__link !font-regular" data-tracking-control-name="language-selector-pt_BR" data-locale="pt_BR" role="menuitem" lang="pt_BR">
                Português (Portuguese)
            </button>
          </li>
          <li class="language-selector__item" role="presentation">
            <!-- Adding aria-label to both the li and the button because screen reader focus goes to button on desktop and li on mobile-->
            <button aria-label="Română (Romanian)" class="font-sans text-xs link block py-[5px] px-2 w-full hover:cursor-pointer hover:bg-color-action hover:text-color-text-on-dark focus:bg-color-action focus:text-color-text-on-dark
                language-selector__link !font-regular" data-tracking-control-name="language-selector-ro_RO" data-locale="ro_RO" role="menuitem" lang="ro_RO">
                Română (Romanian)
            </button>
          </li>
          <li class="language-selector__item" role="presentation">
            <!-- Adding aria-label to both the li and the button because screen reader focus goes to button on desktop and li on mobile-->
            <button aria-label="Русский (Russian)" class="font-sans text-xs link block py-[5px] px-2 w-full hover:cursor-pointer hover:bg-color-action hover:text-color-text-on-dark focus:bg-color-action focus:text-color-text-on-dark
                language-selector__link !font-regular" data-tracking-control-name="language-selector-ru_RU" data-locale="ru_RU" role="menuitem" lang="ru_RU">
                Русский (Russian)
            </button>
          </li>
          <li class="language-selector__item" role="presentation">
            <!-- Adding aria-label to both the li and the button because screen reader focus goes to button on desktop and li on mobile-->
            <button aria-label="Svenska (Swedish)" class="font-sans text-xs link block py-[5px] px-2 w-full hover:cursor-pointer hover:bg-color-action hover:text-color-text-on-dark focus:bg-color-action focus:text-color-text-on-dark
                language-selector__link !font-regular" data-tracking-control-name="language-selector-sv_SE" data-locale="sv_SE" role="menuitem" lang="sv_SE">
                Svenska (Swedish)
            </button>
          </li>
          <li class="language-selector__item" role="presentation">
            <!-- Adding aria-label to both the li and the button because screen reader focus goes to button on desktop and li on mobile-->
            <button aria-label="తెలుగు (Telugu)" class="font-sans text-xs link block py-[5px] px-2 w-full hover:cursor-pointer hover:bg-color-action hover:text-color-text-on-dark focus:bg-color-action focus:text-color-text-on-dark
                language-selector__link !font-regular" data-tracking-control-name="language-selector-te_IN" data-locale="te_IN" role="menuitem" lang="te_IN">
                తెలుగు (Telugu)
            </button>
          </li>
          <li class="language-selector__item" role="presentation">
            <!-- Adding aria-label to both the li and the button because screen reader focus goes to button on desktop and li on mobile-->
            <button aria-label="ภาษาไทย (Thai)" class="font-sans text-xs link block py-[5px] px-2 w-full hover:cursor-pointer hover:bg-color-action hover:text-color-text-on-dark focus:bg-color-action focus:text-color-text-on-dark
                language-selector__link !font-regular" data-tracking-control-name="language-selector-th_TH" data-locale="th_TH" role="menuitem" lang="th_TH">
                ภาษาไทย (Thai)
            </button>
          </li>
          <li class="language-selector__item" role="presentation">
            <!-- Adding aria-label to both the li and the button because screen reader focus goes to button on desktop and li on mobile-->
            <button aria-label="Tagalog (Tagalog)" class="font-sans text-xs link block py-[5px] px-2 w-full hover:cursor-pointer hover:bg-color-action hover:text-color-text-on-dark focus:bg-color-action focus:text-color-text-on-dark
                language-selector__link !font-regular" data-tracking-control-name="language-selector-tl_PH" data-locale="tl_PH" role="menuitem" lang="tl_PH">
                Tagalog (Tagalog)
            </button>
          </li>
          <li class="language-selector__item" role="presentation">
            <!-- Adding aria-label to both the li and the button because screen reader focus goes to button on desktop and li on mobile-->
            <button aria-label="Türkçe (Turkish)" class="font-sans text-xs link block py-[5px] px-2 w-full hover:cursor-pointer hover:bg-color-action hover:text-color-text-on-dark focus:bg-color-action focus:text-color-text-on-dark
                language-selector__link !font-regular" data-tracking-control-name="language-selector-tr_TR" data-locale="tr_TR" role="menuitem" lang="tr_TR">
                Türkçe (Turkish)
            </button>
          </li>
          <li class="language-selector__item" role="presentation">
            <!-- Adding aria-label to both the li and the button because screen reader focus goes to button on desktop and li on mobile-->
            <button aria-label="Українська (Ukrainian)" class="font-sans text-xs link block py-[5px] px-2 w-full hover:cursor-pointer hover:bg-color-action hover:text-color-text-on-dark focus:bg-color-action focus:text-color-text-on-dark
                language-selector__link !font-regular" data-tracking-control-name="language-selector-uk_UA" data-locale="uk_UA" role="menuitem" lang="uk_UA">
                Українська (Ukrainian)
            </button>
          </li>
          <li class="language-selector__item" role="presentation">
            <!-- Adding aria-label to both the li and the button because screen reader focus goes to button on desktop and li on mobile-->
            <button aria-label="Tiếng Việt (Vietnamese)" class="font-sans text-xs link block py-[5px] px-2 w-full hover:cursor-pointer hover:bg-color-action hover:text-color-text-on-dark focus:bg-color-action focus:text-color-text-on-dark
                language-selector__link !font-regular" data-tracking-control-name="language-selector-vi_VN" data-locale="vi_VN" role="menuitem" lang="vi_VN">
                Tiếng Việt (Vietnamese)
            </button>
          </li>
          <li class="language-selector__item" role="presentation">
            <!-- Adding aria-label to both the li and the button because screen reader focus goes to button on desktop and li on mobile-->
            <button aria-label="简体中文 (Chinese (Simplified))" class="font-sans text-xs link block py-[5px] px-2 w-full hover:cursor-pointer hover:bg-color-action hover:text-color-text-on-dark focus:bg-color-action focus:text-color-text-on-dark
                language-selector__link !font-regular" data-tracking-control-name="language-selector-zh_CN" data-locale="zh_CN" role="menuitem" lang="zh_CN">
                简体中文 (Chinese (Simplified))
            </button>
          </li>
          <li class="language-selector__item" role="presentation">
            <!-- Adding aria-label to both the li and the button because screen reader focus goes to button on desktop and li on mobile-->
            <button aria-label="正體中文 (Chinese (Traditional))" class="font-sans text-xs link block py-[5px] px-2 w-full hover:cursor-pointer hover:bg-color-action hover:text-color-text-on-dark focus:bg-color-action focus:text-color-text-on-dark
                language-selector__link !font-regular" data-tracking-control-name="language-selector-zh_TW" data-locale="zh_TW" role="menuitem" lang="zh_TW">
                正體中文 (Chinese (Traditional))
            </button>
          </li>
<!---->      
        </ul>

          
        <button class="language-selector__button select-none relative pr-2 font-sans text-xs font-bold text-color-text-low-emphasis hover:text-color-link-hover hover:cursor-pointer focus:text-color-link-focus focus:outline-dotted focus:outline-1" aria-expanded="false" data-tracking-control-name="footer-lang-dropdown_trigger">
          <span class="language-selector__label-text mr-0.5 break-words">
            Language
          </span>
          <icon class="language-selector__label-chevron w-2 h-2 absolute top-0 right-0" data-delayed-url="https://static.licdn.com/aero-v1/sc/h/cyolgscd0imw2ldqppkrb84vo"></icon>
        </button>
      
    </div>
  
  
          
  </li>

      </ul>

<!---->    </footer>
  
  
  
      
            
  
    

    <div id="toasts" class="toasts fixed z-8 babybear:right-4 mamabear:right-4 papabear:min-h-[96px] invisible
        top:auto bottom-4 left-4 papabear:w-[400px]
        toasts--bottom" type="bottom">
    

    <template id="toast-template">
      <div class="toast container-raised flex
          toast--bottom
          transition ease-accelerate duration-xxslow
          " data-id="toast">
        <div class="toast__message flex flex-1 babybear:items-center mamabear:items-center papabear:items-start py-2 px-1.5" data-id="toast__message" role="alert" tabindex="-1">
          <div class="toast__message-content-container" data-id="toast__message-content-container">
            <p class="toast__message-content font-sans text-sm opacity-90 inline babybear:self-center mamabear:self-center papabear:self-start" data-id="toast__message-content"></p>
          </div>
        </div>
        <button class="toast__dismiss-btn cursor-pointer babybear:self-center mamabear:self-center papabear:self-start pt-3 pb-2 papabear:py-2 pl-0.5 pr-0" data-id="toast__dismiss-btn" aria-label="Close">
          <svg width="24" height="24" class="fill-color-icon"><path d="M13 4.32 9.31 8 13 11.69 11.69 13 8 9.31 4.31 13 3 11.69 6.69 8 3 4.31 4.31 3 8 6.69 11.68 3Z"></path></svg>
        </button>
      </div>
    </template>
      <template id="toast-icon-caution">
        <icon class="text-color-icon-caution toast__icon w-3 h-3 shrink-0 mr-2" data-delayed-url="https://static.licdn.com/aero-v1/sc/h/bk9xca6x9l1fga1tbzame3i3l"></icon>
      </template>
      <template id="toast-icon-error">
        <icon class="text-color-icon-negative toast__icon w-3 h-3 shrink-0 mr-2" data-delayed-url="https://static.licdn.com/aero-v1/sc/h/8c0098stai8lcqypn95r47dew"></icon>
      </template>
      <template id="toast-icon-gdpr">
        <icon class="text-color-icon-neutral toast__icon w-3 h-3 shrink-0 mr-2" data-delayed-url="https://static.licdn.com/aero-v1/sc/h/a9phzx7id2abubo45lgookfd"></icon>
      </template>
      <template id="toast-icon-notify">
        <icon class="text-color-icon-neutral toast__icon w-3 h-3 shrink-0 mr-2" data-delayed-url="https://static.licdn.com/aero-v1/sc/h/4xg53nt8deu1y7tb1t3km8tfh"></icon>
      </template>
      <template id="toast-icon-success">
        <icon class="text-color-icon-positive toast__icon w-3 h-3 shrink-0 mr-2" data-delayed-url="https://static.licdn.com/aero-v1/sc/h/9zhm3eh2dq7vh2muo8xnfikxh"></icon>
      </template>
    <template id="toast-cta">
      <a class="toast__cta cta-link font-medium ml-0.5 text-sm text-inherit inline" target="_blank"></a>
    </template>
  </div>
  

      

            <script src="https://static.licdn.com/aero-v1/sc/h/11w2cyeco40g892agkqchdc8a" async></script>
<!---->          
        
        <script src="https://static.licdn.com/aero-v1/sc/h/b48ttj0w0o6zyrfdapjcpmlu5" async defer></script>
        <script data-delayed-url="https://static.licdn.com/aero-v1/sc/h/19m2m2iij3pcbxe4bkogyzklj" data-module-id="media-player"></script>
      
      
          
<!----><!---->  
      </body>
    </html>
  
  
  