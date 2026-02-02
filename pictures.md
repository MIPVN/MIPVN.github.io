---
title: Pictures
permalink: /pictures/
---

<style>
  /* 页面基础排版 */
  .gallery-wrapper {
    max-width: 1200px;
    margin: 0 auto;
    font-family: "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
  }
  
  .page-title {
    text-align: center;
    color: #2c3e50;
    margin: 40px 0 10px;
    font-size: 32px;
  }
  
  .page-subtitle {
    text-align: center;
    color: #7f8c8d;
    margin-bottom: 50px;
  }

  /* 响应式网格系统 */
  .photo-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 25px;
    justify-content: center;
    padding: 20px 0;
  }

  /* 统一卡片样式 */
  .item-card {
    width: 350px; /* 统一宽度 */
    background: #fff;
    border-radius: 12px;
    box-shadow: 0 4px 15px rgba(0,0,0,0.08);
    overflow: hidden;
    display: flex;
    flex-direction: column;
    transition: transform 0.3s ease;
  }
  
  .item-card:hover {
    transform: translateY(-8px);
    box-shadow: 0 8px 25px rgba(0,0,0,0.15);
  }

  /* 媒体容器：确保所有图片/视频比例一致 (16:9) */
  .media-box {
    width: 100%;
    height: 200px;
    overflow: hidden;
    background: #f0f0f0;
  }
  
  .media-box img, .media-box video {
    width: 100%;
    height: 100%;
    object-fit: cover; /* 自动裁剪，填满容器不留白 */
  }

  /* 文字区域：统一对齐 */
  .info-box {
    padding: 15px;
    text-align: center; /* 文字居中 */
    flex-grow: 1;
    display: flex;
    flex-direction: column;
    justify-content: center;
    border-top: 1px solid #f5f5f5;
  }

  .date-tag {
    font-size: 12px;
    color: #007bff;
    font-weight: bold;
    text-transform: uppercase;
    margin-bottom: 5px;
  }

  .description {
    font-size: 15px;
    color: #34495e;
    line-height: 1.4;
    font-weight: 500;
  }

  /* 时间线分割标题 */
  .year-divider {
    width: 100%;
    text-align: left;
    margin: 40px 0 20px;
    padding-left: 20px;
    border-left: 5px solid #007bff;
    font-size: 24px;
    color: #2c3e50;
    font-weight: bold;
  }
</style>




<div class="gallery-wrapper">
  
  <h1 class="page-title">📸 Group Gallery</h1>
  <p class="page-subtitle">Memories of research, celebrations, and friendships at MIPVN Lab.</p>

  <div class="year-divider">2026 - 2025</div>
  <div class="photo-grid">
    
    <div class="item-card">
      <div class="media-box"><img src="{{site.baseurl}}/images/home/2026_01_31_课题组年会/课题组年会合影.jpg"></div>
      <div class="info-box">
        <div class="date-tag">Jan 2026</div>
        <div class="description">MIPVN Group Annual Photo</div>
      </div>
    </div>

    <div class="item-card">
      <div class="media-box">
        <video controls><source src="{{site.baseurl}}/images/home/2026_01_31_课题组年会/年会活动开场.mp4" type="video/mp4"></video>
      </div>
      <div class="info-box">
        <div class="date-tag">Jan 2026</div>
        <div class="description">Annual Party Opening Highlights</div>
      </div>
    </div>

    <div class="item-card">
      <div class="media-box"><img src="{{site.baseurl}}/images/home/2026_01_31_课题组年会/年会聚餐_蒜蓉小青龙.jpg"></div>
      <div class="info-box">
        <div class="date-tag">Jan 2026</div>
        <div class="description">Annual Dinner: Delicious Moments</div>
      </div>
    </div>

    <div class="item-card">
      <div class="media-box">
        <video controls><source src="{{site.baseurl}}/images/home/2026_01_31_课题组年会/年会聚餐.mp4" type="video/mp4"></video>
      </div>
      <div class="info-box">
        <div class="date-tag">Jan 2026</div>
        <div class="description">Dinner Party Video</div>
      </div>
    </div>

    <div class="item-card">
      <div class="media-box"><img src="{{site.baseurl}}/images/home/2026_01_31_课题组年会/年会小活动.jpg"></div>
      <div class="info-box">
        <div class="date-tag">Jan 2026</div>
        <div class="description">Group Fun Activities</div>
      </div>
    </div>
  </div>

  <div class="year-divider">2024</div>
  <div class="photo-grid">
    <div class="item-card">
      <div class="media-box"><img src="{{site.baseurl}}/images/home/2024_animal.jpg"></div>
      <div class="info-box">
        <div class="date-tag">Apr 2024</div>
        <div class="description">Undergraduate Students with Our Lab</div>
      </div>
    </div>

    <div class="item-card">
      <div class="media-box"><img src="{{site.baseurl}}/images/home/2024_01_all_members.jpg"></div>
      <div class="info-box">
        <div class="date-tag">Jan 2024</div>
        <div class="description">Full Lab Membership Photo</div>
      </div>
    </div>
  </div>

  <div class="year-divider">2023 - 2022</div>
  <div class="photo-grid">
    <div class="item-card">
      <div class="media-box"><img src="{{site.baseurl}}/images/home/2024_group_photo1.jpg"></div>
      <div class="info-box">
        <div class="date-tag">Jan 2023</div>
        <div class="description">Undergraduate Research Group</div>
      </div>
    </div>

    <div class="item-card">
      <div class="media-box"><img src="{{site.baseurl}}/images/home/2022_0623.jpg"></div>
      <div class="info-box">
        <div class="date-tag">Jun 2022</div>
        <div class="description">Thesis Defense: Yutao Hu & Anran Zhang</div>
      </div>
    </div>
  </div>

  <div class="year-divider">2021</div>
  <div class="photo-grid">
    <div class="item-card">
      <div class="media-box"><img src="{{site.baseurl}}/images/home/2021_12_31_元旦聚餐.jpg"></div>
      <div class="info-box">
        <div class="date-tag">Dec 2021</div>
        <div class="description">New Year Celebration Dinner</div>
      </div>
    </div>

    <div class="item-card">
      <div class="media-box"><img src="{{site.baseurl}}/images/home/2021_12_skiing.jpg"></div>
      <div class="info-box">
        <div class="date-tag">Dec 2021</div>
        <div class="description">Lab Outing: Skiing Trip</div>
      </div>
    </div>

    <div class="item-card">
      <div class="media-box"><img src="{{site.baseurl}}/images/home/2021_10_24_lxy_birthday.jpg"></div>
      <div class="info-box">
        <div class="date-tag">Oct 2021</div>
        <div class="description">Prof. Luo's Birthday Celebration</div>
      </div>
    </div>

    <div class="item-card">
      <div class="media-box"><img src="{{site.baseurl}}/images/home/group_old.jpg"></div>
      <div class="info-box">
        <div class="date-tag">Jan 2021</div>
        <div class="description">Early Days Group Reunion</div>
      </div>
    </div>
  </div>

</div>