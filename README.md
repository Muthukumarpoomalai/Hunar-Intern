import pandas as 
df = pd.read_csv("food_coded.csv")


print("Initial Dataset Preview:")
print(df.head())
print("\nSummary Information:")

df = df.dropna()




df = df.drop_duplicates()


df.columns = df.columns.str.strip().str.lower().str.replace(' ', '_')  




df['category_column'] = df['category_column'].str.lower().str.strip()  

 df.drop(columns=['unnecessary_column'])  



df = pd.get_dummies(df, columns=['category_column'], drop_first=True)  


print("\nCleaned Dataset Preview:")
print(df.head())
print("\nCleaned Data Information:")
print(df.info())


print("\nCleaned data saved to 'food_coded_cleaned.csv'")# Hunar-Intern
