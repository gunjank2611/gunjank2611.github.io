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
  
  
  