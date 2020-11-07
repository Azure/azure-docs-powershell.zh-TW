---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 03EAFFB2-EA64-4227-A33B-D24EB4A75F71
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac88bc2494bad975c6169262edd05c7b821061bb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967842"
---
# Add-AzureAccount

## 摘要
將 Azure 帳戶新增至 Windows PowerShell。

## 句法

### 使用者 (預設) 
```
Add-AzureAccount [-Environment <String>] [-Credential <PSCredential>] [-Tenant <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ServicePrincipal
```
Add-AzureAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
**AzureAccount** Cmdlet 會使您的 Azure 帳戶及其訂閱可在 Windows PowerShell 中使用。
就像是在 Windows PowerShell 中登入您的 Azure 帳戶一樣。
若要登出帳戶，請使用 **AzureAccount** Cmdlet。

**載入 AzureAccount** 下載 Azure 帳戶的相關資訊，並將它儲存在您的漫遊使用者設定檔的訂閱資料檔中。
它也會取得允許 Windows PowerShell 代表您存取 Azure 帳戶的存取權杖。
當命令完成時，您可以在 Windows PowerShell 中管理您的 Azure 帳戶。

您可以透過兩種不同的方式，讓您的 Azure 帳戶可供 Windows PowerShell 使用。
您可以使用 **AzureAccount** Cmdlet，使用 Azure Active Directory (azure AD) 驗證存取權杖，或使用管理憑證的匯 **入-AzurePublishSettingsFile** 。
如需使用何種方法的指導方針，請參閱 [如何：連線至您的訂閱](https://azure.microsoft.com/documentation/articles/install-configure-powershell) (https://azure.microsoft.com/documentation/articles/install-configure-powershell/#Connect) 。

當您執行 [ **載入 AzureAccount** ] 時，會顯示互動式視窗，提示您登入您的 Azure 帳戶。
此登入一直有效，直到存取權杖到期為止。
當它到期時，需要存取您帳戶的 Cmdlet 會提示您再次執行 **AzureAccount 附加程式** 。

本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。
若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。

## 示例

### 範例1：新增帳戶
```
PS C:\> Add-AzureAccount
```

這個命令會將 Azure 帳戶新增至 Windows PowerShell。
當您執行命令時，windows 會彈出來要求帳戶的使用者名稱和密碼。

### 範例2：使用替代訂閱資料檔案
```
PS C:\> Add-AzureAccount -SubscriptionDataFile C:\Testing\SDF.xml
```

這個命令使用 **SubscriptionDataFile** 參數來直接 **AzureAccount 將** 帳戶資料儲存在 C:\Testing\SDF.xml 檔案中，而不是預設檔案。

## 參數

### -認證
```yaml
Type: PSCredential
Parameter Sets: User
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: PSCredential
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -環境
指定 Azure 環境。

Azure 環境是獨立部署的 Microsoft Azure，例如針對全域 Azure 的 AzureCloud，以及由中國由世紀運營之 AzureChinaCloud 的 Azure。
您也可以使用 Azure Pack 和 WAPack Cmdlet，建立內部部署的 Azure 環境。
如需詳細資訊，請參閱 [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) 。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -設定檔
指定此 Cmdlet 讀取的 Azure 設定檔。 如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServicePrincipal
```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -租使用者
```yaml
Type: String
Parameter Sets: User
Aliases: TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServicePrincipal
Aliases: TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有
您無法將輸入管到這個 Cmdlet

## 輸出

### 所有
這個 Cmdlet 不會傳回任何輸出。

## 筆記
* **載入 AzureAccount** (和 Azure AD 驗證方法) 優先于 **Import AzurePublishSettings** (且管理憑證方法) 。 如果您在帳戶上使用 **Add-AzureAccount** ，則會使用 Azure AD 驗證方法，且系統會忽略管理憑證。 若要移除 Azure AD 權杖並還原管理證書方法，請使用 **AzureAccount** Cmdlet。 如需詳細資訊，請輸入： **Get-help 移除-AzureAccount** 。
* 錯誤，"您的認證已過期。 請使用 Add-AzureAccount 再次登入。」 表示您的存取權杖已過期，且 Windows PowerShell 無法存取您的 Azure 帳戶。 若要還原您帳戶的存取權，請再次執行 [ **載入 AzureAccount** ]。
* Azure PowerShell 帳戶和訂閱 Cmdlet 會從訂閱資料檔案取得資料，而不是從實際的 Azure 帳戶取得。 如果您在 Windows PowerShell 之外變更您的帳戶或訂閱（例如使用 Azure 管理入口網站），請再次執行 [ **載入 AzureAccount** ] 以重新整理訂閱資料檔案。

## 相關連結

[附加 AzureEnvironment](./Add-AzureEnvironment.md)

[AzureEnvironment](./Get-AzureEnvironment.md)

[匯入-AzurePublishSettingsFile](./Import-AzurePublishSettingsFile.md)

[AzureAccount](./Get-AzureAccount.md)

[移除-AzureAccount](./Remove-AzureAccount.md)


