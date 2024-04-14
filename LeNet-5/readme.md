这个LeNet5模型主要使用torch在本地部署。

在train文件和Test文件中，只要改变一下数据集，就可以实现不同数据集的训练。如果想自己训练模型，可以加载自己的数据集再转换为tensor格式
# 加载训练数据集
train_dataset = datasets.MNIST(root='./data', train=True, transform=data_transform, download=True)
train_dataloader = torch.utils.data.DataLoader(dataset=train_dataset, batch_size=16, shuffle=True)
# 加载测试数据集
test_dataset = datasets.MNIST(root='./data', train=False, transform=data_transform, download=True)
test_dataloader = torch.utils.data.DataLoader(dataset=test_dataset, batch_size=16, shuffle=True)


训练得到的模型权重：
------------------
train_loss0.036882649901894424
train_acc0.98835
val_losse. 03949112932882272
val_acco.9877
save best model
epoch50

最终结果：
predicted: "7", actual:"7"
predicted: "2", actual:"2"
predicted: "1", actual:"1"
predicted: "0", actual:"0"
predicted: "4", actual:"4"
predicted: "1", actual:"1"
predicted: "4", actual:"4"
predicted: "9", actual:"9"
predicted: "5", actual:"5"
predicted: "9", actual:"9"
