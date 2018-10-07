# Install Panda

Type the follwing in CMD Line if you need to upgrade 
C:\Users\shijian.he>pip3 install --upgrade pip
pip3 install jupyter

pip install pandas

pip3 install matplotlib


import numpy as np
import pandas as pd
data =pd.read_csv('shijian.csv')
data.iloc[0:10,:]

import numpy as np
import pandas as pd
data =pd.read_csv('shijian.csv')
data.iloc[5,:]
---------------------------
import numpy as np
import pandas as pd
data =pd.read_csv('shijian.csv')
data.loc[0:10,:]
data.index

import numpy as np
import pandas as pd
data =pd.read_csv('shijian.csv')
data.loc[0:10,["EMPLOYEE_NAME","team_name"]]
data["number_of_days"].mean() ## average on column
data["number_of_days"].mean(axis=1) ## average on row

#DataFrame
frame = pd.DataFrame(
    [
        [1,2],
        ["Boris Yeltsin", "Mikhail Gorbachev"]
    ],
    index=["row1", "row2"],
    columns=["column1", "column2"]
)
frame

frame = pd.DataFrame(
    {
        "column1": [1, "Boris Yeltsin"],
        "column2": [2, "Mikhail Gorbachev"]
    }
)
frame

#Filter
import numpy as np
import pandas as pd
data =pd.read_csv('shijian.csv')
score_filter = data["number_of_days"] > 6.3
filtered_reviews = data[score_filter]
filtered_reviews.loc[:,:]
