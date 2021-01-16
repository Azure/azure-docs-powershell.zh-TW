---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 1CA26790-C791-4BFD-B986-70F28E3B095B
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActionGroup.md
ms.openlocfilehash: 90bd9c7943e6e788d81f8ddec85513676afade23
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98282963"
---
# Get-AzActionGroup

## 摘要
取得動作群組 (s) 。

## 句法

### BySubscriptionOrResourceGroup (預設) 
```
Get-AzActionGroup [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByName
```
Get-AzActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
**AzActionGroup** Cmdlet 會取得一或多個動作群組。

## 示例

### 範例1：依訂閱識別碼取得動作群組
```
PS C:\>Get-AzActionGroup
```

這個命令會列出目前訂閱的所有動作群組。

### 範例2：取得指定資源群組的動作群組
```
PS C:\>Get-AzActionGroup -ResourceGroup "Default-activityLogAlerts"
```

這個命令會列出指定資源群組的 [動作] 群組。

### 範例3：取得動作群組。
```
PS C:\>Get-AzActionGroup -ResourceGroup "Default-activityLogAlerts" -Name "actionGroup1"
```

這個命令會列出一個 (清單，其中只有一個元素) [動作] 群組。

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
動作群組的名稱。

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
資源群組名稱

```yaml
Type: System.String
Parameter Sets: BySubscriptionOrResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### System.object

## 輸出

### PSActionGroupResource 中的 OutputClasses。

## 筆記

## 相關連結

[Set-AzActionGroup](./Set-AzActionGroup.md) 
[移除-AzActionGroup](./Remove-AzActionGroup.md) 
[新-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)
