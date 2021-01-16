---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/restore-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restore-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restore-AzMariaDbServer.md
ms.openlocfilehash: 95988d83cbb4c3dcf0b5da890bf38f8c40eb4dfa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281835"
---
# Restore-AzMariaDbServer

## 摘要
從現有的 MariaDB 還原 MariaDB。

## 句法

```
Restore-AzMariaDbServer -Name <String> -RestorePointInTime <DateTime> [-InputObject <IServer>]
 [-ResourceGroupName <String>] [-ServerName <String>] [-SubscriptionId <String>] [-Location <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## 說明
從現有的 MariaDB 還原 MariaDB。

## 示例

### 範例1：依伺服器名稱還原 PointInTime MariaDB。
```powershell
PS C:\> Restore-AzMariaDbServer -Name restore-db01 -ServerName mariadb-test-usegeo -ResourceGroupName mariadb-test-4rih5z -UsePointInTimeRestore -RestorePointInTime $(Get-Date) -Location eastus

Name         Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----         -------- ------------------ ------- ----------------------- -------   -------        --------------
restore-db01 eastus   adminuser          10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

這個命令會透過伺服器名稱還原 PointInTime MariaDB。

### 範例2：透過 server 物件還原 PointInTime MariaDB
```powershell
PS C:\> $db = Get-AzMariaDbServer -Name mariadb-test-usegeo -ResourceGroupName mariadb-test-4rih5z
PS C:\>Restore-AzMariaDbServer -Name restore-db02 -InputObject $db -UsePointInTimeRestore -RestorePointInTime $(Get-Date) -Location eastus

Name         Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----         -------- ------------------ ------- ----------------------- -------   -------        --------------
restore-db02 eastus   adminuser          10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

這個命令會透過 server 物件還原 PointInTime MariaDB。

## 參數

### -AsJob
執行命令做為工作

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
地區 DefaultParameters 用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

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
要從中還原的源伺服器物件。
若要構造，請參閱適用于 INPUTOBJECT 屬性的 [記事] 區段，並建立雜湊表。

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -位置
資源所在的位置。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
要還原的目標伺服器名稱。

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

### -NoWait
以非同步方式執行命令

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
包含資源之資源群組的名稱。
您可以從 Azure 資源管理器 API 或入口網站取得此值。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestorePointInTime
[地區] PointInTimeRestore 資源所在的位置。

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerName
要從中還原的源伺服器名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
取得唯一識別 Microsoft Azure 訂閱的訂閱 Id。
訂閱識別碼是每個服務呼叫 URI 的一部分。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
以鍵值對形式的特定應用程式中繼資料。

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -確認
在執行 Cmdlet 之前提示您進行確認。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
顯示在執行 Cmdlet 時會發生什麼情況。
未執行 Cmdlet。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### IServer （MariaDb）。 Api20180601Preview。

## 輸出

### IServer （MariaDb）。 Api20180601Preview。

## 筆記

別名

複雜的參數屬性

若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。 如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。


INPUTOBJECT <IServer> ：要從中還原的源伺服器物件。
  - `Location <String>`：資源所在的位置。
  - `[Tag <ITrackedResourceTags>]`：以鍵值對形式的特定應用程式中繼資料。
    - `[(Any) <String>]`：這表示您可以將任何屬性新增至此物件。
  - `[AdministratorLogin <String>]`：管理員的伺服器登入名稱。 只能在 (建立伺服器時指定，且在建立) 時需要。
  - `[EarliestRestoreDate <DateTime?>]`： (ISO8601 格式的最早還原點建立時間) 
  - `[FullyQualifiedDomainName <String>]`：伺服器的完整功能變數名稱。
  - `[IdentityType <IdentityType?>]`：身分識別類型。 將此值設定為 ' SystemAssigned」，即可自動為資源建立並指派 Azure Active Directory 主體。
  - `[MasterServerId <String>]`：複本伺服器的主伺服器 id。
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

