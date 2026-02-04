<script lang="ts">
  import ContactModal from './lib/ContactModal.svelte';

  let contactOpen = $state(false);

  const apps = [
    { name: 'Portfolio', url: 'https://portfolio.hatstack.fun' },
    { name: 'Tracker', url: 'https://tracker.hatstack.fun' },
    { name: 'Writer', url: 'https://writer.hatstack.fun' },
    { name: 'Gemenie Labs', url: 'https://gemenielabs.hatstack.fun' },
    { name: 'Family Archive - Document AI', url: 'https://showcase-htt.hatstack.fun' },
    { name: 'Family', url: 'https://family.hatstack.fun' },
    { name: 'Float', url: 'https://float.hatstack.fun' },
    { name: 'Looper', url: 'https://looper.hatstack.fun' },
    { name: 'Movies', url: 'https://movies.hatstack.fun' },
    { name: 'Trachtenberg', url: 'https://trachtenberg.hatstack.fun' },
    { name: 'Vocabulary', url: 'https://vocabulary.hatstack.fun' },
    { name: 'Credentials', url: 'https://credentials.hatstack.fun' },
    { name: 'SavorSwipe', url: 'https://savorswipe.hatstack.fun' },
  ];

  const lastUpdated = 'January 31, 2026';
</script>

<ContactModal bind:open={contactOpen} />

<header>
  <div class="header-content">
    <div class="logo">Gemenie Labs</div>
    <button class="contact-btn" onclick={() => contactOpen = true}>Contact Us</button>
  </div>
</header>

