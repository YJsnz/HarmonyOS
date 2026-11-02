# 运行时美术资源

本文只记录当前 HarmonyOS 项目实际使用的资源。页面在 ArkUI 中绘制文字和交互控件，插画以独立图像资源打包。

## 首页与角色

- `home_wave_body.png`、`home_wave_arm.png`：首页女孩身体与手臂的透明分层图。两层常驻，不切换帧；手臂围绕肩部以原生旋转完成约 2.34 秒挥手，之后待机约 10 秒。
- `home_garden.svg`、`home_reading_banner.jpg`、`home_recommend.svg`、`home_books.svg`、`home_checkin.svg`、`home_chat.svg`：首页场景装饰、共读横幅与快捷入口。
- `motion_reward_girl.png`、`motion_think_girl.png`、`motion_jump_girl.png`：按主页女孩造型重新生成的透明动作插画，分别用于奖励抱星、思考歪头、完成跳跃。使用预加载的固定图层配合 ArkUI 原生位移、缩放、旋转与淡入淡出，不逐帧替换图片，避免闪帧。
- 首页挥手继续使用 `home_wave_body.png`、`home_wave_arm.png` 两层骨骼式原生旋转；绘本卡片采用错峰淡入和轻微上移。页面之间统一使用短暂淡出、轻移位、淡入过渡，并尊重“减少动态效果”设置。
- `girl_wave_00..07.png`、`girl_reading_00..07.png`、`girl_think_00..07.png`、`girl_celebrate_00..07.png`：早期动作序列资源，当前页面不再引用。

## 五个面板

- `page_library.jpg`、`page_covers_forest.jpg`、`page_covers_moon.jpg`、`page_covers_seed.jpg`、`page_themes_spring.jpg`、`page_themes_feelings.jpg`、`page_themes_nature.jpg`：绘本馆场景、封面和主题卡片。
- `page_boy.png`、`page_reader.png`：阅读成长和设备中心插画。
- `page_sky.jpg`：AI 共读的回答配图。
- `page_radar.svg`：阅读能力图示底图。
- `page_content.svg`、`page_focus.svg`、`page_settings.svg`、`icon_battery.svg`、`icon_voice.svg`：设备功能和状态图标。
- `nav_home.svg`、`nav_book.svg`、`nav_growth.svg`、`nav_ai.svg`、`nav_device.svg`：底部导航图标。
- `AppScope/resources/base/media/app_icon.svg`：应用图标。

## 字体

应用将 Resource Han Rounded CN v0.990 的 Regular、Bold、Heavy 字重注册为 `TongyueRoundedRegular`、`TongyueRoundedBold`、`TongyueRoundedHeavy`。字体文件和 SIL Open Font License 1.1 随应用放在 `entry/src/main/resources/rawfile/fonts/`。

上游字体项目与许可证：<https://github.com/CyanoHao/Resource-Han-Rounded/releases/tag/v0.990>
