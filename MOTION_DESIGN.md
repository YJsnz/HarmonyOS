# 示意图四处角色动效

使用内置 image_gen 工具，以用户提供的四角色横条示意图为人物参照，分别生成透明 PNG。保留各自发型、服装与半身构图；固定图层预加载，以连续属性动画播放。

## 生成提示词摘要

共同要求：Use the attached narrow illustration strip as the ONLY visual reference. Faithfully reconstruct ONE of its four original cartoon characters as a crisp transparent PNG app asset. Match the exact reference face, hairstyle, costume, proportions, soft shaded glossy children's-book rendering and colors. Keep the upper-body/bust framing as in the reference. No UI, phones, landscape, grass, labels, arrows, text, watermark or backdrop. Preserve true transparency with generous padding.

- motion_reading_boy.png：Far-left reading boy, fluffy curly black hair, green long sleeves, holding an open blue picture book, excited expression.
- motion_reward_boy.png：Second reward boy, short chestnut swept hair, blue shirt, green lower clothing, closed smiling eyes, hugging one large yellow five-point star.
- motion_thinking_child.png：Third thinking girl, dark side pigtails with yellow ties, yellow shirt and purple dungarees, finger to cheek, tilted head, yellow question mark.
- motion_happy_child.png：Far-right happy girl, chestnut hair with yellow tie, green top and yellow skirt, eyes closed joyfully, both arms up, jumping.

## 播放与触发

- 绘本馆：绿衣读书男孩和卡片错峰入场，单次约 480ms。
- 共读奖励：蓝衣抱星男孩分四段轻弹，单次约 630ms。
- AI 等待：黄紫衣女孩歪头，左右回正约 940ms，随后显示回答。
- RFID 配对成功：绿衣黄裙女孩上升、落地、回弹，单次约 780ms。
- 页面切换：130ms 淡出，240ms 淡入与轻位移；快速导航使用代次标识取消过期回调。
- 开启减少动态效果时呈现静态角色；各动作播放一次后静止，等待下一次交互。

