---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementcustomhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCustomHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCustomHostnameConfiguration.md
ms.openlocfilehash: e2f7ca5ac27faa3730742f77495b6b21ac084553
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902158"
---
# <span data-ttu-id="ec6e5-101">New-AzApiManagementCustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="ec6e5-101">New-AzApiManagementCustomHostnameConfiguration</span></span>

## <span data-ttu-id="ec6e5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ec6e5-102">SYNOPSIS</span></span>
<span data-ttu-id="ec6e5-103">會建立一個 `PsApiManagementCustomHostNameConfiguration` .</span><span class="sxs-lookup"><span data-stu-id="ec6e5-103">Creates an instance of `PsApiManagementCustomHostNameConfiguration`.</span></span>

## <span data-ttu-id="ec6e5-104">語法</span><span class="sxs-lookup"><span data-stu-id="ec6e5-104">SYNTAX</span></span>

### <span data-ttu-id="ec6e5-105">NoChangeCertificate (預設) </span><span class="sxs-lookup"><span data-stu-id="ec6e5-105">NoChangeCertificate (Default)</span></span>
```
New-AzApiManagementCustomHostnameConfiguration -Hostname <String> -HostnameType <PsApiManagementHostnameType>
 -HostNameCertificateInformation <PsApiManagementCertificateInformation> [-DefaultSslBinding]
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec6e5-106">SslCertificateFromFile</span><span class="sxs-lookup"><span data-stu-id="ec6e5-106">SslCertificateFromFile</span></span>
```
New-AzApiManagementCustomHostnameConfiguration -Hostname <String> -HostnameType <PsApiManagementHostnameType>
 -PfxPath <String> [-PfxPassword <SecureString>] [-DefaultSslBinding] [-NegotiateClientCertificate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec6e5-107">SslCertificateFromKeyVault</span><span class="sxs-lookup"><span data-stu-id="ec6e5-107">SslCertificateFromKeyVault</span></span>
```
New-AzApiManagementCustomHostnameConfiguration -Hostname <String> -HostnameType <PsApiManagementHostnameType>
 -KeyVaultId <String> [-DefaultSslBinding] [-NegotiateClientCertificate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec6e5-108">描述</span><span class="sxs-lookup"><span data-stu-id="ec6e5-108">DESCRIPTION</span></span>
<span data-ttu-id="ec6e5-109">**New-AzApiManagementCustomHostnameConfiguration** Cmdlet 是建立 **PsApiManagementCustomHostNameConfiguration** 實例的協助程式命令。</span><span class="sxs-lookup"><span data-stu-id="ec6e5-109">The **New-AzApiManagementCustomHostnameConfiguration** cmdlet is a helper command that creates an instance of **PsApiManagementCustomHostNameConfiguration**.</span></span>
<span data-ttu-id="ec6e5-110">此命令會與 New-AzApiManagement 和 Set-AzApiManagement 一起使用。</span><span class="sxs-lookup"><span data-stu-id="ec6e5-110">This command is used with the New-AzApiManagement and Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="ec6e5-111">例子</span><span class="sxs-lookup"><span data-stu-id="ec6e5-111">EXAMPLES</span></span>

### <span data-ttu-id="ec6e5-112">範例 1：使用檔案的 Ssl 憑證建立 PsApiManagementCustomHostNameConfiguration 實例並初始化</span><span class="sxs-lookup"><span data-stu-id="ec6e5-112">Example 1: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Ssl Certificate from file</span></span>
```powershell
PS C:\>$portal = New-AzApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -PfxPath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111" -DefaultSslBinding
PS C:\>$customConfig = @($portal)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -CustomHostnameConfiguration $customConfig
```

<span data-ttu-id="ec6e5-113">此命令會建立並初始化入口網站 **PsApiManagementCustomHostNameConfiguration** 的實例。</span><span class="sxs-lookup"><span data-stu-id="ec6e5-113">This command creates and initializes an instance of **PsApiManagementCustomHostNameConfiguration** for Portal.</span></span> <span data-ttu-id="ec6e5-114">接著，它會使用自訂 hostname 設定檔來建立新的 ApiManagement 服務。</span><span class="sxs-lookup"><span data-stu-id="ec6e5-114">Then it creates a new ApiManagement service with custom hostname configuration.</span></span>

### <span data-ttu-id="ec6e5-115">範例 2：使用 KeyVault Resource 的機密建立和初始化 PsApiManagementCustomHostNameConfiguration 的實例</span><span class="sxs-lookup"><span data-stu-id="ec6e5-115">Example 2: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Secret from KeyVault Resource</span></span>
```powershell
PS C:\>$portal = New-AzApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/api-portal-custom-ssl.pfx"

PS C:\>$customConfig = @($portal)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -CustomHostnameConfiguration $customConfig -SystemAssignedIdentity
```

<span data-ttu-id="ec6e5-116">此命令會建立並初始化 **PsApiManagementCustomHostNameConfiguration 的實例**。</span><span class="sxs-lookup"><span data-stu-id="ec6e5-116">This command creates and initializes an instance of **PsApiManagementCustomHostNameConfiguration**.</span></span>

## <span data-ttu-id="ec6e5-117">參數</span><span class="sxs-lookup"><span data-stu-id="ec6e5-117">PARAMETERS</span></span>

### <span data-ttu-id="ec6e5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec6e5-118">-DefaultProfile</span></span>
<span data-ttu-id="ec6e5-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ec6e5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec6e5-120">-DefaultSslBinding</span><span class="sxs-lookup"><span data-stu-id="ec6e5-120">-DefaultSslBinding</span></span>
<span data-ttu-id="ec6e5-121">判斷值是否為機密，是否應該加密。</span><span class="sxs-lookup"><span data-stu-id="ec6e5-121">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="ec6e5-122">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="ec6e5-122">This parameter is optional.</span></span>
<span data-ttu-id="ec6e5-123">預設值為 False。</span><span class="sxs-lookup"><span data-stu-id="ec6e5-123">Default Value is false.</span></span>

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

### <span data-ttu-id="ec6e5-124">-Hostname</span><span class="sxs-lookup"><span data-stu-id="ec6e5-124">-Hostname</span></span>
<span data-ttu-id="ec6e5-125">自訂主機名稱</span><span class="sxs-lookup"><span data-stu-id="ec6e5-125">Custom Hostname</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec6e5-126">-HostNameCertificateInformation</span><span class="sxs-lookup"><span data-stu-id="ec6e5-126">-HostNameCertificateInformation</span></span>
<span data-ttu-id="ec6e5-127">現有憑證組配置。</span><span class="sxs-lookup"><span data-stu-id="ec6e5-127">Existing Certificate Configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCertificateInformation
Parameter Sets: NoChangeCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec6e5-128">-HostnameType</span><span class="sxs-lookup"><span data-stu-id="ec6e5-128">-HostnameType</span></span>
<span data-ttu-id="ec6e5-129">Hostname 類型</span><span class="sxs-lookup"><span data-stu-id="ec6e5-129">Hostname Type</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameType
Parameter Sets: (All)
Aliases:
Accepted values: Proxy, Portal, Management, Scm, DeveloperPortal

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec6e5-130">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="ec6e5-130">-KeyVaultId</span></span>
<span data-ttu-id="ec6e5-131">KeyVaultId to the secret stor the Custom SSL Certificate.</span><span class="sxs-lookup"><span data-stu-id="ec6e5-131">KeyVaultId to the secret storing the Custom SSL Certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: SslCertificateFromKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec6e5-132">-NegotiateClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ec6e5-132">-NegotiateClientCertificate</span></span>
<span data-ttu-id="ec6e5-133">判斷值是否為機密，是否應該加密。</span><span class="sxs-lookup"><span data-stu-id="ec6e5-133">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="ec6e5-134">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="ec6e5-134">This parameter is optional.</span></span>
<span data-ttu-id="ec6e5-135">預設值為 False。</span><span class="sxs-lookup"><span data-stu-id="ec6e5-135">Default Value is false.</span></span>

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

### <span data-ttu-id="ec6e5-136">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="ec6e5-136">-PfxPassword</span></span>
<span data-ttu-id="ec6e5-137">.pfx 憑證檔案的密碼。</span><span class="sxs-lookup"><span data-stu-id="ec6e5-137">Password for the .pfx certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: SslCertificateFromFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec6e5-138">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="ec6e5-138">-PfxPath</span></span>
<span data-ttu-id="ec6e5-139">.pfx 憑證檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="ec6e5-139">Path to a .pfx certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: SslCertificateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec6e5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec6e5-140">CommonParameters</span></span>
<span data-ttu-id="ec6e5-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ec6e5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec6e5-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ec6e5-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec6e5-143">輸入</span><span class="sxs-lookup"><span data-stu-id="ec6e5-143">INPUTS</span></span>

### <span data-ttu-id="ec6e5-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCertificateInformation</span><span class="sxs-lookup"><span data-stu-id="ec6e5-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCertificateInformation</span></span>

## <span data-ttu-id="ec6e5-145">輸出</span><span class="sxs-lookup"><span data-stu-id="ec6e5-145">OUTPUTS</span></span>

### <span data-ttu-id="ec6e5-146">Microsoft.Azure.Commands.ApiManagement.models.PsApiManagementCustomHostNameConfiguration</span><span class="sxs-lookup"><span data-stu-id="ec6e5-146">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration</span></span>

## <span data-ttu-id="ec6e5-147">筆記</span><span class="sxs-lookup"><span data-stu-id="ec6e5-147">NOTES</span></span>

## <span data-ttu-id="ec6e5-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="ec6e5-148">RELATED LINKS</span></span>

[<span data-ttu-id="ec6e5-149">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="ec6e5-149">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="ec6e5-150">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="ec6e5-150">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)