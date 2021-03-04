---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/powershell/module/az.importexport/update-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Update-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Update-AzImportExport.md
ms.openlocfilehash: 7b604c22878d3d76e66a6d615deb1b46cedaad32
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907654"
---
# Update-AzImportExport

## 簡介
更新工作的特定屬性。
您可以撥打此作業來通知匯進/匯出服務，指出包含匯進或匯出工作的硬碟已運送至 Microsoft 資料中心。
它也可以用來取消現有的工作。

## 語法

### UpdateExpanded (預設) 
```
Update-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-BackupDriveManifest] [-CancelRequested] [-DeliveryPackageCarrierName <String>]
 [-DeliveryPackageDriveCount <Int32>] [-DeliveryPackageShipDate <String>]
 [-DeliveryPackageTrackingNumber <String>] [-DriveList <IDriveStatus[]>] [-LogLevel <String>]
 [-ReturnAddressCity <String>] [-ReturnAddressCountryOrRegion <String>] [-ReturnAddressEmail <String>]
 [-ReturnAddressPhone <String>] [-ReturnAddressPostalCode <String>] [-ReturnAddressRecipientName <String>]
 [-ReturnAddressStateOrProvince <String>] [-ReturnAddressStreetAddress1 <String>]
 [-ReturnAddressStreetAddress2 <String>] [-ReturnShippingCarrierAccountNumber <String>]
 [-ReturnShippingCarrierName <String>] [-State <String>] [-Tag <IUpdateJobParametersTags>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### UpdateViaIdentityExpanded
```
Update-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>] [-BackupDriveManifest]
 [-CancelRequested] [-DeliveryPackageCarrierName <String>] [-DeliveryPackageDriveCount <Int32>]
 [-DeliveryPackageShipDate <String>] [-DeliveryPackageTrackingNumber <String>] [-DriveList <IDriveStatus[]>]
 [-LogLevel <String>] [-ReturnAddressCity <String>] [-ReturnAddressCountryOrRegion <String>]
 [-ReturnAddressEmail <String>] [-ReturnAddressPhone <String>] [-ReturnAddressPostalCode <String>]
 [-ReturnAddressRecipientName <String>] [-ReturnAddressStateOrProvince <String>]
 [-ReturnAddressStreetAddress1 <String>] [-ReturnAddressStreetAddress2 <String>]
 [-ReturnShippingCarrierAccountNumber <String>] [-ReturnShippingCarrierName <String>] [-State <String>]
 [-Tag <IUpdateJobParametersTags>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## 描述
更新工作的特定屬性。
您可以撥打此作業來通知匯進/匯出服務，指出包含匯進或匯出工作的硬碟已運送至 Microsoft 資料中心。
它也可以用來取消現有的工作。

## 例子

### 範例 1：根據資源群組和伺服器名稱更新 ImportExport 工作
```powershell
PS C:\> Update-AzImportExport -Name test-job -ResourceGroupName ImportTestRG -DeliveryPackageCarrierName pwsh -DeliveryPackageTrackingNumber pwsh20200000
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

此 Cmdlet 會根據資源群組和伺服器名稱更新 ImportExport 工作。

### 範例 2：根據身分識別更新 ImportExport 工作。
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG | Update-AzImportExport -CancelRequested
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

此 Cmdlet 會以身分識別更新 ImportExport 工作。

## 參數

### -AcceptLanguage
指定回應的偏好語言。

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

### -BackupDriveManifest
指出是否應該複製磁片磁碟機上的清單檔案以封鎖 Blob。

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

### -CancelRequested
如果指定，值必須為 True。
服務會嘗試取消該工作。

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
用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。

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

### -DeliveryPackageCarrierName
用來出貨匯進或匯出磁片磁碟機的電信業者名稱。

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

### -DeliveryPackageDriveCount
套件中包含的磁片磁碟機數量。

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeliveryPackageShipDate
包裹出貨日期。

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

### -DeliveryPackageTrackingNumber
包裹的追蹤編號。

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

### -DriveList
組成工作的磁片磁碟機清單。
若要建構，請參閱 DRIVELIST 屬性的附注區段，然後建立雜湊表。

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveStatus[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -LogLevel
指出是否已啟用錯誤記錄或詳細記錄。

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

### -名稱
匯進/匯出工作的名稱。

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: JobName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
資源組名可唯一識別使用者訂閱中的資源群組。

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReturnAddressCity
要用於退回磁片磁碟機的城市名稱。

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

### -ReturnAddressCountryOrRegion
退回磁片磁碟機時要使用的國家/地區或地區。

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

### -ReturnAddressEmail
所退回磁片磁碟機收件者的電子郵件地址。

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

### -ReturnAddressPhone
所退回磁片磁碟機收件者的電話號碼。

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

### -ReturnAddressPostalCode
退回磁片磁碟機時使用的郵遞區號。

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

### -ReturnAddressRecipientName
收到硬碟的收件者名稱。

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

### -ReturnAddressStateOrProvince
退回磁片磁碟機時所使用之省/市。

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

### -ReturnAddressStreetAddress1
退回磁片磁碟機時，所使用街地道號的第一行。

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

### -ReturnAddressStreetAddress2
退回磁片磁碟機時，所使用之街地道道的第二行。

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

### -ReturnShippingCarrierAccountNumber
客戶與電信公司的帳戶號碼。

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

### -ReturnShippingCarrierName
電信公司的名稱。

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

### -State
如果指定，值必須是出貨，這告訴匯進/匯出服務該工作的套件已出貨。
必須在此要求或之前的要求中設定 ReturnAddress 和 DeliveryPackage 屬性，否則要求將會失敗。

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
Azure 使用者的訂閱識別碼。

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -標記
指定要指派給工作的標記

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IUpdateJobParametersTags
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

### Microsoft.Azure.PowerShell.Cmdlets.ImportExport.models.IImportExportIdentity

## 輸出

### Microsoft.Azure.PowerShell.Cmdlets.ImportExport.models.Api20161101.IJobResponse

## 筆記

別名

複雜的參數屬性

若要建立下列描述的參數，請建構包含適當屬性的雜湊表。 有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。


DRIVELIST <IDriveStatus[]>：組成工作的磁片磁碟機清單。
  - `[BitLockerKey <String>]`：用來加密硬碟的 BitLocker 金鑰。
  - `[BytesSucceeded <Int64?>]`：已成功傳輸硬碟的位元組。
  - `[CopyStatus <String>]`：資料傳輸程式的詳細狀態。 在磁碟機位於傳輸狀態之前，此欄位不會在回應中返回。
  - `[DriveHeaderHash <String>]`：磁碟機頭雜湊值。
  - `[DriveId <String>]`：不含空格的硬碟硬體序號。
  - `[ErrorLogUri <String>]`：指向包含資料傳輸作業錯誤記錄之 Blob 的 URI。
  - `[ManifestFile <String>]`：磁碟機上之清單檔案的相對路徑。 
  - `[ManifestHash <String>]`：雲端硬碟上清單檔案的 Base16 編碼 MD5 雜湊。
  - `[ManifestUri <String>]`：指向包含磁碟機清單檔案之 Blob 的 URI。 
  - `[PercentComplete <Int32?>]`：完成磁碟機的百分比。 
  - `[State <DriveState?>]`：磁碟機的目前狀態。 
  - `[VerboseLogUri <String>]`：指向包含資料傳輸作業詳細記錄之 Blob 的 URI。 

INPUTOBJECT： <IImportExportIdentity> 身分識別參數
  - `[Id <String>]`：資源識別路徑
  - `[JobName <String>]`：匯進/匯出工作的名稱。
  - `[LocationName <String>]`：位置的名稱。 例如，美國西部或西部。
  - `[ResourceGroupName <String>]`：資源組名可唯一識別使用者訂閱中的資源群組。
  - `[SubscriptionId <String>]`：Azure 使用者的訂閱識別碼。

## 相關連結

