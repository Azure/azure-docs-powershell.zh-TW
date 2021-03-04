---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/get-azpostgresqlconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConnectionString.md
ms.openlocfilehash: ae0a5f2130ea4b5120fdbe78ab4cc23a7eba29a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913365"
---
# Get-AzPostgreSqlConnectionString

## 簡介
根據用戶端連接提供者取得連接字串。

## 語法

### 取得 (預設) 
```
Get-AzPostgreSqlConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzPostgreSqlConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## 描述
根據用戶端連接提供者取得連接字串。

## 例子

### 範例 1：根據資源群組和伺服器名稱取得 PostgreSql 伺服器連接字串
```powershell
PS C:\> Get-AzPostgreSqlConnectionString -Client ADO.NET -Name PostgreSqlTestServer -ResourceGroupName PostgreSqlTestRG

Server=postgresqltestserver.postgres.database.azure.com;Database={your_database};Port=5432;User Id=pwsh@postgresqltestserver;Password={your_password};Ssl Mode=Require;
```

此 Cmdlet 會根據資源群組和伺服器名稱，獲得 PostgreSql 伺服器連接字串。

### 範例 2：根據身分識別取得 PostgreSql 伺服器連接字串
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | Get-AzPostgreSqlConnectionString -Client PHP

host=postgresqltestserver.postgres.database.azure.com port=5432 dbname={your_database} user=pwsh@postgresqltestserver password={your_password} sslmode=require
```

此 Cmdlet 會以身分識別方式獲得 PostgreSql 伺服器連接字串。

## 參數

### -用戶端
用戶端連接提供者。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
連接字串的伺服器若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -名稱
伺服器名稱。

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
包含資源的資源組名，您可從 Azure Resource Manager API 或入口網站取得此值。

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
可識別 Azure 訂閱的訂閱識別碼。

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer

## 輸出

### System.String

## 筆記

別名

複雜的參數屬性

若要建立下列描述的參數，請建構包含適當屬性的雜湊表。 有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。


INPUTOBJECT： <IServer> 連接字串的伺服器
  - `Location <String>`：資源所在地的地理位置
  - `[Tag <ITrackedResourceTags>]`：資源標記。
    - `[(Any) <String>]`：這表示任何屬性都可以新增到這個物件。
  - `[AdministratorLogin <String>]`：系統管理員的伺服器登入名稱。 只能在建立伺服器時指定， (建立時) 。
  - `[EarliestRestoreDate <DateTime?>]`：ISO8601 格式的最早還原點建立時間 (ISO8601 格式) 
  - `[FullyQualifiedDomainName <String>]`：伺服器完整功能變數名稱。
  - `[IdentityType <IdentityType?>]`：身分識別類型。 將此選項設定為 'SystemAssigned'，以自動建立及指派資源的 Azure Active Directory 主體。
  - `[InfrastructureEncryption <InfrastructureEncryption?>]`：狀態顯示伺服器是否啟用基礎結構加密。
  - `[MasterServerId <String>]`：複本伺服器的主伺服器識別碼。
  - `[MinimalTlsVersion <MinimalTlsVersionEnum?>]`：針對伺服器強制執行最小 Tls 版本。
  - `[PublicNetworkAccess <PublicNetworkAccessEnum?>]`：此伺服器是否允許公用網路存取。 Value 為選擇性，但如果傳遞，則必須是 'Enabled' 或 'Disabled'
  - `[ReplicaCapacity <Int32?>]`：主伺服器可擁有的最大複本數目。
  - `[ReplicationRole <String>]`：伺服器的複製角色。
  - `[SkuCapacity <Int32?>]`：向上/縮小容量，代表伺服器的計算單位。
  - `[SkuFamily <String>]`：硬體系列。
  - `[SkuName <String>]`：SKU 的名稱，通常是 tier + family + cores，例如B_Gen4_1、GP_Gen5_8。
  - `[SkuSize <String>]`：大小代碼，以適當的資源解譯。
  - `[SkuTier <SkuTier?>]`：特定 SKU 的層級，例如基本。
  - `[SslEnforcement <SslEnforcementEnum?>]`：在連接至伺服器時啟用 ssl 強制執行或不啟用。
  - `[StorageProfileBackupRetentionDay <Int32?>]`：伺服器的備份保留天數。
  - `[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`：針對伺服器備份啟用異地重複或不啟用。
  - `[StorageProfileStorageAutogrow <StorageAutogrow?>]`：啟用儲存空間自動放大。
  - `[StorageProfileStorageMb <Int32?>]`：伺服器允許的最大儲存空間。
  - `[UserVisibleState <ServerState?>]`：使用者可看見的伺服器狀態。
  - `[Version <ServerVersion?>]`：伺服器版本。

## 相關連結

