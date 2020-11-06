---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmLog.md
ms.openlocfilehash: 90f65c7e3db862ca4d24b67187f587511593be4d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449130"
---
# Get-AzureRmLog

## 摘要
取得事件的記錄。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### GetByCorrelationId
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-CorrelationId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByResourceId
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByResourceGroup
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceGroupName] <String> [-MaxRecord <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceProvider
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceProvider] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetBySubscription
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmLog** Cmdlet 會取得事件的記錄。
事件可以與目前的訂閱識別碼、相關識別碼、資源群組、資源識別碼或資源提供者相關聯。

## 示例

### 範例1：依訂閱識別碼取得事件記錄
```
PS C:\>Get-AzureRmLog
```

這個命令會列出與使用者訂閱識別碼相關聯的1000事件，這些事件是在目前日期/時間之前的7天內發生。

### 範例2：依訂閱識別碼（含最大事件數）來取得事件記錄
```
PS C:\>Get-AzureRmLog -MaxEvents 100
```

這個命令會列出與使用者訂閱識別碼相關聯的100事件，這些事件是在目前日期/時間之前的7天內發生。

### 範例3：依訂閱識別碼（含開始時間）取得事件記錄檔。
```
PS C:\>Get-AzureRmLog -StartTime 2017-06-01T10:30
```

這個命令會列出與在2017年或2017之後所發生的使用者訂閱識別碼相關聯的1000事件（最大01T10：30個當地時間），如果該日期/時間不是從目前日期/時間的90天之前。

### 範例4：按照訂閱識別碼，以開始時間和結束時間來取得事件記錄。
```
PS C:\>Get-AzureRmLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

這個命令最多可列出與在2017年或2017年之後所發生的使用者訂閱 ID 相關的事件 1000 01T10：30個當地時間，以及2017年-14T11：30（當地時間）如果整個日期/時間範圍不超過從目前日期/時間的90天，亦即： [保留期間]。

### 範例5：依相關識別碼取得事件記錄檔
```
PS C:\>Get-AzureRmLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

這個命令會列出與指定的相關識別碼相關聯的1000事件，這些事件會從目前的日期/時間開始，發生7天。 
**注意** ：這通常只是一個事件。

### 範例6：使用最大事件數的相關識別碼來取得事件記錄檔
```
PS C:\>Get-AzureRmLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxEvents 100
```

這個命令會列出與指定的相關識別碼相關聯的100事件，這些事件會從目前的日期/時間開始，發生7天。 
**注意** ：這通常只是一個事件。

### 範例7：依相關識別碼和開始時間取得事件記錄檔
```
PS C:\>Get-AzureRmLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

這個命令最多可列出與2017年或2017之後所發生的指定相關識別碼相關聯的1000事件，22T04：30：00當地時間（如果開始時間不是從目前日期/時間的90天之前）。
**注意** ：這通常只是一個事件。

### 範例8：依 [開始時間] 和 [結束時間] 的相關識別碼來取得事件記錄
```
PS C:\>Get-AzureRmLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

這個命令會列出與在2017年或2017年15T04：30個當地時間，但在2017年到 04-25T12：30個當地時間為止，如果整個日期/時間範圍不是從目前日期/時間開始的90天內，就會列出與此設定相關聯的1000事件（例如： [保留期間]）。

### 範例9：取得資源群組的事件記錄
```
PS C:\>Get-AzureRmLog -ResourceGroupName "Contoso-Web-CentralUS"
```

這個命令1000最多可列出與指定資源群組相關聯的事件，這些事件是從目前的日期/時間開始7天。

### 範例10：取得含有最大事件數之資源群組的事件記錄檔
```
PS C:\>Get-AzureRmLog -ResourceGroup "Contoso-Web-CentralUS" -MaxEvents 100
```

這個命令會列出與特定資源群組相關聯的100事件，這些事件是從目前的日期/時間開始7天。

### 範例11：依開始時間取得資源群組的事件記錄
```
PS C:\>Get-AzureRmLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

這個命令最多可列出與2017年或之後所發生的指定資源群組相關聯的 1000 evetns，22T04：30：00當地時間（如果開始時間不早于目前日期/時間的90天）。

### 範例12：取得具有開始時間和結束時間之資源群組的事件記錄
```
PS C:\>Get-AzureRmLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

