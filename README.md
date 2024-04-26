## GIT
''' bash
git init
git add .
git commit -m "msg"
git branch -M main
git remote add origin <ssh or http link>
git push

git status
'''

## DVC
''' bash
dvc init
dvc add ./data/ ./models/
dvc remote add --default myremote gdrive://1VxqCt_9VOetUUna_R_Ub0JEPSGTWFu9V
dvc push

dvc status
'''

## MLFLOW MODEL

'''
mlflow models server -m "file:///D:/my%20github/MLOP-Agoor/mlflow%20model/src/mlruns/317579281513027371/e9509ed08797416a86028d121b588c19/artifacts/RandomForestClassifier/with-SMOT" --port 8000 --env-manager-local

# exmaple of data to be sent
{
    "dataframe_split": {
        "columns": [
            "Age", 
            "CreditScore", 
            "Balance", 
            "EstimatedSalary", 
            "Gender_Male", 
            "Geography_Germany", 
            "Geography_Spain", 
            "HasCrCard", 
            "Tenure", 
            "IsActiveMember", 
            "NumOfProducts"
        ],
        "data": [
            [-0.7541830079917924, 
            0.5780143566720919, 
            0.11375998165198585, 
            -0.14673040749854463, 
            0.0, 
            0.0, 
            0.0, 
            0.0, 
            2.0, 
            0.0, 
            2.0]
        ]
    }
}


## multiple samples
{
    "dataframe_split": {
        "columns": [
            "Age",
            "CreditScore",
            "Balance",
            "EstimatedSalary",
            "Gender_Male",
            "Geography_Germany",
            "Geography_Spain",
            "HasCrCard",
            "Tenure",
            "IsActiveMember",
            "NumOfProducts"
        ],
        "data": [
            [-0.7541830079917924, 0.5780143566720919, 0.11375998165198585, -0.14673040749854463, 0.0, 0.0, 0.0, 0.0, 2.0, 0.0, 2.0],
            [-0.5605884106597949, 0.753908347743766, 0.7003528882054108, 1.6923927520037099, 0.0, 1.0, 0.0, 1.0, 9.0, 1.0, 1.0],
            [0.11699268000219652, -0.3221490094005933, 0.5222180917013974, -0.8721429873346316, 1.0, 1.0, 0.0, 1.0, 5.0, 0.0, 2.0],
            [0.6977764719981892, -0.7256705183297281, -1.2170740485175422, 0.07677206232885857, 0.0, 0.0, 1.0, 1.0, 1.0, 0.0, 2.0]
        ]
    }
}
'''

''' bash
mlflow server --host 0.0.0.0 --port 5050 --backend-store-url mysql://root:ammar@localhost:3306/mlflow_logs --default-artifact-root ./mlruns

'''

