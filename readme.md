---
title: MineBlaze
style: |
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    
    body {
      background: linear-gradient(135deg, #6a11cb 0%, #2575fc 100%);
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      color: white;
      text-align: center;
      padding: 20px;
      position: relative;
      overflow-x: hidden;
    }
    
    body::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: 
        radial-gradient(circle at 20% 80%, rgba(157, 80, 255, 0.3) 0%, transparent 40%),
        radial-gradient(circle at 80% 20%, rgba(255, 119, 230, 0.3) 0%, transparent 40%),
        radial-gradient(circle at 40% 40%, rgba(106, 17, 203, 0.4) 0%, transparent 50%);
      z-index: -1;
      animation: pulse 8s ease-in-out infinite alternate;
    }
    
    @keyframes pulse {
      0% { opacity: 0.8; }
      100% { opacity: 1; }
    }
    
    .main-container {
      background: rgba(255, 255, 255, 0.1);
      backdrop-filter: blur(10px);
      border-radius: 30px;
      padding: 50px 70px;
      border: 1px solid rgba(255, 255, 255, 0.2);
      box-shadow: 
        0 20px 40px rgba(0, 0, 0, 0.2),
        inset 0 1px 0 rgba(255, 255, 255, 0.3);
      max-width: 800px;
      margin: 20px;
      position: relative;
      overflow: hidden;
      z-index: 1;
    }
    
    .main-container::after {
      content: '';
      position: absolute;
      top: -50%;
      left: -50%;
      width: 200%;
      height: 200%;
      background: linear-gradient(
        to bottom right,
        rgba(255, 255, 255, 0.1) 0%,
        rgba(255, 255, 255, 0) 30%
      );
      transform: rotate(30deg);
      z-index: -1;
    }
    
    .server-address {
      font-size: 4.5rem;
      font-weight: 800;
      margin-bottom: 40px;
      text-shadow: 
        0 5px 15px rgba(0, 0, 0, 0.3),
        0 0 30px rgba(157, 80, 255, 0.5);
      letter-spacing: 1px;
      background: linear-gradient(90deg, #ff9af5, #a855f7);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      animation: glow 3s ease-in-out infinite alternate;
    }
    
    @keyframes glow {
      0% { filter: drop-shadow(0 0 10px rgba(168, 85, 247, 0.7)); }
      100% { filter: drop-shadow(0 0 25px rgba(255, 154, 245, 0.9)); }
    }
    
    .separator {
      width: 80%;
      height: 2px;
      background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.5), transparent);
      margin: 50px auto;
    }
    
    .russian-section {
      margin-top: 40px;
      padding-top: 30px;
      border-top: 1px solid rgba(255, 255, 255, 0.2);
    }
    
    .russian-label {
      font-size: 1.5rem;
      margin-bottom: 15px;
      color: rgba(255, 255, 255, 0.9);
      font-weight: 300;
      letter-spacing: 1px;
    }
    
    .russian-address {
      font-size: 2.8rem;
      font-weight: 700;
      color: #ffccff;
      text-shadow: 0 3px 10px rgba(0, 0, 0, 0.3);
      background: linear-gradient(90deg, #e0b3ff, #ffb3ff);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
    }
    
    .subtitle {
      font-size: 1.2rem;
      margin-top: 15px;
      color: rgba(255, 255, 255, 0.7);
      font-weight: 300;
      max-width: 500px;
      line-height: 1.6;
    }
    
    .particles {
      position: absolute;
      width: 100%;
      height: 100%;
      top: 0;
      left: 0;
      z-index: -2;
    }
    
    .particle {
      position: absolute;
      background: rgba(255, 255, 255, 0.2);
      border-radius: 50%;
      animation: float 15s infinite linear;
    }
    
    @keyframes float {
      0% { transform: translateY(0) rotate(0deg); opacity: 0; }
      10% { opacity: 1; }
      90% { opacity: 1; }
      100% { transform: translateY(-100vh) rotate(360deg); opacity: 0; }
    }
    
    @media (max-width: 768px) {
      .server-address {
        font-size: 3rem;
      }
      
      .russian-address {
        font-size: 2rem;
      }
      
      .main-container {
        padding: 30px;
        margin: 15px;
      }
    }
    
    @media (max-width: 480px) {
      .server-address {
        font-size: 2.2rem;
      }
      
      .russian-address {
        font-size: 1.6rem;
      }
      
      .main-container {
        padding: 25px 20px;
      }
    }
  </style>
---

<div class="main-container">
  <h1 class="server-address">mc.mineblaze.net</h1>
  <p class="subtitle">Присоединяйтесь к нашему удивительному игровому сообществу</p>
  
  <div class="separator"></div>
  
  <div class="russian-section">
    <div class="russian-label">Для проживающих в РФ</div>
    <div class="russian-address">mc.mineblaze.ru</div>
    <p class="subtitle">Оптимизированное соединение для российских игроков</p>
  </div>
</div>

<div class="particles" id="particles"></div>

<script>
  // Создание частиц для фона
  document.addEventListener('DOMContentLoaded', function() {
    const particlesContainer = document.getElementById('particles');
    const particleCount = 30;
    
    for (let i = 0; i < particleCount; i++) {
      const particle = document.createElement('div');
      particle.classList.add('particle');
      
      // Случайные параметры
      const size = Math.random() * 15 + 5;
      const posX = Math.random() * 100;
      const delay = Math.random() * 15;
      const duration = Math.random() * 10 + 15;
      
      particle.style.width = `${size}px`;
      particle.style.height = `${size}px`;
      particle.style.left = `${posX}%`;
      particle.style.animationDelay = `${delay}s`;
      particle.style.animationDuration = `${duration}s`;
      
      // Пурпурные оттенки
      const purpleHue = Math.random() * 30 + 270;
      particle.style.background = `hsla(${purpleHue}, 80%, 70%, ${Math.random() * 0.3 + 0.1})`;
      
      particlesContainer.appendChild(particle);
    }
  });
</script>            </button>
        </div>
    </header>

    <!-- Боковое меню -->
    <aside class="sidebar" id="sidebar">
        <div class="sidebar-section">
            <a href="#" class="sidebar-item active" id="sidebarHome">
                <svg viewBox="0 0 24 24" width="24" height="24">
                    <path fill="currentColor" d="M10 20v-6h4v6h5v-8h3L12 3 2 12h3v8z"></path>
                </svg>
                <span>Главная</span>
            </a>
            <a href="#" class="sidebar-item" id="sidebarMyChannel">
                <svg viewBox="0 0 24 24" width="24" height="24">
                    <path fill="currentColor" d="M3 13h8V3H3v10zm0 8h8v-6H3v6zm10 0h8V11h-8v10zm0-18v6h8V3h-8z"></path>
                </svg>
                <span>Мой канал</span>
            </a>
            <a href="#" class="sidebar-item" id="sidebarShorts">
                <svg viewBox="0 0 24 24" width="24" height="24">
                    <path fill="currentColor" d="M10 18v-6l5 3-5 3zm7-15H7v1h10V3zm3 3H4v1h16V6zm2 3H2v12h20V9zM3 10h18v10H3V10z"></path>
                </svg>
                <span>Shorts</span>
            </a>
            <a href="#" class="sidebar-item" id="sidebarSubscriptions">
                <svg viewBox="0 0 24 24" width="24" height="24">
                    <path fill="currentColor" d="M10 18v-6l5 3-5 3zm7-15H7v1h10V3zm3 3H4v1h16V6zm2 3H2v12h20V9zM3 10h18v10H3V10z"></path>
                </svg>
                <span>Подписки</span>
            </a>
        </div>
        <hr class="sidebar-divider">
        <div class="sidebar-section">
            <a href="#" class="sidebar-item">
                <svg viewBox="0 0 24 24" width="24" height="24">
                    <path fill="currentColor" d="M11 7l6 3.5-6 3.5V7zm7 13H4V6H3v15h15v-1zm3-2H6V3h15v15zM7 4v13h13V4H7z"></path>
                </svg>
                <span>Библиотека</span>
            </a>
            <a href="#" class="sidebar-item">
                <svg viewBox="0 0 24 24" width="24" height="24">
                    <path fill="currentColor" d="M14.97 16.95L10 13.87V7h2v5.76l4.03 2.49-1.06 1.7zM12 3c-4.96 0-9 4.04-9 9s4.04 9 9 9 9-4.04 9-9-4.04-9-9-9m0-1c5.52 0 10 4.48 10 10s-4.48 10-10 10S2 17.52 2 12 6.48 2 12 2z"></path>
                </svg>
                <span>История</span>
            </a>
            <a href="#" class="sidebar-item" id="sidebarLiked">
                <svg viewBox="0 0 24 24" width="24" height="24">
                    <path fill="currentColor" d="M18.77,11h-4.23l1.52-4.94C16.38,5.03,15.54,4,14.38,4c-0.58,0-1.14,0.24-1.52,0.65L7,11H3v10h4h1h9.43 c1.06,0,1.98-0.67,2.19-1.61l1.34-6C21.23,12.15,20.18,11,18.77,11z M7,20H4v-8h3V20z M19.98,13.17l-1.34,6 C18.54,19.65,18.03,20,17.43,20H8v-8.61l5.6-6.06C13.79,5.12,14.08,5,14.38,5c0.26,0,0.5,0.11,0.63,0.3 c0.07,0.1,0.15,0.26,0.09,0.47l-1.52,4.94L13.18,12h1.35h4.23c0.41,0,0.8,0.17,1.03,0.46C19.92,12.61,20.05,12.86,19.98,13.17z"></path>
                </svg>
                <span>Понравившиеся</span>
            </a>
        </div>
        <hr class="sidebar-divider">
        <div class="sidebar-section">
            <h4 class="sidebar-title">Подписки</h4>
            <div id="subscriptionsList">
                <!-- Подписки будут добавляться динамически -->
            </div>
        </div>
    </aside>

    <!-- Основной контент -->
    <main class="main-content" id="mainContent">
        <!-- Главная страница -->
        <div id="homePage">
            <!-- Категории -->
            <div class="categories">
                <button class="category-btn active">Все</button>
                <button class="category-btn">Игры</button>
                <button class="category-btn">Музыка</button>
                <button class="category-btn">Новости</button>
                <button class="category-btn">Фильмы</button>
                <button class="category-btn">В прямом эфире</button>
                <button class="category-btn">Программирование</button>
                <button class="category-btn">Недавно добавленные</button>
            </div>

            <!-- Сетка видео -->
            <div class="videos-grid" id="videosGrid">
                <!-- Видео будут добавляться динамически -->
            </div>
        </div>

        <!-- Страница канала -->
        <div id="channelPage" class="channel-page hidden">
            <div class="channel-banner" id="channelBanner">
                <div class="channel-banner-gradient"></div>
            </div>
            <div class="channel-header">
                <div class="channel-avatar-large" id="channelAvatarLarge">
                    <img id="channelAvatarImg" src="" alt="" class="hidden" style="width: 100%; height: 100%; object-fit: cover; border-radius: 50%;">
                    <span id="channelAvatarText">G</span>
                </div>
                <div class="channel-info-header">
                    <h1 id="channelNameTitle">Название канала</h1>
                    <p class="channel-stats">
                        <span id="channelHandle">@channel</span> • 
                        <span id="channelSubscribers">0 подписчиков</span> • 
                        <span id="channelVideosCount">0 видео</span>
                    </p>
                    <p class="channel-description" id="channelDescription">Описание канала</p>
                </div>
                <button class="subscribe-btn" id="subscribeBtn">Подписаться</button>
                <button class="subscribe-btn hidden" id="editChannelBtn" style="background-color: var(--bg-hover); color: var(--text-primary);">Настроить вид канала</button>
            </div>
            <div class="channel-tabs">

                <button class="channel-tab active">Видео</button>
                <button class="channel-tab">О канале</button>
            </div>
            <div class="channel-videos videos-grid" id="channelVideos">
                <!-- Видео канала будут добавляться динамически -->
            </div>
        </div>

        <!-- Страница подписок -->
        <div id="subscriptionsPage" class="subscriptions-page hidden">
            <h2 class="page-title">Мои подписки</h2>
            <div class="subscriptions-grid" id="subscriptionsGrid">
                <!-- Подписки будут добавляться динамически -->
            </div>
            <div class="empty-state" id="emptySubscriptions">
                <svg viewBox="0 0 24 24" width="64" height="64">
                    <path fill="currentColor" d="M10 18v-6l5 3-5 3zm7-15H7v1h10V3zm3 3H4v1h16V6zm2 3H2v12h20V9zM3 10h18v10H3V10z"></path>
                </svg>
                <p>У вас пока нет подписок</p>
            </div>
        </div>

        <!-- Страница понравившихся видео -->
        <div id="likedPage" class="liked-page hidden">
            <h2 class="page-title">Понравившиеся видео</h2>
            <div class="videos-grid" id="likedVideosGrid">
                <!-- Понравившиеся видео будут добавляться динамически -->
            </div>
            <div class="empty-state" id="emptyLiked">
                <svg viewBox="0 0 24 24" width="64" height="64">
                    <path fill="currentColor" d="M18.77,11h-4.23l1.52-4.94C16.38,5.03,15.54,4,14.38,4c-0.58,0-1.14,0.24-1.52,0.65L7,11H3v10h4h1h9.43 c1.06,0,1.98-0.67,2.19-1.61l1.34-6C21.23,12.15,20.18,11,18.77,11z"></path>
                </svg>
                <p>У вас пока нет понравившихся видео</p>
            </div>
        </div>
    </main>

    <!-- Модальное окно видеоплеера -->
    <div class="video-modal" id="videoModal">
        <div class="modal-content">
            <button class="close-modal" id="closeModal">&times;</button>
            <video id="videoPlayer" controls>
                <source src="" type="video/mp4">
            </video>
            <div class="modal-info">
                <div class="modal-header">
                    <h2 id="modalTitle"></h2>
                    <p class="modal-meta" id="modalMeta">0 просмотров • Только что</p>
                </div>
                <div class="modal-channel">
                    <div class="channel-avatar modal-channel-avatar" id="modalChannelAvatar">G</div>
                    <div class="modal-channel-info">
                        <p class="modal-channel-name" id="modalChannelName">Канал</p>
                        <p class="modal-channel-subs" id="modalChannelSubs">0 подписчиков</p>
                    </div>
                    <button class="subscribe-btn modal-subscribe-btn" id="modalSubscribeBtn">Подписаться</button>
                </div>
                <div class="modal-actions">
                    <button class="action-btn" id="likeBtn">
                        <svg viewBox="0 0 24 24" width="24" height="24">
                            <path fill="currentColor" d="M18.77,11h-4.23l1.52-4.94C16.38,5.03,15.54,4,14.38,4c-0.58,0-1.14,0.24-1.52,0.65L7,11H3v10h4h1h9.43 c1.06,0,1.98-0.67,2.19-1.61l1.34-6C21.23,12.15,20.18,11,18.77,11z M7,20H4v-8h3V20z M19.98,13.17l-1.34,6 C18.54,19.65,18.03,20,17.43,20H8v-8.61l5.6-6.06C13.79,5.12,14.08,5,14.38,5c0.26,0,0.5,0.11,0.63,0.3 c0.07,0.1,0.15,0.26,0.09,0.47l-1.52,4.94L13.18,12h1.35h4.23c0.41,0,0.8,0.17,1.03,0.46C19.92,12.61,20.05,12.86,19.98,13.17z"></path>
                        </svg>
                        <span id="likeCount">0</span>
                    </button>
                    <button class="action-btn" id="dislikeBtn">
                        <svg viewBox="0 0 24 24" width="24" height="24">
                            <path fill="currentColor" d="M17,4h-1H6.57C5.5,4,4.59,4.67,4.38,5.61l-1.34,6C2.77,12.85,3.82,14,5.23,14h4.23l-1.52,4.94C7.62,19.97,8.46,21,9.62,21 c0.58,0,1.14-0.24,1.52-0.65L17,14h4V4H17z"></path>
                        </svg>
                        <span>Не нравится</span>
                    </button>
                    <button class="action-btn">
                        <svg viewBox="0 0 24 24" width="24" height="24">
                            <path fill="currentColor" d="M15 5.63 20.66 12 15 18.37V14h-1c-3.96 0-7.14 1-9.75 3.09 1.84-4.07 5.11-6.4 9.89-7.1l.86-.13V5.63M14 3v6C6.22 10.13 3.11 15.33 2 21c2.78-3.97 6.44-6 12-6v6l8-9-8-9z"></path>
                        </svg>
                        <span>Поделиться</span>
                    </button>
                </div>
            </div>
        </div>
    </div>

    <!-- Модальное окно загрузки видео -->
    <div class="upload-modal" id="uploadModal">
        <div class="upload-modal-content">
            <div class="upload-header">
                <h2>Загрузить видео</h2>
                <button class="close-modal" id="closeUploadModal">&times;</button>
            </div>
            <p style="padding: 0 24px; color: var(--text-secondary); font-size: 12px; margin-bottom: 10px;">
                ⚠️ Загруженные видео доступны только в текущей сессии браузера. После перезагрузки страницы они будут удалены.
            </p>
            <form id="uploadForm">
                <div class="upload-dropzone" id="uploadDropzone">
                    <svg viewBox="0 0 24 24" width="64" height="64">
                        <path fill="currentColor" d="M18 4l2 4h-3l-2-4h-2l2 4h-3l-2-4H8l2 4H7L5 4H4c-1.1 0-1.99.9-1.99 2L2 18c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V4h-4z"></path>
                    </svg>
                    <p>Перетащите видео сюда или нажмите для выбора</p>
                    <input type="file" id="videoFileInput" accept="video/*" hidden>
                </div>
                <div class="upload-preview hidden" id="uploadPreview">
                    <video id="previewVideo" controls></video>
                </div>
                <div class="upload-form-fields">
                    <div class="form-group">
                        <label for="videoTitleInput">Название</label>
                        <input type="text" id="videoTitleInput" placeholder="Введите название видео" required>
                    </div>
                    <div class="form-group">
                        <label for="videoDescInput">Описание</label>
                        <textarea id="videoDescInput" placeholder="Расскажите о вашем видео"></textarea>
                    </div>
                    <div class="form-group">
                        <label>Превью</label>
                        <div class="thumbnail-upload" id="thumbnailUpload">
                            <svg viewBox="0 0 24 24" width="32" height="32">
                                <path fill="currentColor" d="M21 19V5c0-1.1-.9-2-2-2H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2zM8.5 13.5l2.5 3.01L14.5 12l4.5 6H5l3.5-4.5z"></path>
                            </svg>
                            <p>Загрузить превью</p>
                            <input type="file" id="thumbnailInput" accept="image/*" hidden>
                        </div>
                        <div class="thumbnail-preview hidden" id="thumbnailPreview">
                            <img id="thumbnailImg" alt="Превью">
                        </div>
                    </div>
                    <div class="form-group">
                        <label for="channelSelect">Канал</label>
                        <select id="channelSelect">
                            <option value="myChannel" selected>Мой канал</option>
                            <option value="gaming">Gaming Channel</option>
                            <option value="tech">Tech Reviews</option>
                            <option value="retro">Retro Games</option>
                            <option value="apple">Apple News</option>
                            <option value="windows">Windows World</option>
                        </select>
                    </div>
                    <button type="submit" class="upload-submit-btn">Опубликовать</button>
                </div>
            </form>
        </div>
    </div>

    <!-- Модальное окно настройки канала -->
    <div class="upload-modal" id="editChannelModal">
        <div class="upload-modal-content">
            <div class="upload-header">
                <h2>Настройка канала</h2>
                <button class="close-modal" id="closeEditChannelModal">&times;</button>
            </div>
            <form id="editChannelForm">
                <div class="form-group">
                    <label>Аватар канала</label>
                    <div class="thumbnail-upload" id="avatarUpload">
                        <div class="avatar-preview-container">
                            <div class="channel-avatar-large" id="editChannelAvatarPreview" style="width: 100px; height: 100px; font-size: 40px; margin: 0 auto;">
                                <img id="editAvatarImg" src="" alt="" class="hidden" style="width: 100%; height: 100%; object-fit: cover; border-radius: 50%;">
                                <span id="editAvatarText">М</span>
                            </div>
                        </div>
                        <p style="margin-top: 10px; font-size: 14px; text-align: center;">Нажмите, чтобы изменить</p>
                        <input type="file" id="avatarInput" accept="image/*" hidden>
                    </div>
                </div>
                <div class="form-group">
                    <label>Шапка канала</label>
                    <div class="thumbnail-upload" id="bannerUpload" style="height: 100px;">
                         <img id="editBannerImg" src="" alt="" class="hidden" style="width: 100%; height: 100%; object-fit: cover;">
                         <div id="bannerPlaceholder">
                            <svg viewBox="0 0 24 24" width="32" height="32">
                                <path fill="currentColor" d="M21 19V5c0-1.1-.9-2-2-2H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2zM8.5 13.5l2.5 3.01L14.5 12l4.5 6H5l3.5-4.5z"></path>
                            </svg>
                            <p>Загрузить шапку</p>
                         </div>
                        <input type="file" id="bannerInput" accept="image/*" hidden>
                    </div>
                </div>
                <div class="upload-form-fields">
                    <div class="form-group">
                        <label for="channelNameInput">Название канала</label>
                        <input type="text" id="channelNameInput" placeholder="Введите название канала" required>
                    </div>
                    <div class="form-group">
                        <label for="channelHandleInput">Псевдоним (Handle)</label>
                        <input type="text" id="channelHandleInput" placeholder="@username" required>
                    </div>
                    <div class="form-group">
                        <label for="channelDescInput">Описание</label>
                        <textarea id="channelDescInput" placeholder="Расскажите аудитории о своем канале"></textarea>
                    </div>
                    <button type="submit" class="upload-submit-btn">Сохранить</button>
                </div>
            </form>
        </div>
    </div>

    <script src="script.js"></script>
</body>
</html>            <button class="icon-btn" id="uploadBtn" title="Загрузить видео">
                <svg viewBox="0 0 24 24" width="24" height="24">
                    <path fill="currentColor" d="M14 13h-3v3H9v-3H6v-2h3V8h2v3h3v2zm3-7H3v12h14v-6.39l4 1.83V8.56l-4 1.83V6m1-1v3.83L22 7v8l-4-1.83V19H2V5h16z"></path>
                </svg>
            </button>
            <button class="icon-btn">
                <svg viewBox="0 0 24 24" width="24" height="24">
                    <path fill="currentColor" d="M12 22c1.1 0 2-.9 2-2h-4c0 1.1.9 2 2 2zm6-6v-5c0-3.07-1.63-5.64-4.5-6.32V4c0-.83-.67-1.5-1.5-1.5s-1.5.67-1.5 1.5v.68C7.64 5.36 6 7.92 6 11v5l-2 2v1h16v-1l-2-2zm-2 1H8v-6c0-2.48 1.51-4.5 4-4.5s4 2.02 4 4.5v6z"></path>
                </svg>
            </button>
            <button class="avatar-btn" id="userAvatarBtn">
                <div class="avatar">U</div>
            </button>
        </div>
    </header>

    <!-- Боковое меню -->
    <aside class="sidebar" id="sidebar">
        <div class="sidebar-section">
            <a href="#" class="sidebar-item active" id="sidebarHome">
                <svg viewBox="0 0 24 24" width="24" height="24">
                    <path fill="currentColor" d="M10 20v-6h4v6h5v-8h3L12 3 2 12h3v8z"></path>
                </svg>
                <span>Главная</span>
            </a>
            <a href="#" class="sidebar-item" id="sidebarMyChannel">
                <svg viewBox="0 0 24 24" width="24" height="24">
                    <path fill="currentColor" d="M3 13h8V3H3v10zm0 8h8v-6H3v6zm10 0h8V11h-8v10zm0-18v6h8V3h-8z"></path>
                </svg>
                <span>Мой канал</span>
            </a>
            <a href="#" class="sidebar-item" id="sidebarShorts">
                <svg viewBox="0 0 24 24" width="24" height="24">
                    <path fill="currentColor" d="M10 18v-6l5 3-5 3zm7-15H7v1h10V3zm3 3H4v1h16V6zm2 3H2v12h20V9zM3 10h18v10H3V10z"></path>
                </svg>
                <span>Shorts</span>
            </a>
            <a href="#" class="sidebar-item" id="sidebarSubscriptions">
                <svg viewBox="0 0 24 24" width="24" height="24">
                    <path fill="currentColor" d="M10 18v-6l5 3-5 3zm7-15H7v1h10V3zm3 3H4v1h16V6zm2 3H2v12h20V9zM3 10h18v10H3V10z"></path>
                </svg>
                <span>Подписки</span>
            </a>
        </div>
        <hr class="sidebar-divider">
        <div class="sidebar-section">
            <a href="#" class="sidebar-item">
                <svg viewBox="0 0 24 24" width="24" height="24">
                    <path fill="currentColor" d="M11 7l6 3.5-6 3.5V7zm7 13H4V6H3v15h15v-1zm3-2H6V3h15v15zM7 4v13h13V4H7z"></path>
                </svg>
                <span>Библиотека</span>
            </a>
            <a href="#" class="sidebar-item">
                <svg viewBox="0 0 24 24" width="24" height="24">
                    <path fill="currentColor" d="M14.97 16.95L10 13.87V7h2v5.76l4.03 2.49-1.06 1.7zM12 3c-4.96 0-9 4.04-9 9s4.04 9 9 9 9-4.04 9-9-4.04-9-9-9m0-1c5.52 0 10 4.48 10 10s-4.48 10-10 10S2 17.52 2 12 6.48 2 12 2z"></path>
                </svg>
                <span>История</span>
            </a>
            <a href="#" class="sidebar-item" id="sidebarLiked">
                <svg viewBox="0 0 24 24" width="24" height="24">
                    <path fill="currentColor" d="M18.77,11h-4.23l1.52-4.94C16.38,5.03,15.54,4,14.38,4c-0.58,0-1.14,0.24-1.52,0.65L7,11H3v10h4h1h9.43 c1.06,0,1.98-0.67,2.19-1.61l1.34-6C21.23,12.15,20.18,11,18.77,11z M7,20H4v-8h3V20z M19.98,13.17l-1.34,6 C18.54,19.65,18.03,20,17.43,20H8v-8.61l5.6-6.06C13.79,5.12,14.08,5,14.38,5c0.26,0,0.5,0.11,0.63,0.3 c0.07,0.1,0.15,0.26,0.09,0.47l-1.52,4.94L13.18,12h1.35h4.23c0.41,0,0.8,0.17,1.03,0.46C19.92,12.61,20.05,12.86,19.98,13.17z"></path>
                </svg>
                <span>Понравившиеся</span>
            </a>
        </div>
        <hr class="sidebar-divider">
        <div class="sidebar-section">
            <h4 class="sidebar-title">Подписки</h4>
            <div id="subscriptionsList">
                <!-- Подписки будут добавляться динамически -->
            </div>
        </div>
    </aside>

    <!-- Основной контент -->
    <main class="main-content" id="mainContent">
        <!-- Главная страница -->
        <div id="homePage">
            <!-- Категории -->
            <div class="categories">
                <button class="category-btn active">Все</button>
                <button class="category-btn">Игры</button>
                <button class="category-btn">Музыка</button>
                <button class="category-btn">Новости</button>
                <button class="category-btn">Фильмы</button>
                <button class="category-btn">В прямом эфире</button>
                <button class="category-btn">Программирование</button>
                <button class="category-btn">Недавно добавленные</button>
            </div>

            <!-- Сетка видео -->
            <div class="videos-grid" id="videosGrid">
                <!-- Видео будут добавляться динамически -->
            </div>
        </div>

        <!-- Страница канала -->
        <div id="channelPage" class="channel-page hidden">
            <div class="channel-banner" id="channelBanner">
                <div class="channel-banner-gradient"></div>
            </div>
            <div class="channel-header">
                <div class="channel-avatar-large" id="channelAvatarLarge">
                    <img id="channelAvatarImg" src="" alt="" class="hidden" style="width: 100%; height: 100%; object-fit: cover; border-radius: 50%;">
                    <span id="channelAvatarText">G</span>
                </div>
                <div class="channel-info-header">
                    <h1 id="channelNameTitle">Название канала</h1>
                    <p class="channel-stats">
                        <span id="channelHandle">@channel</span> • 
                        <span id="channelSubscribers">0 подписчиков</span> • 
                        <span id="channelVideosCount">0 видео</span>
                    </p>
                    <p class="channel-description" id="channelDescription">Описание канала</p>
                </div>
                <button class="subscribe-btn" id="subscribeBtn">Подписаться</button>
                <button class="subscribe-btn hidden" id="editChannelBtn" style="background-color: var(--bg-hover); color: var(--text-primary);">Настроить вид канала</button>
            </div>
            <div class="channel-tabs">

                <button class="channel-tab active">Видео</button>
                <button class="channel-tab">О канале</button>
            </div>
            <div class="channel-videos videos-grid" id="channelVideos">
                <!-- Видео канала будут добавляться динамически -->
            </div>
        </div>

        <!-- Страница подписок -->
        <div id="subscriptionsPage" class="subscriptions-page hidden">
            <h2 class="page-title">Мои подписки</h2>
            <div class="subscriptions-grid" id="subscriptionsGrid">
                <!-- Подписки будут добавляться динамически -->
            </div>
            <div class="empty-state" id="emptySubscriptions">
                <svg viewBox="0 0 24 24" width="64" height="64">
                    <path fill="currentColor" d="M10 18v-6l5 3-5 3zm7-15H7v1h10V3zm3 3H4v1h16V6zm2 3H2v12h20V9zM3 10h18v10H3V10z"></path>
                </svg>
                <p>У вас пока нет подписок</p>
            </div>
        </div>

        <!-- Страница понравившихся видео -->
        <div id="likedPage" class="liked-page hidden">
            <h2 class="page-title">Понравившиеся видео</h2>
            <div class="videos-grid" id="likedVideosGrid">
                <!-- Понравившиеся видео будут добавляться динамически -->
            </div>
            <div class="empty-state" id="emptyLiked">
                <svg viewBox="0 0 24 24" width="64" height="64">
                    <path fill="currentColor" d="M18.77,11h-4.23l1.52-4.94C16.38,5.03,15.54,4,14.38,4c-0.58,0-1.14,0.24-1.52,0.65L7,11H3v10h4h1h9.43 c1.06,0,1.98-0.67,2.19-1.61l1.34-6C21.23,12.15,20.18,11,18.77,11z"></path>
                </svg>
                <p>У вас пока нет понравившихся видео</p>
            </div>
        </div>
    </main>

    <!-- Модальное окно видеоплеера -->
    <div class="video-modal" id="videoModal">
        <div class="modal-content">
            <button class="close-modal" id="closeModal">&times;</button>
            <video id="videoPlayer" controls>
                <source src="" type="video/mp4">
            </video>
            <div class="modal-info">
                <div class="modal-header">
                    <h2 id="modalTitle"></h2>
                    <p class="modal-meta" id="modalMeta">0 просмотров • Только что</p>
                </div>
                <div class="modal-channel">
                    <div class="channel-avatar modal-channel-avatar" id="modalChannelAvatar">G</div>
                    <div class="modal-channel-info">
                        <p class="modal-channel-name" id="modalChannelName">Канал</p>
                        <p class="modal-channel-subs" id="modalChannelSubs">0 подписчиков</p>
                    </div>
                    <button class="subscribe-btn modal-subscribe-btn" id="modalSubscribeBtn">Подписаться</button>
                </div>
                <div class="modal-actions">
                    <button class="action-btn" id="likeBtn">
                        <svg viewBox="0 0 24 24" width="24" height="24">
                            <path fill="currentColor" d="M18.77,11h-4.23l1.52-4.94C16.38,5.03,15.54,4,14.38,4c-0.58,0-1.14,0.24-1.52,0.65L7,11H3v10h4h1h9.43 c1.06,0,1.98-0.67,2.19-1.61l1.34-6C21.23,12.15,20.18,11,18.77,11z M7,20H4v-8h3V20z M19.98,13.17l-1.34,6 C18.54,19.65,18.03,20,17.43,20H8v-8.61l5.6-6.06C13.79,5.12,14.08,5,14.38,5c0.26,0,0.5,0.11,0.63,0.3 c0.07,0.1,0.15,0.26,0.09,0.47l-1.52,4.94L13.18,12h1.35h4.23c0.41,0,0.8,0.17,1.03,0.46C19.92,12.61,20.05,12.86,19.98,13.17z"></path>
                        </svg>
                        <span id="likeCount">0</span>
                    </button>
                    <button class="action-btn" id="dislikeBtn">
                        <svg viewBox="0 0 24 24" width="24" height="24">
                            <path fill="currentColor" d="M17,4h-1H6.57C5.5,4,4.59,4.67,4.38,5.61l-1.34,6C2.77,12.85,3.82,14,5.23,14h4.23l-1.52,4.94C7.62,19.97,8.46,21,9.62,21 c0.58,0,1.14-0.24,1.52-0.65L17,14h4V4H17z"></path>
                        </svg>
                        <span>Не нравится</span>
                    </button>
                    <button class="action-btn">
                        <svg viewBox="0 0 24 24" width="24" height="24">
                            <path fill="currentColor" d="M15 5.63 20.66 12 15 18.37V14h-1c-3.96 0-7.14 1-9.75 3.09 1.84-4.07 5.11-6.4 9.89-7.1l.86-.13V5.63M14 3v6C6.22 10.13 3.11 15.33 2 21c2.78-3.97 6.44-6 12-6v6l8-9-8-9z"></path>
                        </svg>
                        <span>Поделиться</span>
                    </button>
                </div>
            </div>
        </div>
    </div>

    <!-- Модальное окно загрузки видео -->
    <div class="upload-modal" id="uploadModal">
        <div class="upload-modal-content">
            <div class="upload-header">
                <h2>Загрузить видео</h2>
                <button class="close-modal" id="closeUploadModal">&times;</button>
            </div>
            <p style="padding: 0 24px; color: var(--text-secondary); font-size: 12px; margin-bottom: 10px;">
                ⚠️ Загруженные видео доступны только в текущей сессии браузера. После перезагрузки страницы они будут удалены.
            </p>
            <form id="uploadForm">
                <div class="upload-dropzone" id="uploadDropzone">
                    <svg viewBox="0 0 24 24" width="64" height="64">
                        <path fill="currentColor" d="M18 4l2 4h-3l-2-4h-2l2 4h-3l-2-4H8l2 4H7L5 4H4c-1.1 0-1.99.9-1.99 2L2 18c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V4h-4z"></path>
                    </svg>
                    <p>Перетащите видео сюда или нажмите для выбора</p>
                    <input type="file" id="videoFileInput" accept="video/*" hidden>
                </div>
                <div class="upload-preview hidden" id="uploadPreview">
                    <video id="previewVideo" controls></video>
                </div>
                <div class="upload-form-fields">
                    <div class="form-group">
                        <label for="videoTitleInput">Название</label>
                        <input type="text" id="videoTitleInput" placeholder="Введите название видео" required>
                    </div>
                    <div class="form-group">
                        <label for="videoDescInput">Описание</label>
                        <textarea id="videoDescInput" placeholder="Расскажите о вашем видео"></textarea>
                    </div>
                    <div class="form-group">
                        <label>Превью</label>
                        <div class="thumbnail-upload" id="thumbnailUpload">
                            <svg viewBox="0 0 24 24" width="32" height="32">
                                <path fill="currentColor" d="M21 19V5c0-1.1-.9-2-2-2H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2zM8.5 13.5l2.5 3.01L14.5 12l4.5 6H5l3.5-4.5z"></path>
                            </svg>
                            <p>Загрузить превью</p>
                            <input type="file" id="thumbnailInput" accept="image/*" hidden>
                        </div>
                        <div class="thumbnail-preview hidden" id="thumbnailPreview">
                            <img id="thumbnailImg" alt="Превью">
                        </div>
                    </div>
                    <div class="form-group">
                        <label for="channelSelect">Канал</label>
                        <select id="channelSelect">
                            <option value="myChannel" selected>Мой канал</option>
                            <option value="gaming">Gaming Channel</option>
                            <option value="tech">Tech Reviews</option>
                            <option value="retro">Retro Games</option>
                            <option value="apple">Apple News</option>
                            <option value="windows">Windows World</option>
                        </select>
                    </div>
                    <button type="submit" class="upload-submit-btn">Опубликовать</button>
                </div>
            </form>
        </div>
    </div>

    <!-- Модальное окно настройки канала -->
    <div class="upload-modal" id="editChannelModal">
        <div class="upload-modal-content">
            <div class="upload-header">
                <h2>Настройка канала</h2>
                <button class="close-modal" id="closeEditChannelModal">&times;</button>
            </div>
            <form id="editChannelForm">
                <div class="form-group">
                    <label>Аватар канала</label>
                    <div class="thumbnail-upload" id="avatarUpload">
                        <div class="avatar-preview-container">
                            <div class="channel-avatar-large" id="editChannelAvatarPreview" style="width: 100px; height: 100px; font-size: 40px; margin: 0 auto;">
                                <img id="editAvatarImg" src="" alt="" class="hidden" style="width: 100%; height: 100%; object-fit: cover; border-radius: 50%;">
                                <span id="editAvatarText">М</span>
                            </div>
                        </div>
                        <p style="margin-top: 10px; font-size: 14px; text-align: center;">Нажмите, чтобы изменить</p>
                        <input type="file" id="avatarInput" accept="image/*" hidden>
                    </div>
                </div>
                <div class="form-group">
                    <label>Шапка канала</label>
                    <div class="thumbnail-upload" id="bannerUpload" style="height: 100px;">
                         <img id="editBannerImg" src="" alt="" class="hidden" style="width: 100%; height: 100%; object-fit: cover;">
                         <div id="bannerPlaceholder">
                            <svg viewBox="0 0 24 24" width="32" height="32">
                                <path fill="currentColor" d="M21 19V5c0-1.1-.9-2-2-2H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2zM8.5 13.5l2.5 3.01L14.5 12l4.5 6H5l3.5-4.5z"></path>
                            </svg>
                            <p>Загрузить шапку</p>
                         </div>
                        <input type="file" id="bannerInput" accept="image/*" hidden>
                    </div>
                </div>
                <div class="upload-form-fields">
                    <div class="form-group">
                        <label for="channelNameInput">Название канала</label>
                        <input type="text" id="channelNameInput" placeholder="Введите название канала" required>
                    </div>
                    <div class="form-group">
                        <label for="channelHandleInput">Псевдоним (Handle)</label>
                        <input type="text" id="channelHandleInput" placeholder="@username" required>
                    </div>
                    <div class="form-group">
                        <label for="channelDescInput">Описание</label>
                        <textarea id="channelDescInput" placeholder="Расскажите аудитории о своем канале"></textarea>
                    </div>
                    <button type="submit" class="upload-submit-btn">Сохранить</button>
                </div>
            </form>
        </div>
    </div>

    <script src="script.js"></script>
</body>
</html>
