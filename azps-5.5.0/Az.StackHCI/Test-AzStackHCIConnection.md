---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/test-azstackhciconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
ms.openlocfilehash: 34831104bc1b27aa115d56545c784e0fea856ba4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100128147"
---
# Test-AzStackHCIConnection

## 摘要
Test-AzStackHCIConnection 驗證來自內部部署叢集節點的連線至 Azure 堆疊 HCI 所需的 Azure 服務。

## 句法

```
Test-AzStackHCIConnection [[-EnvironmentName] <String>] [[-Region] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [<CommonParameters>]
```

## 說明
Test-AzStackHCIConnection 驗證來自內部部署叢集節點的連線至 Azure 堆疊 HCI 所需的 Azure 服務。

## 示例

### 範例1
```powershell
C:\PS\>Test-AzStackHCIConnection
Test: Connect to Azure Stack HCI Service
EndpointTested: https://azurestackhci-df.azurefd.net/health
IsRequired: True
Result: Succeeded
```
在其中一個叢集節點上喚醒。 成功案例。

### 範例2
```powershell
C:\PS\>Test-AzStackHCIConnection
Test: Connect to Azure Stack HCI Service
EndpointTested: https://azurestackhci-df.azurefd.net/health
IsRequired: True
Result: Failed
FailedNodes: Node1inClus2, Node2inClus3
```
在其中一個叢集節點上喚醒。 失敗的情況。

## 參數

### -ComputerName
指定登錄至 Azure 之內部部署群集中的其中一個叢集節點。

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

### -認證
指定 ComputerName 的認證。
[預設值] 是執行 Cmdlet 的目前使用者。

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
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
Position: 1
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### -Region
指定要連接的地區。
除非是 [無中的區域]，否則不使用。

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

## 輸出

### PSCustomObject. 在 PSCustomObject 中傳回下列屬性
### 測試：執行的測試名稱。
### EndpointTested：測試中使用的端點。
### IsRequired： True 或 False
### 結果：成功或失敗
### FailedNodes：測試失敗的節點清單。
## 筆記

## 相關連結
