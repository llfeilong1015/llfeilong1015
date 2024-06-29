
import matplotlib.pyplot as plt
import matplotlib.patches as patches

fig, ax = plt.subplots()

# 绘制瓶盖主体
bottle_cap_body = patches.Rectangle((1, 1), 6, 6, linewidth=2, edgecolor='black', facecolor='none')
ax.add_patch(bottle_cap_body)

# 绘制气孔
hole = patches.Circle((4, 5.5), 0.5, linewidth=2, edgecolor='blue', facecolor='none')
ax.add_patch(hole)

# 绘制弹簧
spring = patches.Polygon([(3, 3), (3.5, 4), (4, 3), (4.5, 4), (5, 3)], closed=False, linewidth=2, edgecolor='green')
ax.add_patch(spring)

# 绘制阀门
valve = patches.Rectangle((3.5, 5), 1, 0.5, linewidth=2, edgecolor='red', facecolor='none')
ax.add_patch(valve)

# 绘制密封件
seal = patches.Rectangle((3.5, 2.5), 1, 0.2, linewidth=2, edgecolor='purple', facecolor='none')
ax.add_patch(seal)

# 绘制调整螺钉
adjustment_screw = patches.Rectangle((3.5, 1), 1, 0.5, linewidth=2, edgecolor='orange', facecolor='none')
ax.add_patch(adjustment_screw)

# 添加标签
plt.text(4.5, 7, '瓶盖主体', fontsize=12, verticalalignment='bottom', horizontalalignment='right')
plt.text(4.5, 5.5, '气孔和阀门', fontsize=12, verticalalignment='bottom', horizontalalignment='right')
plt.text(4.5, 4, '弹簧', fontsize=12, verticalalignment='bottom', horizontalalignment='right')
plt.text(4.5, 2.5, '密封件', fontsize=12, verticalalignment='bottom', horizontalalignment='right')
plt.text(4.5, 1, '调整螺钉', fontsize=12, verticalalignment='bottom', horizontalalignment='right')

plt.xlim(0, 8)
plt.ylim(0, 8)
plt.gca().set_aspect('equal', adjustable='box')
plt.axis('off')
plt.title('弹簧泄压瓶盖示意图')
plt.show()