<nav class="app-nav">
  <div class="nav-content">
    <span class="nav-label">Our Apps:</span>
    <div class="app-links">
      {#each apps as app}
        <a href={app.url} target="_blank" rel="noopener noreferrer">{app.name}</a>
      {/each}
    </div>
  </div>
</nav>

<main>
  <article>
    <h1>Privacy Policy</h1>
    <p class="last-updated">Last updated: {lastUpdated}</p>

    <section>
      <p>Gemenie Labs LLC ("we," "us," or "our") respects the privacy of our users ("user" or "you"). This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you use our mobile applications, websites, and related services (collectively, the "Services"). This policy applies to all applications listed above and any other services operated by Gemenie Labs LLC.</p>

      <p><strong>Please read this Privacy Policy carefully. By accessing or using our Services, you acknowledge that you have read, understood, and agree to be bound by this Privacy Policy. If you do not agree with the terms of this Privacy Policy, please do not access or use the Services.</strong></p>
    </section>

    <h2>Changes to This Privacy Policy</h2>
    <section>
      <p>We reserve the right to make changes to this Privacy Policy at any time. We will notify you of any material changes by updating the "Last updated" date and, where appropriate, through in-app notifications or email. You are encouraged to periodically review this Privacy Policy to stay informed of updates. Your continued use of the Services after the date of any revised Privacy Policy constitutes your acceptance of the changes.</p>
    </section>

    <h2>Information We Collect</h2>
    <section>
      <p>We may collect information about you in a variety of ways depending on which Services you use. The information we collect falls into the following categories:</p>

      <h3>Information You Provide Directly</h3>
      <ul>
        <li><strong>Account Information:</strong> When you create an account, we may collect your name, email address, and password. Some Services offer authentication through third-party providers (such as Google), in which case we receive basic profile information from those providers.</li>
        <li><strong>Profile Information:</strong> You may choose to provide additional information for your profile, such as a display name or profile picture.</li>
        <li><strong>User-Generated Content:</strong> Content you create, upload, or share through our Services, including text, images, documents, recipes, audio recordings, and other media.</li>
        <li><strong>Audio Recordings:</strong> Some Services allow you to record audio using your device's microphone. These recordings may be processed locally, transmitted to our servers, or sent to third-party AI services for transcription and analysis.</li>
        <li><strong>Communications:</strong> Information you provide when you contact us for support, submit feedback, or participate in surveys.</li>
      </ul>

      <h3>Information Collected Automatically</h3>
      <ul>
        <li><strong>Device Information:</strong> Device type, operating system version, unique device identifiers, and general hardware information.</li>
        <li><strong>Usage Data:</strong> Information about how you interact with our Services, including features used, content viewed, and actions taken within the app.</li>
        <li><strong>Log Data:</strong> Server logs that may include your IP address, browser type, referring/exit pages, and timestamps.</li>
        <li><strong>Local Storage Data:</strong> Many of our Services store data locally on your device (using technologies like AsyncStorage, SQLite, or localStorage) to provide offline functionality and remember your preferences. This data typically remains on your device and is not transmitted to our servers unless you explicitly sync or back up your data.</li>
      </ul>

      <h3>Device Permissions</h3>
      <p>Depending on the Service, we may request access to certain device features:</p>
      <ul>
        <li><strong>Microphone:</strong> To record audio for voice input, transcription, or content creation features.</li>
        <li><strong>Notifications:</strong> To send you push notifications, reminders, and updates related to your use of the Services.</li>
        <li><strong>Camera:</strong> To capture photos or scan documents within certain Services.</li>
        <li><strong>Storage:</strong> To save and access files on your device.</li>
      </ul>
      <p>You can manage these permissions through your device settings at any time.</p>

      <h3>Health and Wellness Data</h3>
      <p>Certain Services may collect information related to your health, wellness, or emotional state, including:</p>
      <ul>
        <li>Emotional state indicators and sentiment information you provide</li>
        <li>Voice recordings describing personal experiences or feelings</li>
        <li>Responses to wellness-related prompts or check-ins</li>
      </ul>
      <p>This information is used solely to provide personalized features within the Service (such as guided meditations or wellness content) and is treated with heightened confidentiality. We do not share health and wellness data with third parties for marketing purposes.</p>

      <h3>Information from Third-Party Services</h3>
      <p>When you connect your account to third-party services or use features that integrate with external platforms, we may receive information from those services as permitted by their privacy policies and your settings. This may include:</p>
      <ul>
        <li>Basic profile information from authentication providers (Google, etc.)</li>
        <li>Content from external APIs you choose to access through our Services</li>
      </ul>
    </section>

    <h2>Third-Party Services and AI Processing</h2>
    <section>
      <p>Some of our Services utilize third-party services and artificial intelligence technologies to provide enhanced functionality:</p>

      <h3>Cloud Infrastructure (Amazon Web Services)</h3>
      <p>We use AWS services including Lambda, S3, DynamoDB, Cognito, and SES to host, store, and process data. AWS processes data in accordance with their privacy policy and applicable data processing agreements.</p>

      <h3>AI and Machine Learning Services</h3>
      <p>Certain Services may use AI technologies for features such as:</p>
      <ul>
        <li><strong>Google Gemini API:</strong> Used for content analysis, text generation, transcription services, and sentiment analysis. Audio recordings and text you provide may be sent to Google for processing.</li>
        <li><strong>OpenAI APIs:</strong> Used for image analysis (Vision) and text-to-speech generation. Content and generated text may be sent to OpenAI for processing.</li>
      </ul>
      <p>When you use features powered by these AI services, relevant content (including audio recordings, text, and images) may be transmitted to these providers for processing. We do not use your personal data to train AI models. Please review the privacy policies of <a href="https://policies.google.com/privacy" target="_blank" rel="noopener noreferrer">Google</a> and <a href="https://openai.com/privacy" target="_blank" rel="noopener noreferrer">OpenAI</a> for more information about how they handle data.</p>

      <h3>External Content APIs</h3>
      <p>Some Services retrieve content from external sources such as:</p>
      <ul>
        <li>TMDb (The Movie Database) for movie information</li>
        <li>YouTube for video content</li>
        <li>Google Custom Search for web search functionality</li>
      </ul>
      <p>Your interactions with these external services are subject to their respective privacy policies.</p>
    </section>

    <h2>How We Use Your Information</h2>
    <section>
      <p>We use the information we collect to:</p>
      <ul>
        <li>Provide, maintain, and improve our Services</li>
        <li>Create and manage your account</li>
        <li>Process your requests and transactions</li>
        <li>Generate personalized content based on your inputs (such as guided meditations or recommendations)</li>
        <li>Send you technical notices, updates, and support messages</li>
        <li>Send push notifications including reminders, follow-up check-ins, and feature updates</li>
        <li>Respond to your comments, questions, and customer service requests</li>
        <li>Monitor and analyze usage patterns and trends</li>
        <li>Detect, prevent, and address technical issues, fraud, or security concerns</li>
        <li>Comply with legal obligations and enforce our terms</li>
        <li>Personalize your experience within our Services</li>
      </ul>
    </section>

    <h2>Push Notifications</h2>
    <section>
      <p>Some of our Services may send push notifications to your device. These notifications may include:</p>
      <ul>
        <li>Reminders and follow-up check-ins based on your activity within the app</li>
        <li>Updates about new features or content</li>
        <li>Important account or service-related messages</li>
      </ul>
      <p>Push notification timing and content may be personalized based on your interactions with the Service. You can disable push notifications at any time through your device settings or within the app's notification preferences.</p>
    </section>

    <h2>How We Share Your Information</h2>
    <section>
      <p>We do not sell your personal information. We may share your information in the following circumstances:</p>

      <h3>Service Providers</h3>
      <p>We share information with third-party vendors who perform services on our behalf, such as hosting, data analysis, payment processing, and customer support. These providers are contractually obligated to protect your information and use it only for the purposes we specify.</p>

      <h3>Legal Requirements</h3>
      <p>We may disclose your information if required to do so by law or in response to valid legal requests by public authorities (e.g., court orders or government agencies).</p>

      <h3>Protection of Rights</h3>
      <p>We may disclose information when we believe disclosure is necessary to protect our rights, investigate potential violations of our terms, or protect the safety of our users or others.</p>

      <h3>Business Transfers</h3>
      <p>If we are involved in a merger, acquisition, or sale of assets, your information may be transferred as part of that transaction. We will notify you of any change in ownership or use of your personal information.</p>

      <h3>With Your Consent</h3>
      <p>We may share your information with third parties when you give us explicit consent to do so.</p>
    </section>

    <h2>Data Retention</h2>
    <section>
      <p>We retain your information for as long as necessary to provide the Services you have requested, or for other essential purposes such as complying with legal obligations, resolving disputes, and enforcing our agreements. When data is no longer needed, we will delete or anonymize it in accordance with our data retention policies.</p>

      <p>Data stored locally on your device (such as app preferences, progress, or cached content) remains on your device until you clear the app's data or uninstall the application.</p>
    </section>

    <h2>Data Security</h2>
    <section>
      <p>We implement appropriate technical and organizational security measures to protect your personal information against unauthorized access, alteration, disclosure, or destruction. These measures include encryption, secure authentication protocols, and regular security assessments.</p>

      <p>However, no method of transmission over the Internet or electronic storage is 100% secure. While we strive to protect your personal information, we cannot guarantee its absolute security. You are responsible for maintaining the confidentiality of your account credentials.</p>
    </section>

    <h2>Your Privacy Rights</h2>
    <section>
      <p>Depending on your location, you may have certain rights regarding your personal information:</p>

      <h3>Access and Portability</h3>
      <p>You may request access to the personal information we hold about you and, where applicable, receive it in a portable format.</p>

      <h3>Correction</h3>
      <p>You may request that we correct inaccurate or incomplete personal information.</p>

      <h3>Deletion</h3>
      <p>You may request that we delete your personal information, subject to certain legal exceptions.</p>

      <h3>Restriction and Objection</h3>
      <p>You may request that we restrict processing of your personal information or object to certain processing activities.</p>

      <h3>Withdraw Consent</h3>
      <p>Where we rely on consent to process your information, you may withdraw that consent at any time.</p>

      <p>To exercise any of these rights, please contact us using the information provided below. We will respond to your request within the timeframe required by applicable law.</p>
    </section>

    <h2>California Privacy Rights (CCPA)</h2>
    <section>
      <p>If you are a California resident, the California Consumer Privacy Act (CCPA) provides you with specific rights regarding your personal information:</p>
      <ul>
        <li><strong>Right to Know:</strong> You have the right to request disclosure of the categories and specific pieces of personal information we have collected about you.</li>
        <li><strong>Right to Delete:</strong> You have the right to request deletion of your personal information, subject to certain exceptions.</li>
        <li><strong>Right to Opt-Out:</strong> You have the right to opt out of the "sale" of your personal information. We do not sell personal information as defined by the CCPA.</li>
        <li><strong>Right to Non-Discrimination:</strong> We will not discriminate against you for exercising your CCPA rights.</li>
      </ul>
      <p>To submit a request, please contact us using the information below. You may also designate an authorized agent to make a request on your behalf.</p>
    </section>

    <h2>European Privacy Rights (GDPR)</h2>
    <section>
      <p>If you are located in the European Economic Area (EEA), United Kingdom, or Switzerland, you have additional rights under the General Data Protection Regulation (GDPR):</p>
      <ul>
        <li>The right to access, correct, or delete your personal data</li>
        <li>The right to restrict or object to processing</li>
        <li>The right to data portability</li>
        <li>The right to lodge a complaint with a supervisory authority</li>
      </ul>
      <p>Our legal basis for processing personal information depends on the specific context: performance of a contract, your consent, our legitimate interests, or compliance with legal obligations.</p>
    </section>

    <h2>Children's Privacy</h2>
    <section>
      <p>Our Services are not directed to children under the age of 13 (or 16 in certain jurisdictions). We do not knowingly collect personal information from children under these ages. If you are a parent or guardian and believe your child has provided us with personal information, please contact us immediately. If we discover that we have collected personal information from a child in violation of applicable law, we will promptly delete that information.</p>
    </section>

    <h2>International Data Transfers</h2>
    <section>
      <p>Your information may be transferred to and processed in countries other than your country of residence, including the United States, where data protection laws may differ. We take appropriate safeguards to ensure that your personal information remains protected in accordance with this Privacy Policy and applicable law.</p>
    </section>

    <h2>Do Not Track Signals</h2>
    <section>
      <p>Some browsers include a "Do Not Track" (DNT) feature that signals to websites that you do not want your online activity tracked. Because there is no universally accepted standard for how to respond to DNT signals, our Services do not currently respond to DNT browser signals. However, you can manage your privacy preferences through your device settings and the options we provide within our Services.</p>
    </section>

    <h2>Third-Party Links</h2>
    <section>
      <p>Our Services may contain links to third-party websites, applications, or services that are not operated by us. This Privacy Policy does not apply to those third-party services. We encourage you to review the privacy policies of any third-party services you access through our Services.</p>
    </section>

    <h2>App Store Disclosures</h2>
    <section>
      <p>Our mobile applications are distributed through app stores operated by third parties (such as the Apple App Store and Google Play Store). These stores may collect and use data about you in accordance with their own privacy policies. Please review the privacy policies of the applicable app stores for information about their data practices.</p>
    </section>

    <h2>Contact Us</h2>
    <section>
      <p>If you have questions, concerns, or requests regarding this Privacy Policy or our privacy practices, please contact us using the "Contact Us" button above.</p>

      <p>We will respond to your inquiry within a reasonable timeframe and in accordance with applicable law.</p>
    </section>
  </article>
</main>

<footer>
  <div class="footer-content">
    <p>&copy; {new Date().getFullYear()} Gemenie Labs LLC. All rights reserved.</p>
    <button class="footer-contact" onclick={() => contactOpen = true}>Contact Us</button>
  </div>
</footer>

<style>
  header {
    background: #141414;
    border-bottom: 1px solid #262626;
    position: sticky;
    top: 0;
    z-index: 50;
  }

  .header-content {
    max-width: 900px;
    margin: 0 auto;
    padding: 1rem 1.5rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .logo {
    font-size: 1.25rem;
    font-weight: 600;
    color: #f5f5f5;
  }

  .contact-btn {
    background: #3b82f6;
    color: white;
    border: none;
    border-radius: 6px;
    padding: 0.5rem 1rem;
    font-size: 0.875rem;
    cursor: pointer;
    transition: background 0.2s;
  }

  .contact-btn:hover {
    background: #2563eb;
  }

  .app-nav {
    background: #0f0f0f;
    border-bottom: 1px solid #262626;
    overflow-x: auto;
  }

  .nav-content {
    max-width: 900px;
    margin: 0 auto;
    padding: 0.75rem 1.5rem;
    display: flex;
    align-items: center;
    gap: 1rem;
  }

  .nav-label {
    color: #737373;
    font-size: 0.875rem;
    white-space: nowrap;
  }

  .app-links {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
  }

  .app-links a {
    background: #1a1a1a;
    border: 1px solid #262626;
    border-radius: 4px;
    padding: 0.25rem 0.75rem;
    font-size: 0.75rem;
    color: #a3a3a3;
    white-space: nowrap;
    transition: all 0.2s;
  }

  .app-links a:hover {
    background: #262626;
    color: #e5e5e5;
    text-decoration: none;
    border-color: #3b82f6;
  }

  main {
    max-width: 900px;
    margin: 0 auto;
    padding: 2rem 1.5rem 4rem;
  }

  article {
    background: #141414;
    border: 1px solid #262626;
    border-radius: 12px;
    padding: 2rem;
  }

  @media (max-width: 768px) {
    article {
      padding: 1.5rem;
      border-radius: 0;
      border-left: none;
      border-right: none;
    }

    main {
      padding: 1rem 0 3rem;
    }
  }

  .last-updated {
    color: #737373;
    font-size: 0.875rem;
    margin-bottom: 2rem;
  }

  section {
    margin-bottom: 1rem;
  }

  footer {
    background: #0f0f0f;
    border-top: 1px solid #262626;
    padding: 2rem 1.5rem;
  }

  .footer-content {
    max-width: 900px;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 1rem;
  }

  .footer-content p {
    margin: 0;
    color: #737373;
    font-size: 0.875rem;
  }

  .footer-contact {
    background: transparent;
    border: 1px solid #262626;
    color: #a3a3a3;
    border-radius: 6px;
    padding: 0.5rem 1rem;
    font-size: 0.875rem;
    cursor: pointer;
    transition: all 0.2s;
  }

  .footer-contact:hover {
    border-color: #3b82f6;
    color: #e5e5e5;
  }
</style>
