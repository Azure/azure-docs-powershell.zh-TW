---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/update-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
ms.openlocfilehash: 522de6721d92b76938843b28322b94b5cc6ce481
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904682"
---
# Update-AzFunctionAppPlan

## 簡介
更新功能應用程式服務方案。

## 語法

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

## 描述
更新功能應用程式服務方案。

## 例子

### 範例 1：將 App 服務方案更新為 EP2 SKU，並包含最多二十名員工。
```powershell
PS C:\> Update-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                                 -Name MyPremiumPlan `
                                 -MaximumWorkerCount 20 `
                                 -Sku EP2

```

此命令將 App 服務方案更新為 EP2 SKU，最多 20 位員工。

## 參數

### -AsJob
以工作執行命令。

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
若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，然後建立雜湊表。

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
應用程式服務方案的員工人數上限。

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
應用程式服務方案的最小工作人員人數。

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
應用程式服務方案的名稱。

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
非同步執行命令。

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
資源所屬的資源組名。

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

### -SKU
方案 SKU。
有效的輸入為：EP1、EP2、EP3

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
Azure 訂閱識別碼。

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

### -標記
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
執行 Cmdlet 之前，提示您確認。

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
顯示 Cmdlet 執行時會發生什麼情況。
不會執行 Cmdlet。

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
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### Microsoft.Azure.PowerShell.Cmdlets.Functions.models.Api20190801.IAppServicePlan

## 輸出

### Microsoft.Azure.PowerShell.Cmdlets.Functions.models.Api20190801.IAppServicePlan

## 筆記

別名

複雜的參數屬性

若要建立下列描述的參數，請建構包含適當屬性的雜湊表。 有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。


INPUTOBJECT： <IAppServicePlan> 
  - `Location <String>`：資源位置。
  - `[Kind <String>]`：資源類型。
  - `[Tag <IResourceTags>]`：資源標記。
    - `[(Any) <String>]`：這表示任何屬性都可以新增到這個物件。
  - `[Capacity <Int32?>]`：指派給資源的目前實例數目。
  - `[FreeOfferExpirationTime <DateTime?>]`：伺服器伺服器伺服器系列免費優惠到期的時間。
  - `[HostingEnvironmentProfileId <String>]`：應用程式服務環境的資源識別碼。
  - `[HyperV <Boolean?>]`：如果 Hyper-V 容器應用程式服務方案， <code>true</code> 否則 <code>false</code> 。
  - `[IsSpot <Boolean?>]`：如果 <code>true</code> ，此應用程式服務方案擁有 spot 實例。
  - `[IsXenon <Boolean?>]`：已過時：如果 Hyper-V 容器應用程式服務方案 <code>true</code> ，否則 <code>false</code> 。
  - `[MaximumElasticWorkerCount <Int32?>]`：此ScaleEnabled App 服務方案允許的工作者總數上限
  - `[PerSiteScaling <Boolean?>]`： <code>true</code> 如果 ，指派給此應用程式服務方案的應用程式可以獨立縮放。         如果 <code>false</code> ，指派給此應用程式服務方案的應用程式會縮放至計畫的所有實例。
  - `[Reserved <Boolean?>]`：否則，如果 Linux 應用程式服務方案 <code>true</code> <code>false</code> 。
  - `[SkuCapability <ICapability[]>]`：SKU 的功能，例如，是否已啟用流量管理員？
    - `[Name <String>]`：SKU 功能的名稱。
    - `[Reason <String>]`：SKU 功能的原因。
    - `[Value <String>]`：SKU 功能的值。
  - `[SkuCapacityDefault <Int32?>]`：此 App 服務方案 SKU 的預設工作人員人數。
  - `[SkuCapacityMaximum <Int32?>]`：此 App 服務方案 SKU 的員工人數上限。
  - `[SkuCapacityMinimum <Int32?>]`：此 App 服務方案 SKU 的最小員工人數。
  - `[SkuCapacityScaleType <String>]`：應用程式服務方案可用的縮放比例組配置。
  - `[SkuFamily <String>]`：資源 SKU 的家庭代碼。
  - `[SkuLocation <String[]>]`：SKU 的位置。
  - `[SkuName <String>]`：資源 SKU 的名稱。
  - `[SkuSize <String>]`：資源 SKU 的大小指定元。
  - `[SkuTier <String>]`：資源 SKU 的服務層級。
  - `[SpotExpirationTime <DateTime?>]`：伺服器伺服器伺服器組到期的時間。 只有當它是 Spot 伺服器時，才有效。
  - `[TargetWorkerCount <Int32?>]`：縮放員工計數。
  - `[TargetWorkerSizeId <Int32?>]`：縮放員工大小識別碼。
  - `[WorkerTierName <String>]`：指派給應用程式服務方案的目標員工層級。

## 相關連結

