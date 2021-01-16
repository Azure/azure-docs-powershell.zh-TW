---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/unregister-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
ms.openlocfilehash: e063af1a489c9e68845f087e339f42de65281501
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98285496"
---
# Unregister-AzStackHCI

## 摘要
Unregister-AzStackHCI 刪除代表內部部署群集的 AzureStackHCI 雲端資源，並以 Azure 登出內部部署群集。
如果未傳遞任何參數，則會使用在群集上註冊的資訊來登出群集。

## 句法

```
Unregister-AzStackHCI [[-SubscriptionId] <String>] [[-ResourceName] <String>] [[-TenantId] <String>]
 [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>] [[-GraphAccessToken] <String>]
 [[-AccountId] <String>] [[-EnvironmentName] <String>] [[-ComputerName] <String>] [-UseDeviceAuthentication]
 [[-Credential] <PSCredential>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
Unregister-AzStackHCI 刪除代表內部部署群集的 AzureStackHCI 雲端資源，並以 Azure 登出內部部署群集。
如果未傳遞任何參數，則會使用在群集上註冊的資訊來登出群集。

## 示例

### 範例1
```
Invoking on one of the cluster node
```

C:\PS \> 取消註冊-AzStackHCI 結果：成功

### 範例2
```
Invoking from the management node
```

C:\PS \> 取消註冊-AzStackHCI-ComputerName ClusterNode1 結果：成功

### 範例3
```
Invoking from WAC
```

C:\PS \> [取消註冊-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd]-ArmAccessToken etyer .。。ere =-GraphAccessToken acyee。rerrer- user1@corp1.com DemoHCICluster3-ResourceGroupName DemoHCIRG-確認： $False 結果：成功

### 範例4
```
Invoking with all the parameters
```

C:\PS \> 取消註冊-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-CoNtext.resourcename HciCluster1-TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557"-ResourceGroupName HciClusterRG-ArmAccessToken eerrer .。。ere =-GraphAccessToken acee。rerrer- user1@corp1.com EnvironmentName AzureCloud-ComputerName node1hci-認證 Get-Credential 結果：成功

## 參數

### -AccountId
指定 ARM 存取權杖。
將它與 ArmAccessToken 和 GraphAccessToken 一起指定，將會避開 Azure 互動式登入。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ArmAccessToken
指定 ARM 存取權杖。
將此指定與 GraphAccessToken 和 AccountId 搭配使用，就可以避免 Azure 互動式登入。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ComputerName
指定登錄至 Azure 之內部部署群集中的其中一個叢集節點。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -認證
指定 ComputerName 的認證。
[預設值] 是執行 Cmdlet 的目前使用者。

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnvironmentName
指定 Azure 環境。
預設值為 AzureCloud。
有效值為 AzureCloud、AzureChinaCloud、AzureUSGovernment、AzureGermanCloud、AzurePPE

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### -GraphAccessToken
指定圖形存取權杖。
將此指定與 ArmAccessToken 和 AccountId 搭配使用，就可以避免 Azure 互動式登入。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
指定 Azure 資源組名稱。
如果沒有指定 \<LocalClusterName\> ，則會將 rg 用作資源組名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CoNtext.resourcename
指定在 Azure 中建立之資源的資源名稱。
如果沒有指定，則會使用內部部署的群集名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
指定 Azure 訂閱以建立資源

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TenantId
指定 Azure TenantId。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseDeviceAuthentication
使用裝置程式碼驗證，而非互動式瀏覽器提示。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
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

## 輸出

### PSCustomObject. 在 PSCustomObject 中傳回下列屬性
### 結果：成功或失敗或已取消。
## 筆記

## 相關連結
