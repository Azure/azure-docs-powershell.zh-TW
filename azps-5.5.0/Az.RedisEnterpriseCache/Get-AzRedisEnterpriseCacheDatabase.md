---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/get-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 99956b752b71309278af4c1f9b43b8efa9015f21
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100130906"
---
# Get-AzRedisEnterpriseCacheDatabase

## 摘要
取得 RedisEnterprise 群集中資料庫的相關資訊。

## 句法

```
Get-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## 說明
取得 RedisEnterprise 群集中資料庫的相關資訊。

## 示例

### 範例1：取得資料庫
```powershell
PS C:\> Get-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup"

Name    Type
----    ----
default Microsoft.Cache/redisEnterprise/databases

```

這個命令會取得名為 MyCache 之 Redis Enterprise Cache 的資料庫。

## 參數

### -ClusterName
RedisEnterprise 群集的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

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

### -ResourceGroupName
資源群組的名稱。

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

### -SubscriptionId
取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。
[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。

```yaml
Type: System.String[]
Parameter Sets: (All)
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

## 輸出

### IDatabase （RedisEnterpriseCache）。 Api20201001Preview。

## 筆記

別名

## 相關連結

