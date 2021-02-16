---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactivitylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
ms.openlocfilehash: 9b57d7584ee7720ec73aa57ddec070ad26ddff9f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100132714"
---
# Get-AzActivityLog

## 摘要
檢索活動記錄事件。

## 句法

### GetByCorrelationId
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-CorrelationId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByResourceId
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByResourceGroup
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceGroupName] <String> [-MaxRecord <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceProvider
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceProvider] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetBySubscription
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
Get-AzActivityLog Cmdlet 會檢索活動記錄事件。 事件可以與目前的訂閱識別碼、相關識別碼、資源群組、資源識別碼或資源提供者相關聯。

## 示例

### 範例1：依訂閱識別碼取得事件記錄
```
PS C:\>Get-ActivityAzLog
```

這個命令會列出與使用者訂閱識別碼相關聯的1000事件，這些事件是在目前日期/時間之前的7天內發生。

### 範例2：依訂閱識別碼（含最大事件數）來取得事件記錄
```
PS C:\>Get-AzActivityLog -MaxRecord 100
```

這個命令會列出與使用者訂閱識別碼相關聯的100事件，這些事件是在目前日期/時間之前的7天內發生。

### 範例3：依訂閱識別碼（含開始時間）取得事件記錄檔。
```
PS C:\>Get-AzActivityLog -StartTime 2017-06-01T10:30
```

這個命令會列出與在2017年或2017之後所發生的使用者訂閱識別碼相關聯的1000事件（最大01T10：30個當地時間），如果該日期/時間不是從目前日期/時間的90天之前。

### 範例4：按照訂閱識別碼，以開始時間和結束時間來取得事件記錄。
```
PS C:\>Get-AzActivityLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

這個命令最多可列出與在2017年或2017年之後所發生的使用者訂閱 ID 相關的事件 1000 01T10：30個當地時間，以及2017年-14T11：30（當地時間）如果整個日期/時間範圍不超過從目前日期/時間的90天，亦即： [保留期間]。

### 範例5：依相關識別碼取得事件記錄檔
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

這個命令會列出與指定的相關識別碼相關聯的1000事件，這些事件會從目前的日期/時間開始，發生7天。 
**注意**：這通常只是一個事件。

### 範例6：使用最大事件數的相關識別碼來取得事件記錄檔
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxRecord 100
```

這個命令會列出與指定的相關識別碼相關聯的100事件，這些事件會從目前的日期/時間開始，發生7天。 
**注意**：這通常只是一個事件。

### 範例7：依相關識別碼和開始時間取得事件記錄檔
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

這個命令最多可列出與2017年或2017之後所發生的指定相關識別碼相關聯的1000事件，22T04：30：00當地時間（如果開始時間不是從目前日期/時間的90天之前）。
**注意**：這通常只是一個事件。

### 範例8：依 [開始時間] 和 [結束時間] 的相關識別碼來取得事件記錄
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

這個命令會列出與在2017年或2017年15T04：30個當地時間，但在2017年到 04-25T12：30個當地時間為止，如果整個日期/時間範圍不是從目前日期/時間開始的90天內，就會列出與此設定相關聯的1000事件（例如： [保留期間]）。

### 範例9：取得資源群組的事件記錄
```
PS C:\>Get-AzActivityLog -ResourceGroupName "Contoso-Web-CentralUS"
```

這個命令1000最多可列出與指定資源群組相關聯的事件，這些事件是從目前的日期/時間開始7天。

### 範例10：取得含有最大事件數之資源群組的事件記錄檔
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -MaxRecord 100
```

這個命令會列出與特定資源群組相關聯的100事件，這些事件是從目前的日期/時間開始7天。

### 範例11：依開始時間取得資源群組的事件記錄
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

這個命令會列出與在2017年或之後發生的特定資源群組相關聯的1000事件（最大值），22T04：30：00當地時間（如果開始時間不早于目前日期/時間的90天）。

### 範例12：取得具有開始時間和結束時間之資源群組的事件記錄
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

這個命令會列出與在2017年或2017之後所發生的特定資源群組相關聯的1000事件，但在2017年到 04-25T12：30個15T04 之前，如果整個日期/時間範圍不超過從目前日期/時間的90天，亦即： [保留期間]。

### 範例13：透過資源識別碼取得事件記錄
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

這個命令會列出與指定的資源識別碼相關聯的1000事件，這些事件是從目前的日期/時間開始所發生的7天。

### 範例14：以資源識別碼（含最大事件數）來取得事件記錄
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxRecord 100
```

這個命令會列出與指定的資源識別碼相關聯的100事件，這些事件是從目前的日期/時間開始所發生的7天。

### 範例15：透過資源識別碼取得開始時間的事件記錄
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

這個命令最多可列出與2017年或2017之後所發生的指定資源識別碼相關聯的1000事件（22T04：30：00當地時間），如果開始時間不是從目前日期/時間的90天之前。

### 範例16：以資源識別碼（含開始時間和結束時間）來取得事件記錄
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

這個命令會列出與在2017年或2017年之後所發生的指定資源識別碼相關聯的1000事件，但在2017年到 04-25T12：30個15T04 之前，如果整個日期/時間範圍不是從目前日期/時間的90天之前，即為 [保留期間]。

### 範例17：透過資源提供者取得事件記錄
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web"
```

這個命令會列出與指定資源提供者相關的1000事件，這些事件是從目前的日期/時間開始所發生的7天。

### 範例18：以資源提供者取得最大事件數的事件記錄
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -MaxRecord 100
```

這個命令會列出與指定資源提供者相關的100事件，這些事件是從目前的日期/時間開始所發生的7天。

### 範例19：由資源提供者使用啟動時間來取得事件記錄檔
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

這個命令會列出與在2017年或之後所發生的指定資源提供者相關聯的1000事件（最多個），22T04：30：00當地時間（如果開始時間不是從目前日期/時間的90天之前）。

### 範例20：透過資源提供者取得開始時間和結束時間的事件記錄檔
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

這個命令會列出與在2017年或2017之後所發生的指定資源提供者所產生的1000事件（15T04：30個當地時間），但在2017年之前的25T12：30個當地時間（如果整個日期/時間範圍不是從目前日期/時間起的90天以內），亦即： [保留期間]。

## 參數

### -來電者
要提取事件的來電者

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CorrelationId
CorrelationId

```yaml
Type: System.String
Parameter Sets: GetByCorrelationId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

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

### -DetailedOutput
傳回包含事件之所有詳細資料的物件 (預設值是只傳回部分屬性，亦即傳回詳細資料) 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EndTime
查詢的 endTime

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxRecord
要提取的記錄數目上限。
別名： MaxRecords、MaxEvents

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
資源群組名稱

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
ResourceId

```yaml
Type: System.String
Parameter Sets: GetByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceProvider
ResourceProvider 名稱

```yaml
Type: System.String
Parameter Sets: GetByResourceProvider
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StartTime
查詢的 correlationId

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -狀態
要提取事件的狀態

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### System.object Null ' 1 [CoreLib，System.object = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]

### System.object

### SwitchParameter 的系統管理功能

### System.object

## 輸出

### PSEventData 中的 OutputClasses。

## 筆記

## 相關連結
