# Case Study Documentation


# Pre-processing Function Updates ("Complete - User path.ipynb")

Here is a list of new functions (modules) added to the pre-processing pipeline for DBDP

1. Standardization

# standardize(df, col_names)

Params: df (dataframe containing the data), col_names (selected columns to be transformed)
Output: dataframe with scaled, transformed columns

Description: Standardizing features/data by removing the mean and scaling to unit variance.
https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.StandardScaler.html



2. Normalization

# normalize(df, col_names)

Params: df (dataframe containing the data), col_names (selected columns to be transformed)
Output: dataframe with normalized, transformed columns

Description: Scale input vectors individually to unit norm (vector length).
https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.normalize.html

3. One Hot Encoding

# oneHotEncode(df, category_List)

Params: df (dataframe containing the data), category_list (categories expected for the dataframe)
Output: one-hot numeric array

Note: if category_list is empty, then the function will automatically derive the categories based on the unique values of each "feature".

Description: Encode categorical features as a one-hot numeric array. The input to this transformer should be an array-like of integers or strings, denoting the values taken on by categorical (discrete) features. The features are encoded using a one-hot (aka ‘one-of-K’ or ‘dummy’) encoding scheme. This creates a binary column for each category and returns a sparse matrix or dense array (depending on the sparse parameter).
https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.OneHotEncoder.html

4. MinMax Scaling

# minMaxScaler(df, column_names)

Params: df (dataframe containing the data), col_names (selected columns to be transformed)
Output: dataframe with scaled, transformed columns

Description: Transform features by scaling each feature to a given range. This estimator scales and translates each feature individually such that it is in the given range on the training set, e.g. between zero and one.
https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.MinMaxScaler.html

5. Standard Scaling

# StandardScaler(df, column_names)

Params: df (dataframe containing the data), col_names (selected columns to be transformed)
Output: dataframe with scaled, transformed columns

Description: Scale each feature by its maximum absolute value. This function scales and translates each feature individually such that the maximal absolute value of each feature in the training set will be 1.0. It does not shift/center the data, and thus does not destroy any sparsity.
https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.MaxAbsScaler.html

6. Data type conversions

Params:
Output: