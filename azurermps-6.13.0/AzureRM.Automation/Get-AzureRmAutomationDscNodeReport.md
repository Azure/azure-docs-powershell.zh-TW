---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 1246C3AC-A123-4EA1-B99E-458A85789109
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdscnodereport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeReport.md
ms.openlocfilehash: 747ffdb9df955609a38718016af50bb5434c0224
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624939"
---
# Get-AzureRmAutomationDscNodeReport

## 摘要
取得從 DSC 節點傳送到自動化的報表。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### ByAll (預設) 
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByLatest
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> [-Latest] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ById
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmAutomationDscNodeReport** Cmdlet 會從傳送所需的接入件人狀態設定傳送報告至 Azure 自動化 (DSC) 節點。

## 示例

### 範例1：取得 DSC 節點的所有報表
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup14" -AutomationAccountName "Contoso17" -NodeId $Node.Id
```

第一個命令會取得名為 Contoso17 之自動化帳戶中名為 Computer14 的電腦的 DSC 節點。
該命令會將這個物件儲存在 $Node 變數中。
第二個命令會從名為 Computer14 的 DSC 節點傳送到名為 Contoso17 的自動化帳戶的所有報表，取得中繼資料。
命令會使用 $Node 物件的 **識別碼** 屬性來指定節點。

### 範例2：依報表識別碼取得 DSC 節點的報表
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

第一個命令會取得名為 Contoso17 之自動化帳戶中名為 Computer14 的電腦的 DSC 節點。
該命令會將這個物件儲存在 $Node 變數中。
第二個命令會針對從名為 Computer14 的 DSC 節點傳送給名為 Contoso17 之自動化帳戶的指定識別碼所標識的報表，取得中繼資料。

### 範例3：取得 DSC 節點的最新報表
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Latest
```

第一個命令會取得名為 Contoso17 之自動化帳戶中名為 Computer14 的電腦的 DSC 節點。
該命令會將這個物件儲存在 $Node 變數中。
第二個命令會針對從名為 Computer14 的 DSC 節點傳送到名為 Contoso17 的自動化帳戶的最新報表，取得中繼資料。

## 參數

### -AutomationAccountName
指定自動化帳戶的名稱。
這個 Cmdlet 會匯出屬於此參數所指定帳戶的 DSC 節點報告。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndTime
指定結束時間。
這個 Cmdlet 會取得此時間之前接收到的自動報告。

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -識別碼
指定此 Cmdlet 要取得的 DSC 節點報告的唯一識別碼。

```yaml
Type: System.Guid
Parameter Sets: ById
Aliases: ReportId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -最新
表示此 Cmdlet 只會取得指定節點的最新 DSC 報告。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByLatest
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -
指定此 Cmdlet 取得報告之 DSC 節點的唯一識別碼。

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定包含此 Cmdlet 取得報告之 DSC 節點之資源群組的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StartTime
指定開始時間。
這個 Cmdlet 會取得此時間之後自動接收的報告。

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### Guid.empty

### System.object "1 [[System. DateTimeOffset，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]

### System.object

## 輸出

### DscNode 中的 [.]

## 筆記

## 相關連結

[AzureRmAutomationDscNode](./Get-AzureRmAutomationDscNode.md)

[Export-AzureRmAutomationDscNodeReportContent](./Export-AzureRmAutomationDscNodeReportContent.md)


