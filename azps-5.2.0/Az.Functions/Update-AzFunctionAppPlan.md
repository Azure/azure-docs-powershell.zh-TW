---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/update-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
ms.openlocfilehash: e0831e95a5601d3558af7089825684cc48e7838c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279400"
---
# Update-AzFunctionAppPlan

## 摘要
更新函數 app 服務方案。

## 句法

### ByName (預設) 
```
Update-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ByObjectInput
```
Update-AzFunctionAppPlan -InputObject <IAppServicePlan> [-MaximumWorkerCount <Int32>]
 [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## 說明
更新函數 app 服務方案。

## 示例

### 範例1：更新 app 服務方案以 EP2 含20個以上最大工人的 sku。
```powershell
PS C:\> Update-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                                 -Name MyPremiumPlan `
                                 -MaximumWorkerCount 20 `
                                 -Sku EP2

```

這個命令會更新應用程式服務方案，以 EP2 含二十個最大工人的 sku。

## 參數

### -AsJob
執行命令做為作業。

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
若要構造，請參閱適用于 INPUTOBJECT 屬性的 [記事] 區段，並建立雜湊表。

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan
Parameter Sets: ByObjectInput
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MaximumWorkerCount
App 服務方案的工作人數上限。

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MaxBurst

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinimumWorkerCount
App 服務方案的工作人數最小值。

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MinInstances

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
App 服務方案的名稱。

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait
以非同步方式執行命令。

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
資源所屬之資源群組的名稱。

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Sku
方案 sku。
有效的輸入為： EP1、EP2、EP3

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
Azure 訂閱 ID。

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
資源標記。

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

### IAppServicePlan 中的 Api20190801，然後再

## 輸出

### IAppServicePlan 中的 Api20190801，然後再

## 筆記

別名

複雜的參數屬性

若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。 如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。


INPUTOBJECT <IAppServicePlan> ： 
  - `Location <String>`：資源位置。
  - `[Kind <String>]`：資源類型。
  - `[Tag <IResourceTags>]`：資源標記。
    - `[(Any) <String>]`：這表示您可以將任何屬性新增至此物件。
  - `[Capacity <Int32?>]`：目前指派給資源的實例數。
  - `[FreeOfferExpirationTime <DateTime?>]`：伺服器場免費優惠到期的時間。
  - `[HostingEnvironmentProfileId <String>]`：應用程式服務環境的資源識別碼。
  - `[HyperV <Boolean?>]`：如果是 Hyper-v 容器 app 服務方案 <code>true</code> ，則 <code>false</code> 為。
  - `[IsSpot <Boolean?>]`： If <code>true</code> ，此 App 服務方案擁有的是污點實例。
  - `[IsXenon <Boolean?>]`：已過時：如果是 Hyper-v 容器 app 服務方案 <code>true</code> ，則 <code>false</code> 為。
  - `[MaximumElasticWorkerCount <Int32?>]`：此 ElasticScaleEnabled 應用程式服務方案允許的總工作人數上限
  - `[PerSiteScaling <Boolean?>]`： If <code>true</code> ，指派給這個 App 服務方案的應用程式可以獨立地伸縮。         如果 <code>false</code> 指派給這個 App 服務方案的應用程式將會縮放為方案的所有實例。
  - `[Reserved <Boolean?>]`：如果是 Linux app 服務方案 <code>true</code> ，則 <code>false</code> 為。
  - `[SkuCapability <ICapability[]>]`： SKU 的功能（例如，已啟用流量管理器）嗎？
    - `[Name <String>]`： SKU 功能的名稱。
    - `[Reason <String>]`： SKU 功能的原因。
    - `[Value <String>]`： SKU 功能的值。
  - `[SkuCapacityDefault <Int32?>]`：此應用程式服務方案 SKU 的預設工作執行緒數。
  - `[SkuCapacityMaximum <Int32?>]`：此 App 服務方案 SKU 的最大工作人數。
  - `[SkuCapacityMinimum <Int32?>]`：此 App 服務方案 SKU 的最小員工數量。
  - `[SkuCapacityScaleType <String>]`：應用程式服務方案的可用縮放設定。
  - `[SkuFamily <String>]`：資源 SKU 的家用程式碼。
  - `[SkuLocation <String[]>]`： SKU 的位置。
  - `[SkuName <String>]`：資源 SKU 的名稱。
  - `[SkuSize <String>]`：資源 SKU 的大小指定符。
  - `[SkuTier <String>]`：資源 SKU 的服務層級。
  - `[SpotExpirationTime <DateTime?>]`：伺服器伺服器陣列的到期時間。 只有在它是專色伺服器群時才有效。
  - `[TargetWorkerCount <Int32?>]`：縮放工作人員計數。
  - `[TargetWorkerSizeId <Int32?>]`：縮放輔助角色大小 ID。
  - `[WorkerTierName <String>]`：指派給 App 服務方案的目標 worker 層。

## 相關連結

