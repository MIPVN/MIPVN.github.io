---
title: Reference
permalink: /presentations/
---

<style>
    .ref-container { 
        max-width: 1000px; 
        margin: 0 auto; 
    }

    /* 顶部介绍区：字号对齐首页 18px */
    .intro-banner {
        background: #f8f9fa;
        padding: 25px;
        border-radius: 12px;
        border-left: 4px solid #0056b3;
        margin-bottom: 40px;
    }
    .intro-banner h1 { 
        font-weight: 800; color: #2c3e50; font-size: 36px; margin-top: 0;
    }
    .intro-banner p { 
        font-size: 18px; line-height: 1.6; color: #546e7a; text-align: justify;
    }

    /* 表格样式：字号对齐首页 16px */
    .meeting-table {
        width: 100%;
        border-collapse: collapse;
        margin: 25px 0;
        border: 1px solid #eee;
    }
    .meeting-table th { 
        background-color: #f8f9fa; 
        color: #0056b3; 
        text-align: left; 
        padding: 12px 15px; 
        font-size: 16px; 
        font-weight: bold;
        border-bottom: 2px solid #0056b3;
    }
    .meeting-table td { 
        padding: 12px 15px; 
        border-bottom: 1px solid #eee; 
        font-size: 16px; 
        color: #34495e;
    }

    /* 列表与标签：字号对齐首页 15px/11px */
    .section-title { 
        font-size: 24px; color: #2c3e50; border-bottom: 2px solid #6EACDA; 
        display: inline-block; margin: 40px 0 20px; 
    }
    .list-item { 
        padding: 10px 0; display: flex; align-items: baseline; gap: 10px;
    }
    .list-post-title a { 
        color: #007bff; text-decoration: none; font-size: 15px; 
    }
    .list-post-title a:hover { text-decoration: underline; }
    
    .post-date { 
        background: #007bff; color: #fff; padding: 2px 8px; 
        border-radius: 4px; font-size: 11px; white-space: nowrap;
    }

    .custom-hr { border: 0; border-top: 1px solid #eee; margin: 40px 0; }
</style>

<div class="ref-container">

    <div class="intro-banner" style="background: linear-gradient(135deg, #f8fbff 0%, #f0f7ff 100%); padding: 35px; border-radius: 15px; border-left: 6px solid #0056b3; box-shadow: 0 4px 15px rgba(0,0,0,0.05); margin-bottom: 40px;">
        <h1 style="font-weight: 800; color: #2c3e50; font-size: 36px; margin: 0 0 20px 0; display: flex; align-items: center; gap: 15px;"> 
            <span style="font-size: 30px;">🎤</span> Lab Meetings
        </h1>
        
        <p style="font-size: 18px; line-height: 1.8; color: #455a64; text-align: justify; margin: 0;">
            Every week, we get together 
            <span style="background: rgba(0,123,255,0.08); padding: 2px 6px; border-radius: 4px; color: #0056b3; font-weight: 500;">mix of virtual and in-person</span> 
            for lab presentations 
            <span style="border-bottom: 2px dashed #e67e22; color: #e67e22; font-weight: bold;">(with food! sometimes)</span>. 
        </p>

        <div style="margin-top: 20px; padding-top: 20px; border-top: 1px solid rgba(0,86,179,0.1); font-size: 17px; color: #607d8b; line-height: 1.6;">
            On a rotating basis, each member speaks and teaches about something they know—anything from Python packages and new findings to 
literature reviews. 
            It's all about sharing knowledge!
        </div>
    </div>

    <hr class="custom-hr">

    <h3 style="font-weight: bold; color: #2c3e50; font-size: 24px; margin-bottom: 15px;">🗓️ Upcoming Schedule</h3>
    <table class="meeting-table">
        <thead>
            <tr>
                <th style="width: 25%;">Date</th>
                <th style="width: 25%;">Name</th>
                <th>Topic</th>
            </tr>
        </thead>
        <tbody>
            {% assign current_date = "now" | date: "%s" | plus: 0 %}
            {% assign sorted_meetings = site.data.meetings | sort: "date" %}
            {% assign has_upcoming = false %}

            {% for meeting in sorted_meetings %}
                {% assign meeting_date = meeting.date | date: "%s" | plus: 0 %}
                
                {% if meeting_date >= current_date %}
                    <tr>
                        <td>{{ meeting.date }}</td>
                        <td>{{ meeting.name }}</td>
                        <td>{{ meeting.topic }}</td>
                    </tr>
                    {% assign has_upcoming = true %}
                {% endif %}
            {% endfor %}

            {% if has_upcoming == false %}
            <tr>
                <td colspan="3" style="text-align: center; color: #95a5a6; padding: 20px;">No upcoming meetings scheduled.</td>
            </tr>
            {% endif %}
        </tbody>
    </table>

  
    <div class="blog-section">
      <h3 class="section-title">Blogs & Short Essays</h3>
      
      <div class="news-list" style="margin-top: 10px;"> {% capture one_year_ago %}{{ 'now' | date: '%s' | minus: 31104000 }}{% endcapture %}
        
        <ul style="list-style: none; padding: 0; margin: 0;"> {% assign has_recent_posts = false %}
          
          {% for post in site.posts %}
            {% if post.categories contains 'blog' %}
              {% capture post_date_seconds %}{{ post.date | date: '%s' }}{% endcapture %}
              
              {% if post_date_seconds > one_year_ago %}
                <li style="margin-bottom: 8px; display: flex; align-items: flex-start; gap: 12px;"> <span class="post-date" style="background: #007bff; color: #fff; padding: 2px 8px; border-radius: 4px; font-size: 11px; font-weight: bold; min-width: 65px; text-align: center; margin-top: 2px; white-space: nowrap;">
                    {{ post.date | date: "%b %Y" }}
                  </span>
                  
                  <span style="font-size: 15px; color: #2c3e50; line-height: 1.4;">
                    <a href="{{ site.baseurl }}{{ post.url }}" style="color: #007bff; text-decoration: none;">
                      {{ post.title }}
                    </a>
                  </span>
                </li>
                {% assign has_recent_posts = true %}
              {% endif %}
            {% endif %}
          {% endfor %}

          {% if has_recent_posts == false %}
            <li style="font-size: 15px; color: #95a5a6; font-style: italic;">No blog posts in the last year.</li>
          {% endif %}
        </ul>
      </div>
    </div>

    
    <footer style="margin-top: 60px; padding: 40px 0; border-top: 1px solid #eee; color: #95a5a6; font-size: 14px;">
      <p>Department of Aerospace Information Engineering, Beihang University</p>
      <p>© 2026 MIPVN Lab. All Rights Reserved.</p>
    </footer>

</div>