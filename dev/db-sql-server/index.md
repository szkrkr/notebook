#

## クエリ集
```sql
-- ユーザー追加用のクエリ
CREATE USER <Azure_AD_principal_name> FROM EXTERNAL PROVIDER;

-- ロール割り当てクエリ
ALTER ROLE <role_name> ADD MEMBER <database_principal>;

-- ロール割り当て確認用クエリ
SELECT DP1.name AS DatabaseRoleName, isnull (DP2.name, 'No members') AS DatabaseUserName 
FROM sys.database_role_members AS DRM 
  RIGHT OUTER JOIN sys.database_principals AS DP1 
  ON DRM.role_principal_id = DP1.principal_id
    LEFT OUTER JOIN sys.database_principals AS DP2 
    ON DRM.member_principal_id = DP2.principal_id
    WHERE DP1.type = 'R' 
    ORDER BY DP1.name;
```

権限周りのURL
https://docs.microsoft.com/ja-jp/sql/relational-databases/security/authentication-access/database-level-roles?view=sql-server-ver15#fixed-database-roles