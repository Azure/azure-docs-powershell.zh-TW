---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azactivitylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
ms.openlocfilehash: b966f15cc42ffc61f7d88cd5a1855f31564742ee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908973"
---
# Get-AzActivityLog

## 簡介
取回活動記錄事件。

## 語法

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

## 描述
Cmdlet Get-AzActivityLog活動記錄事件。 事件可以與目前的訂閱識別碼、相關識別碼、資源群組、資源識別碼或資源提供者相關聯。

## 例子

### 範例 1：根據訂閱識別碼取得事件記錄
```
PS C:\>Get-AzActivityLog
```

此命令會列出最多 1000 個與使用者訂閱識別碼相關聯的事件，這些事件從目前日期/時間起 7 天發生。

### 範例 2：根據訂閱識別碼取得事件記錄，事件數目上限
```
PS C:\>Get-AzActivityLog -MaxRecord 100
```

此命令會列出最多 100 個與使用者訂閱識別碼相關聯的事件，這些事件從目前日期/時間起 7 天后發生。

### 範例 3：取得具有開始時間之訂閱識別碼的事件記錄。
```
PS C:\>Get-AzActivityLog -StartTime 2017-06-01T10:30
```

此命令會列出最多與 2017-06-01T10：30 當地時間發生或之後之使用者訂閱識別碼相關聯的 1000 個事件，如果日期/時間不大於目前日期/時間 90 天。

### 範例 4：取得具有開始時間和結束時間之訂閱識別碼的事件記錄。
```
PS C:\>Get-AzActivityLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

此命令會列出最多 1000 個與 2017-04-01T10：30 當地時間，以及 2017-04-14T11：30 當地時間之前發生之使用者訂閱識別碼相關聯的事件，如果整個日期/時間範圍不大於目前日期/時間 90 天，即保留期間。

### 範例 5：根據相關識別碼取得事件記錄
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

此命令會列出最多 1000 個與指定相關識別碼相關聯的事件，這些事件從目前日期/時間起 7 天發生。 
**注意**：這通常只有一個事件。

### 範例 6：以事件數目上限的關聯識別碼取得事件記錄
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxRecord 100
```

此命令會列出最多 100 個與指定相關識別碼相關聯的事件，這些事件自目前日期/時間起 7 天之後發生。 
**注意**：這通常只有一個事件。

### 範例 7：根據相關識別碼和開始時間取得事件記錄
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

此命令會列出最多與 2017-05-22T04：30：00 當地時間發生或之後所指定相關識別碼相關聯的 1000 個事件 ，如果開始時間不大於目前日期/時間 90 天。
**注意**：這通常只有一個事件。

### 範例 8：根據相關 ID 取得事件記錄與開始時間和結束時間
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

此命令會列出與 2017-04-15T04：30 當地時間當天或之後所發生之指定相關識別碼相關聯的最多 1000 個事件，但如果整個日期/時間範圍不大於目前日期/時間 90 天 ，即保留期間，則于 2017-04-25T12：30 當地時間之前發生。

### 範例 9：取得資源群組的事件記錄
```
PS C:\>Get-AzActivityLog -ResourceGroupName "Contoso-Web-CentralUS"
```

此命令會列出最多 1000 個與指定資源群組相關聯的事件，這些事件會從目前日期/時間起 7 天發生。

### 範例 10：取得事件數上限的資源群組事件記錄
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -MaxRecord 100
```

此命令會列出最多 100 個與指定資源群組相關聯的事件，這些事件會從目前日期/時間起 7 天發生。

### 範例 11：根據開始時間取得資源群組的事件記錄
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

此命令會列出在 2017-05-22T04：30：00 當地時間當天或之後發生與指定資源群組相關聯的最多 1000 個事件，如果開始時間不大於目前日期/時間 90 天。

### 範例 12：取得具有開始時間和結束時間的資源群組的事件記錄
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

此命令會列出最多 1000 個與指定資源群組相關聯的事件，這些事件是在 2017-04-15T04：30 當地時間發生，但如果整個日期/時間範圍不大於目前日期/時間 90 天，即保留期間，則列于 2017-04-25T12：30 當地時間之前。

### 範例 13：根據資源識別碼取得事件記錄
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

此命令會列出與指定資源識別碼相關聯的最多 1000 個事件，這些事件從目前日期/時間起 7 天后發生。

### 範例 14：根據資源識別碼取得事件記錄，事件數目上限
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxRecord 100
```

此命令會列出最多 100 個與指定資源識別碼相關聯的事件，這些事件從目前日期/時間開始 7 天之後發生。

### 範例 15：根據資源識別碼取得具有開始時間的事件記錄
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

此命令會列出最多與 2017-05-22T04：30：00 當地時間發生或之後所指定資源識別碼相關聯的 1000 個事件，如果開始時間不大於目前日期/時間 90 天。

### 範例 16：根據資源識別碼取得具有開始時間和結束時間的事件記錄
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

此命令會列出最多與 2017-04-15T04：30 當地時間發生或之後所發生之指定資源識別碼相關聯的 1000 個事件，但如果整個日期/時間範圍不大於目前日期/時間 90 天，即保留期間，則列于 2017-04-25T12：30 當地時間之前。

### 範例 17：根據資源提供者取得事件記錄
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web"
```

此命令會列出與指定資源提供者相關聯的最多 1000 個事件，這些事件從目前日期/時間起 7 天后發生。

### 範例 18：根據資源提供者取得事件記錄，事件數目上限
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -MaxRecord 100
```

此命令會列出最多 100 個與指定資源提供者相關聯的事件，這些事件從目前日期/時間起 7 天發生。

### 範例 19：根據資源提供者取得具有開始時間的事件記錄
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

此命令會列出在 2017-05-22T04：30：00 當地時間當天或之後發生與指定資源提供者相關聯的最多 1000 個事件，如果開始時間不大於目前日期/時間 90 天。

### 範例 20：根據資源提供者取得具有開始時間和結束時間的事件記錄
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

此命令會列出在 2017-04-15T04：30 當地時間當天或之後，與指定資源提供者相關聯的最多 1000 個事件，但如果整個日期/時間範圍不大於目前日期/時間 90 天 ，即保留期間，則于 2017-04-25T12：30 當地時間之前發生。

## 參數

### -本機號碼
要抓取之事件的來電者

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
The CorrelationId

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
用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。

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
包含所有事件詳細資料 (的 Return 物件預設只會返回某些屬性，例如沒有詳細資料) 

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
查詢的 EndTime

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
要抓取的記錄數目上限。
別名：MaxRecords，MaxEvents

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
資源組名

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
The ResourceId

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
查詢的相關資料

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
要抓取的事件狀態

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
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### System.Nullable'1[[System.DateTime， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]

### System.String

### System.Management.Automation.SwitchParameter

### System.Int32

## 輸出

### Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData

## 筆記

## 相關連結
