---
marp: true
theme: default
paginate: false
size: A4
style: |
  @import url('https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@400;500;700&family=Manrope:wght@400;500;700;800&display=swap');

  section {
    font-family: 'Noto Sans JP', sans-serif;
    background: var(--warm-bg);
    padding: 0;
    margin: 0;
    box-sizing: border-box;
    display: flex;
    flex-direction: column;
  }

  /* ===== カラー変数 ===== */
  :root {
    --teal: #2C8C90;
    --teal-dark: #223843;
    --teal-light: #EAF6F7;
    --warm-bg: #FAF7F2;
    --text-dark: #24343D;
    --text-mid: #5C6C74;
    --text-light: #7E8D95;
    --accent: #E67A5A;
    --line: #D7E5E8;
  }

  /* ===== ヘッダー ===== */
  .header {
    background: linear-gradient(135deg, #2C8C90 0%, #347C89 100%);
    padding: 22px 48px 18px;
    display: grid;
    grid-template-columns: minmax(0, 1fr) 300px;
    column-gap: 24px;
    align-items: center;
  }

  .header-left {
    min-width: 0;
  }

  .logo {
    font-family: 'Manrope', sans-serif;
    font-weight: 700;
    font-size: 13px;
    color: rgba(255,255,255,0.75);
    letter-spacing: 0.08em;
    margin-bottom: 6px;
  }

  .name-ja {
    font-size: 32px;
    font-weight: 700;
    color: #ffffff;
    letter-spacing: 0.02em;
    line-height: 1.15;
    margin-bottom: 4px;
  }

  .name-en {
    font-family: 'Manrope', sans-serif;
    font-size: 13px;
    font-weight: 500;
    color: rgba(255,255,255,0.8);
    letter-spacing: 0.03em;
    line-height: 1.5;
  }

  .tagline {
    display: flex;
    align-items: center;
    justify-content: center;
    background: transparent;
    border-radius: 0;
    padding: 0;
    width: 100%;
    box-sizing: border-box;
  }

  .tagline img {
    display: block;
    width: 220px;
    max-width: 100%;
    height: auto;
  }

  /* ===== UVP帯 ===== */
  .uvp-bar {
    background: var(--teal-dark);
    padding: 10px 48px;
  }

  .uvp-text {
    font-size: 14px;
    font-weight: 700;
    color: rgba(255,255,255,0.95);
    letter-spacing: 0.01em;
    line-height: 1.5;
  }

  .uvp-sub {
    font-size: 11.5px;
    color: rgba(255,255,255,0.55);
    margin-top: 2px;
    font-family: 'Manrope', sans-serif;
    font-weight: 400;
    letter-spacing: 0.05em;
  }

  /* ===== メインコンテンツ ===== */
  .main {
    display: flex;
    flex: 1;
    padding: 20px 48px 16px;
    gap: 24px;
  }

  .col-left {
    flex: 1.1;
    display: flex;
    flex-direction: column;
    gap: 14px;
  }

  .col-right {
    flex: 0.9;
    display: flex;
    flex-direction: column;
    gap: 14px;
  }

  /* ===== セクション共通 ===== */
  .section-label {
    font-family: 'Noto Sans JP', sans-serif;
    font-size: 12px;
    font-weight: 700;
    color: var(--teal);
    letter-spacing: 0.01em;
    margin-bottom: 6px;
    border-left: 3px solid var(--teal);
    padding-left: 8px;
  }

  .section-label span {
    font-family: 'Manrope', sans-serif;
    font-size: 9px;
    font-weight: 500;
    color: var(--text-light);
    letter-spacing: 0.05em;
    margin-left: 6px;
  }

  /* ===== 自己紹介文 ===== */
  .about-layout {
    display: grid;
    grid-template-columns: 124px 1fr;
    gap: 12px;
    align-items: center;
  }

  .about-photo {
    width: 124px;
    height: 124px;
    border-radius: 12px;
    overflow: hidden;
    border: 1px solid var(--line);
    background: #ffffff;
  }

  .about-photo img {
    display: block;
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: center 35%;
  }

  .bio-text {
    font-size: 12.5px;
    line-height: 1.68;
    color: #4f616a;
    font-weight: 400;
  }

  /* ===== 事業カード ===== */
  .biz-cards {
    display: flex;
    flex-direction: column;
    gap: 8px;
  }

  .biz-card {
    background: #FFFFFF;
    border: 1.5px solid var(--line);
    border-radius: 8px;
    padding: 10px 14px;
    display: flex;
    align-items: flex-start;
    gap: 12px;
  }

  .biz-icon {
    font-size: 22px;
    line-height: 1;
    flex-shrink: 0;
    margin-top: 2px;
  }

  .biz-title {
    font-size: 13px;
    font-weight: 700;
    color: var(--text-dark);
    margin-bottom: 3px;
  }

  .biz-desc {
    font-size: 11px;
    color: var(--text-light);
    line-height: 1.7;
  }

  .biz-tag {
    font-family: 'Manrope', sans-serif;
    font-size: 9px;
    font-weight: 600;
    color: var(--teal);
    background: var(--teal-light);
    border-radius: 3px;
    padding: 2px 6px;
    display: inline-block;
    margin-top: 4px;
    letter-spacing: 0.05em;
  }

  /* ===== 強み ===== */
  .strength-list {
    display: flex;
    flex-direction: column;
    gap: 6px;
  }

  .strength-item {
    display: flex;
    align-items: flex-start;
    gap: 10px;
    font-size: 12px;
    color: var(--text-mid);
    line-height: 1.5;
  }

  .strength-num {
    font-family: 'Manrope', sans-serif;
    font-size: 18px;
    font-weight: 800;
    color: var(--teal);
    line-height: 1;
    flex-shrink: 0;
    width: 24px;
  }

  /* ===== キーワードタグ ===== */
  .tags {
    display: flex;
    flex-wrap: wrap;
    gap: 6px;
    margin-top: 4px;
  }

  .tag {
    font-size: 11px;
    color: var(--text-mid);
    background: #F0F5F7;
    border-radius: 4px;
    padding: 4px 10px;
  }

  /* ===== CTA ===== */
  .cta-box {
    background: #FFF7F3;
    border: 1px solid #F0D7CD;
    border-radius: 8px;
    padding: 12px 14px;
    display: flex;
    align-items: center;
    gap: 16px;
  }

  .cta-qr {
    width: 72px;
    height: 72px;
    background: #ffffff;
    border: 1px solid #d4e5ea;
    border-radius: 6px;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-shrink: 0;
    overflow: hidden;
  }

  .cta-qr img {
    display: block;
    width: 100%;
    height: 100%;
    object-fit: cover;
  }

  .cta-text {}

  .cta-title {
    font-size: 12px;
    font-weight: 700;
    color: var(--text-dark);
    margin-bottom: 4px;
  }

  .cta-handle {
    font-family: 'Manrope', sans-serif;
    font-size: 14px;
    font-weight: 800;
    color: var(--accent);
    letter-spacing: 0.03em;
    display: block;
    line-height: 1.2;
    margin: 0;
    text-decoration: none;
  }

  .cta-desc {
    font-size: 10.5px;
    color: var(--text-light);
    margin-top: 3px;
    line-height: 1.5;
    font-weight: 400;
  }

  /* ===== フッター ===== */
  .footer {
    background: var(--teal-dark);
    min-height: 36px;
    padding: 0 48px;
    display: grid;
    grid-template-columns: auto 1fr;
    column-gap: 16px;
    align-items: center;
  }

  .footer-logo {
    font-family: 'Manrope', sans-serif;
    font-size: 12px;
    font-weight: 700;
    color: rgba(255,255,255,0.5);
    letter-spacing: 0.1em;
    display: block;
    line-height: 1.2;
    margin: 0;
    transform: none;
    align-self: center;
    text-decoration: none;
  }

  .footer-links {
    font-size: 10px;
    color: rgba(255,255,255,0.4);
    letter-spacing: 0.05em;
    display: block;
    line-height: 1.2;
    margin: 0;
    transform: none;
    align-self: center;
    justify-self: end;
  }
---

<div class="header">
  <div class="header-left">
    <div class="name-ja">西村耕太郎</div>
    <div class="name-en">Nishimura Kohtaro<br>Web Partner for Growth</div>
  </div>
  <div class="tagline">
    <img src="Logotype_white.png" alt="COBWEB logo">
  </div>
</div>

<div class="uvp-bar">
  <div class="uvp-text">集客と売上まで考える Web パートナー</div>
</div>

<div class="main">
  <div class="col-left">

  <div>
    <div class="section-label">私について <span>ABOUT</span></div>
    <div class="about-layout">
      <div class="about-photo">
        <img src="DSC08540.jpg" alt="西村耕太郎のプロフィール写真">
      </div>
      <div class="bio-text">
        沖縄を拠点に、Web制作・SNS運用・動画制作から<br>
        たこ焼き屋台まで、複数の事業を実践しながら<br>
        「ビジョンを形にする」をテーマに活動しています。<br>
        <br>
        SUNABACOコミュニティで学び続けながら、<br>
        デザインとITで地域のビジネスを支援しています。
      </div>
    </div>
  </div>

  <div>
    <div class="section-label">できること <span>SERVICE</span></div>
    <div class="biz-cards">
      <div class="biz-card">
        <div class="biz-icon">🌐</div>
        <div>
          <div class="biz-title">COBWEB — Web制作・集客支援</div>
          <div class="biz-desc">Webサイト制作〜SNS運用・動画制作・システム開発まで一貫対応。<br>月次報告でデータ経営をサポート。</div>
          <span class="biz-tag">Web Design</span>
          <span class="biz-tag">SNS Marketing</span>
          <span class="biz-tag">AI × Data</span>
        </div>
      </div>
      <div class="biz-card">
        <div class="biz-icon">🐙</div>
        <div>
          <div class="biz-title">やんばる あちこーこー たこ焼き — ファーマーズマーケット出店</div>
          <div class="biz-desc">焼き立て10〜15分、1時間鮮度キープ。<br>ITとデザインを活用した効率的な屋台運営。</div>
          <span class="biz-tag">Local Business</span>
          <span class="biz-tag">Food Stall</span>
        </div>
      </div>
    </div>
  </div>

  </div>

  <div class="col-right">

  <div>
    <div class="section-label">選ばれる理由 <span>STRENGTH</span></div>
    <div class="strength-list">
      <div class="strength-item">
        <div class="strength-num">01</div>
        <div>
          <strong>制作だけで終わらない</strong><br>
          カスタマージャーニーに沿ったWeb集客戦略で、売上アップまでコミット
        </div>
      </div>
      <div class="strength-item">
        <div class="strength-num">02</div>
        <div>
          <strong>データ×デザイン×ITの三位一体</strong><br>
          GAS自動化・AI分析・SNS運用を経営に直結させる実践者
        </div>
      </div>
      <div class="strength-item">
        <div class="strength-num">03</div>
        <div>
          <strong>学び続けるスタンス</strong><br>
          SUNABACO受講・PBL参加で最新技術を常にアップデート中
        </div>
      </div>
    </div>
  </div>

  <div>
    <div class="section-label">キーワード <span>KEYWORDS</span></div>
    <div class="tags">
      <span class="tag">#Webデザイン</span>
      <span class="tag">#SNSマーケ</span>
      <span class="tag">#GAS自動化</span>
      <span class="tag">#SUNABACO</span>
      <span class="tag">#沖縄</span>
      <span class="tag">#起業家</span>
      <span class="tag">#デザイン経営</span>
    </div>
  </div>

  <div>
    <div class="section-label">つながる <span>CONNECT</span></div>
    <div class="cta-box">
      <div class="cta-qr">
        <img src="Adobe Express QR Code.png" alt="X QR code">
      </div>
      <div class="cta-text">
        <div class="cta-title">Xで日々の発信を見る</div>
        <a class="cta-handle" href="https://x.com/nishikohh" target="_blank" rel="noopener noreferrer">@nishikohh</a>
        <div class="cta-desc">デザイン・Web集客・事業の<br>リアルな進捗を毎日発信中</div>
      </div>
    </div>
  </div>

  </div>
</div>

<div class="footer">
  <a class="footer-logo" href="https://cobwebokinawa.studio.site" target="_blank" rel="noopener noreferrer">cobwebokinawa.studio.site</a>
  <div class="footer-links">Web制作のご相談 · Webマーケ · SNS運用 · システム開発</div>
</div>
