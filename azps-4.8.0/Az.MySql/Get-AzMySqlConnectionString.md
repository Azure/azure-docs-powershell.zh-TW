---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConnectionString.md
ms.openlocfilehash: ab2e820ec0e1c943cfeb5f8b3d83babece38ed95
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129423"
---
# Get-AzMySqlConnectionString

## 摘要
根據用戶端連線提供者取得連接字串。

## 句法

### 取得 (預設) 
```
Get-AzMySqlConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzMySqlConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## 說明
根據用戶端連線提供者取得連接字串。

## 示例

### 範例1：透過資源群組和伺服器名稱取得 MySql 伺服器連線字串
```powershell
PS C:\> Get-AzMySqlConnectionString -Client ADO.NET -Name mysql-test -ResourceGroupName PowershellMySqlTest

Server=mysql-test.mysql.database.azure.com; Port=3306; Database={your_database}; Uid=mysql_test@mysql-test; Pwd={your_password};
```

這個 Cmdlet 透過資源群組和伺服器名稱取得 MySql server 連線字串。

### 範例2：透過身分識別取得 MySql server 連線字串
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Get-AzMySqlConnectionString -Client PHP

$con=mysqli_init(); mysqli_real_connect($con, "mysql-test.mysql.database.azure.com", "mysql_test@mysql-test", {your_password}, {your_database}, 3306);
```

這個 Cmdlet 透過身分識別來取得 MySql server 連線字串。

## 參數

### -用戶端
用戶端連線提供者。

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
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

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
要從中建立複本的來源伺服器物件。
若要構造，請參閱適用于 INPUTOBJECT 屬性的 [記事] 區段，並建立雜湊表。

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -名稱
伺服器的名稱。

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
包含資源之資源群組的名稱，您可以從 Azure 資源管理員 API 或入口網站取得此值。

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
識別 Azure 訂閱的訂閱 ID。

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### IServer 中的 Api20171201 （）。

## 輸出

### System.object

## 筆記

別名

複雜的參數屬性

若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。 如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。


INPUTOBJECT <IServer> ：要從中建立複本的來源伺服器物件。
  - `Location <String>`：資源所在的位置。
  - `[Tag <ITrackedResourceTags>]`：以鍵值對形式的特定應用程式中繼資料。
    - `[(Any) <String>]`：這表示您可以將任何屬性新增至此物件。
  - `[AdministratorLogin <String>]`：管理員的伺服器登入名稱。 只能在 (建立伺服器時指定，且在建立) 時需要。
  - `[EarliestRestoreDate <DateTime?>]`： (ISO8601 格式的最早還原點建立時間) 
  - `[FullyQualifiedDomainName <String>]`：伺服器的完整功能變數名稱。
  - `[IdentityType <IdentityType?>]`：身分識別類型。 將此值設定為 ' SystemAssigned」，即可自動為資源建立並指派 Azure Active Directory 主體。
  - `[InfrastructureEncryption <InfrastructureEncryption?>]`：顯示伺服器是否已啟用基礎結構加密的狀態。
  - `[MasterServerId <String>]`：複本伺服器的主伺服器 id。
  - `[MinimalTlsVersion <MinimalTlsVersionEnum?>]`：為伺服器強制執行最低的 Tls 版本。
  - `[PublicNetworkAccess <PublicNetworkAccessEnum?>]`：此伺服器是否允許公用網路存取。 Value 是 optional，但如果傳入，就必須是「Enabled」或「Disabled」
  - `[ReplicaCapacity <Int32?>]`：主伺服器可擁有的複本數目上限。
  - `[ReplicationRole <String>]`：伺服器的複製角色。
  - `[SkuCapacity <Int32?>]`： [擴大/縮小] 容量，代表伺服器的計算單位。
  - `[SkuFamily <String>]`：硬體系列。
  - `[SkuName <String>]`： Sku 的名稱，通常是 [層 + 家庭 + 核心]，例如 B_Gen4_1、GP_Gen5_8。
  - `[SkuSize <String>]`：根據需要由資源來轉譯的大小代碼。
  - `[SkuTier <SkuTier?>]`：特定 SKU 的層級，例如基本。
  - `[SslEnforcement <SslEnforcementEnum?>]`[：在連線至伺服器時，啟用 ssl 強制執行。
  - `[StorageProfileBackupRetentionDay <Int32?>]`：伺服器的備份保留天數。
  - `[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`：啟用地域冗余，或不用於伺服器備份。
  - `[StorageProfileStorageAutogrow <StorageAutogrow?>]`：啟用儲存空間自動增長。
  - `[StorageProfileStorageMb <Int32?>]`：伺服器允許的最大儲存空間。
  - `[UserVisibleState <ServerState?>]`：使用者可看見的伺服器狀態。
  - `[Version <ServerVersion?>]`：伺服器版本。

## 相關連結

