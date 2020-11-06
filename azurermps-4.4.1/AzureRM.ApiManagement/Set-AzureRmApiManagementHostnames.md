---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F9CE8705-F7B1-45AB-98BC-FC6DC023D38D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementHostnames.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementHostnames.md
ms.openlocfilehash: 3e3fea3e43f2370347ae819604d6caf1e830ebd4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450935"
---
# Set-AzureRmApiManagementHostnames

## 摘要
針對 API 管理服務 proxy 或入口網站設定自訂主機名稱的配置。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### 特定 API 管理服務 (預設) 
```
Set-AzureRmApiManagementHostnames -ResourceGroupName <String> -Name <String>
 [-PortalHostnameConfiguration <PsApiManagementHostnameConfiguration>]
 [-ProxyHostnameConfiguration <PsApiManagementHostnameConfiguration>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### 從提供的 PsApiManagement 實例設定
```
Set-AzureRmApiManagementHostnames -ApiManagement <PsApiManagement> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
AzureRmApiManagementHostnames Cmdlet 會將自訂主機名稱 **設定** 套用至 API 管理服務 proxy 或入口網站。

## 示例

### 範例1：設定 proxy 與入口網站的自訂主機名稱配置
```
PS C:\>Set-AzureRmApiManagementHostnames -Name ContosoApi -ResourceGroupName Contoso -PortalHostnameConfiguration $portalHostnameConf -ProxyHostnameConfiguration $proxyHostnameConf
```

這個命令會設定 proxy 與入口網站的自訂主機名稱配置。

### 範例2：設定 proxy 與入口網站的自訂主機名稱
```
PS C:\>Import-AzureRmApiManagementHostnameCertificate -Name ContosoApi -ResourceGroupName "Contoso" -HostnameType "Proxy" -PfxPath "C:\proxycert.pfx" -PfxPassword "CertSecret"
PS C:\> Import-AzureRmApiManagementHostnameCertificate -Name "ContosoApi" -ResourceGroupName "Contoso" -HostnameType "Portal" -PfxPath "C:\portalcert.pfx" -PfxPassword "CertSecret"
PS C:\> $PortalHostnameConf = New-AzureRmApiManagementHostnameConfiguration -Hostname "portal.contoso.com" -CertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C"
PS C:\> $ProxyHostnameConf = New-AzureRmApiManagementHostnameConfiguration -Hostname "proxy.contoso.com" -CertificateThumbprint "5DD7CCF6A1E74E0987DD2873406B7264"
PS C:\> Set-AzureRmApiManagementHostnames -Name "ContosoApi" -ResourceGroupName "Contoso" -PortalHostnameConfiguration $PortalHostnameConf -ProxyHostnameConfiguration $ProxyHostnameConf
```

這個範例會設定 proxy 與入口網站的自訂主機名稱。
您必須匯入對應的憑證，然後套用自訂的主機名稱。

## 參數

### -ApiManagement
指定此 Cmdlet 取得 *PortalHostnameConfiguration* 和 *ProxyHostnameConfiguration* 參數的 **PsApiManagement** 實例。

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: Set from provided PsApiManagement instance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -名稱
指定 API 管理實例的名稱。

```yaml
Type: System.String
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
傳回代表您正在使用之專案的物件。
根據預設，這個 Cmdlet 不會產生任何輸出。

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

### -PortalHostnameConfiguration
指定自訂入口網站主機名稱的配置。
將 $null 傳遞到 Cmdlet 會設定預設的主機名稱。

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameConfiguration
Parameter Sets: Specific API Management service
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProxyHostnameConfiguration
指定自訂 proxy 主機名稱的配置。
傳遞 $null 會設定預設的主機名稱。

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameConfiguration
Parameter Sets: Specific API Management service
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定 API 管理實例所在之資源群組的名稱。

```yaml
Type: System.String
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### PsApiManagement
形參 "ApiManagement" 接受管線中 "PsApiManagement" 類型的值

## 輸出

### PsApiManagement 中的 ApiManagement。

## 筆記

## 相關連結

[匯入-AzureRmApiManagementHostnameCertificate](./Import-AzureRmApiManagementHostnameCertificate.md)

[新-AzureRmApiManagementHostnameConfiguration](./New-AzureRmApiManagementHostnameConfiguration.md)