這個命令會列出與在2017年或2017之後所發生的特定資源群組相關聯的1000事件，但在2017年到 04-25T12：30個15T04 之前，如果整個日期/時間範圍不超過從目前日期/時間的90天，亦即： [保留期間]。

### 範例13：透過資源識別碼取得事件記錄
```
PS C:\>Get-AzureRmLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

這個命令會列出與指定的資源識別碼相關聯的1000事件，這些事件是從目前的日期/時間開始所發生的7天。

### 範例14：以資源識別碼（含最大事件數）來取得事件記錄
```
PS C:\>Get-AzureRmLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxEvents 100
```

這個命令會列出與指定的資源識別碼相關聯的100事件，這些事件是從目前的日期/時間開始所發生的7天。

### 範例15：透過資源識別碼取得開始時間的事件記錄
```
PS C:\>Get-AzureRmLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

這個命令最多可列出與2017年或2017之後所發生的指定資源識別碼相關聯的1000事件（22T04：30：00當地時間），如果開始時間不是從目前日期/時間的90天之前。

### 範例16：以資源識別碼（含開始時間和結束時間）來取得事件記錄
```
PS C:\>Get-AzureRmLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

這個命令會列出與在2017年或2017年之後所發生的指定資源識別碼相關聯的1000事件，但在2017年到 04-25T12：30個15T04 之前，如果整個日期/時間範圍不是從目前日期/時間的90天之前，即為 [保留期間]。

### 範例17：透過資源提供者取得事件記錄
```
PS C:\>Get-AzureRmLog -ResourceProvider "Microsoft.Web"
```

這個命令會列出與指定資源提供者相關的1000事件，這些事件是從目前的日期/時間開始所發生的7天。

### 範例18：以資源提供者取得最大事件數的事件記錄
```
PS C:\>Get-AzureRmLog -ResourceProvider "Microsoft.Web" -MaxEvents 100
```

這個命令會列出與指定資源提供者相關的100事件，這些事件是從目前的日期/時間開始所發生的7天。

### 範例19：由資源提供者使用啟動時間來取得事件記錄檔
```
PS C:\>Get-AzureRmLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

這個命令會列出與在2017年或之後所發生的指定資源提供者相關聯的1000事件（最多個），22T04：30：00當地時間（如果開始時間不是從目前日期/時間的90天之前）。

### 範例20：透過資源提供者取得開始時間和結束時間的事件記錄檔
```
PS C:\>Get-AzureRmLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

這個命令會列出與在2017年或2017之後所發生的指定資源提供者所產生的1000事件（15T04：30個當地時間），但在2017年之前的25T12：30個當地時間（如果整個日期/時間範圍不是從目前日期/時間起的90天以內），亦即： [保留期間]。

## 參數

### -來電者
指定來電者。

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
指定相關識別碼。
這個參數是必要的。

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

### -DetailedOutput
表示此 Cmdlet 會顯示詳細的輸出。
根據預設，輸出是匯總的。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Switch not present = False, i.e. output summarized
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EndTime
指定當地時間的查詢結束時間。
預設值是目前的時間。
此值必須晚于 *StartTime* 。
您可以使用 Get-Date Cmdlet 來取得 **DateTime** 物件。

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Current date (time: 00:00:00 AM) + 1 day
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxRecord
指定要取得指定篩選的記錄總數。
預設值為1000，且已接受的最大值為100000。 負值和0會被忽略，且會使用預設值。

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1000
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定資源群組的名稱。

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
指定資源識別碼。

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
指定依據資源提供者的篩選。

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
指定當地時間查詢的開始時間。
預設值為 [ *EndTime* 減去七天]。
您可以使用 Get-Date Cmdlet 來取得 **DateTime** 物件。

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: EndTime - 7 days
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -狀態
指定狀態。

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 系統. Nullable "1 [[System. DateTime，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]

### System.object

### SwitchParameter 的系統管理功能

### System.object

## 輸出

### PSEventData 中的 OutputClasses。

## 筆記

## 相關連結
