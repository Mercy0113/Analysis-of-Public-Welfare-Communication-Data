import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# 读取脱敏数据集
def load_data(file_path):
    """加载 Excel 数据"""
    return pd.read_excel(file_path)

# 数据预处理
def preprocess_data(df):
    """清理并转换数据"""
    df = df.dropna()  # 删除空值
    df['日期'] = pd.to_datetime(df['日期'])  # 转换日期格式
    return df

# 数据可视化
def visualize_data(df):
    """绘制传播趋势"""
    plt.figure(figsize=(10, 5))
    sns.lineplot(data=df, x='日期', y='传播量', marker='o')
    plt.title('贵州村超话题传播趋势')
    plt.xlabel('日期')
    plt.ylabel('传播量')
    plt.grid()
    plt.show()

if __name__ == "__main__":
    file_path = "data/guizhou_village_super.xlsx"  # 你的数据文件路径
    df = load_data(file_path)
    df = preprocess_data(df)
    visualize_data(df)
