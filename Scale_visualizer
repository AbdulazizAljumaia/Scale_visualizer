import pandas as pd
import numpy as np
#import os
#import pandas as pd
#import matplotlib
#import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
from bidi.algorithm import get_display
import matplotlib.pyplot as plt
import arabic_reshaper



data = pd.read_excel("survay.xlsx")
data = data.sort_values(by=["sex"]).reset_index()
data = [data.loc[i] for i in range(len( data ) ) if data["sex"][i] == "ذكر"]
Data = pd.DataFrame(data)
Data[Data.columns[4:]]


def Evaluation(X):
    fig = plt.figure(figsize=(10,6))
    x = np.array(Data[Data.columns[4:]])[X]
    sns.set()
    reshaped_text = arabic_reshaper.reshape(Data[Data.columns[4:]].columns[X])
    artext = get_display(reshaped_text)
    plt.title(str(artext))
    #plt.suptitle("Medical stream")
    sns.set_context("paper")

    sns.distplot(x);
    #plt.legend(labels= Data[Data.columns[4:]].columns[X])
    plt.show()

for i in range(25):
    Evaluation(i)
