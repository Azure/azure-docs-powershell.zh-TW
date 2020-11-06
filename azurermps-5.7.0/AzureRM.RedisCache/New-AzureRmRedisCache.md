---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
ms.openlocfilehash: bbba6372be7176b8ac1aec553a9abbbf83c7da31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447697"
---
# New-AzureRmRedisCache

## 摘要
建立 Redis 快取。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
New-AzureRmRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-RedisVersion <String>]
 [-Size <String>] [-Sku <String>] [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>]
 [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-VirtualNetwork <String>]
 [-Subnet <String>] [-SubnetId <String>] [-StaticIP <String>] [-Tag <Hashtable>] [-Zone <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**新的-AzureRmRedisCache** Cmdlet 會建立 Azure Redis Cache。

## 示例

### 範例1：建立 Redis 快取
```
PS C:\>New-AzureRmRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US"

          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : MyGroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/mycache
          Location           : North Central US
          Name               : MyCache
          Type               : Microsoft.Cache/Redis
          HostName           : mycache.redis.cache.windows.net 
          Port               : 6379
          ProvisioningState  : creating
          SslPort            : 6380
          RedisConfiguration : {}
          EnableNonSslPort   : False
          RedisVersion       : 2.8
          Size               : 1GB
          Sku                : Standard
          Tag                : {}
          Zone               : []
```

這個命令會建立 Redis 快取。

### 範例2：建立標準 SKU Redis 快取
```
PS C:\>New-AzureRmRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US" -Size 250MB -Sku "Standard" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"} -Force

          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : MyGroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/MyCache
          Location           : North Central US
          Name               : mycache
          Type               : Microsoft.Cache/Redis
          HostName           : mycache.redis.cache.windows.net
          Port               : 6379
          ProvisioningState  : creating
          SslPort            : 6380
          RedisConfiguration : {[maxmemory-policy, allkeys-random]} 
          EnableNonSslPort   : False
          RedisVersion       : 2.8
          Size               : 250MB
          Sku                : Standard
          Tag                : {}
          Zone               : []
```

這個命令會建立 Redis 快取。

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableNonSslPort
指出是否已啟用非 SSL 埠。
預設值為 $False (停用非 SSL 埠) 。

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -位置
指定要建立 Redis 快取的位置。
有效值為： 

- 美國中北部
- 美國中南部
- 美國中部
- 西歐
- 北歐
- 美國西部
- 東美國
- 東美國2
- 日本東
- 日本西部
- 巴西南部
- 東南亞
- 東亞
- 澳大利亞東
- 澳大利亞東南部

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxMemoryPolicy
已棄用此參數。
使用 *RedisConfiguration* 參數來設定 maxmemory 原則。
例如： 

`-RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}`

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -名稱
指定要建立之 Redis 緩存的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RedisConfiguration
指定 Redis 設定。
此參數可接受的值為：

- rdb-備份-啟用。
指定已啟用 Redis 資料暫留。
僅限 [特優] 層。
- rdb-儲存體-連接字串。
指定 Redis 資料暫留的儲存空間帳戶連接字串。
僅限 [特優] 層。
- rdb-備份頻率。
指定 Redis 資料暫留的備份頻率。
僅限 [特優] 層。 
- maxmemory-保留。
針對非快取程式配置保留的記憶體。
[標準] 和 [特優] 層。 
- maxmemory-原則。
設定快取的快取原則。
所有定價層。 
- notify-keyspace-事件。
配置 keyspace 通知。
[標準] 和 [特優] 層。 
- 散列-最大值-ziplist-專案。
針對小型匯總資料類型配置記憶體優化。
[標準] 和 [特優] 層。 
- 散列-最大值-ziplist。
針對小型匯總資料類型配置記憶體優化。
[標準] 和 [特優] 層。 
- intset-專案（最大值）。
針對小型匯總資料類型配置記憶體優化。
[標準] 和 [特優] 層。 
- zset-最大 ziplist 專案。
針對小型匯總資料類型配置記憶體優化。
[標準] 和 [特優] 層。 
- zset-最大 ziplist 值。
針對小型匯總資料類型配置記憶體優化。
[標準] 和 [特優] 層。 
- 資料庫.
設定資料庫的數目。
這個屬性只能在建立快取記憶體時設定。
[標準] 和 [特優] 層。

如需詳細資訊，請參閱使用 Azure PowerShell (管理 Azure Redis Cache https://go.microsoft.com/fwlink/?LinkId=800051 https://go.microsoft.com/fwlink/?LinkId=800051) 。

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RedisVersion
此參數已棄用，將會從未來版本中移除。

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定要在其中建立 Redis 快取的資源群組的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ShardCount
指定要在 Premium 群集快取上建立的 shards 數目。
此參數可接受的值為：

- sr-1
- pplx-2
- 3
- 4
- 500
- 6
- utf-7
- 型
- 9 
- 第

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -大小
指定 Redis 快取的大小。
有效值為： 

- P1
- 又
- P3
- P4
- C0
- C1
- C3
- C3
- C4
- C5
- C6
- 250MB
- 1GB
- 2.5 GB
- 6GB
- 13GB
- 26GB
- 53GB

預設值為1GB 或 C1。

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: P1, P2, P3, P4, C0, C1, C2, C3, C4, C5, C6, 250MB, 1GB, 2.5GB, 6GB, 13GB, 26GB, 53GB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Sku
指定要建立之 Redis 快取的 SKU。
有效值為： 

- 空白
- 標準
- 佳

預設值為 [標準]。

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StaticIP
在 Redis 快取的子網上指定唯一的 IP 位址。

如果您沒有指定此參數的值，這個 Cmdlet 會從子網上選擇 IP 位址。

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -子網
指定要在其中部署 Redis 快取的子網名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubnetId
```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
代表標記的雜湊資料表。

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TenantSettings
已棄用此參數。

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetwork
指定要部署 Redis 快取的虛擬網路資源識別碼。

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
區域清單。

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -確認
在執行 Cmdlet 之前提示您進行確認。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
顯示在執行 Cmdlet 時會發生什麼情況。 未執行 Cmdlet。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有
您可以依名稱將輸入管到這個 Cmdlet，但不能依值進行。

## 輸出

### RedisCacheAttributesWithAccessKeys 中的 RedisCache。
這個 Cmdlet 會傳回 Redis 快取的所有屬性，包括主要和次要便捷鍵。

## 筆記

## 相關連結

[AzureRmRedisCache](./Get-AzureRmRedisCache.md)

[移除-AzureRmRedisCache](./Remove-AzureRmRedisCache.md)

[Set-AzureRmRedisCache](./Set-AzureRmRedisCache.md)


