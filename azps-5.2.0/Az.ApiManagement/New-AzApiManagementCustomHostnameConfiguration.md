---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcustomhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCustomHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCustomHostnameConfiguration.md
ms.openlocfilehash: a5c619a88f9366699f37124eab5afb2302717762
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98284155"
---
# <span data-ttu-id="2746b-101">New-AzApiManagementCustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="2746b-101">New-AzApiManagementCustomHostnameConfiguration</span></span>

## <span data-ttu-id="2746b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2746b-102">SYNOPSIS</span></span>
<span data-ttu-id="2746b-103">建立的實例 `PsApiManagementCustomHostNameConfiguration` 。</span><span class="sxs-lookup"><span data-stu-id="2746b-103">Creates an instance of `PsApiManagementCustomHostNameConfiguration`.</span></span>

## <span data-ttu-id="2746b-104">句法</span><span class="sxs-lookup"><span data-stu-id="2746b-104">SYNTAX</span></span>

### <span data-ttu-id="2746b-105">NoChangeCertificate (預設) </span><span class="sxs-lookup"><span data-stu-id="2746b-105">NoChangeCertificate (Default)</span></span>
```
New-AzApiManagementCustomHostnameConfiguration -Hostname <String> -HostnameType <PsApiManagementHostnameType>
 -HostNameCertificateInformation <PsApiManagementCertificateInformation> [-DefaultSslBinding]
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2746b-106">SslCertificateFromFile</span><span class="sxs-lookup"><span data-stu-id="2746b-106">SslCertificateFromFile</span></span>
```
New-AzApiManagementCustomHostnameConfiguration -Hostname <String> -HostnameType <PsApiManagementHostnameType>
 -PfxPath <String> [-PfxPassword <SecureString>] [-DefaultSslBinding] [-NegotiateClientCertificate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2746b-107">SslCertificateFromKeyVault</span><span class="sxs-lookup"><span data-stu-id="2746b-107">SslCertificateFromKeyVault</span></span>
```
New-AzApiManagementCustomHostnameConfiguration -Hostname <String> -HostnameType <PsApiManagementHostnameType>
 -KeyVaultId <String> [-DefaultSslBinding] [-NegotiateClientCertificate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2746b-108">說明</span><span class="sxs-lookup"><span data-stu-id="2746b-108">DESCRIPTION</span></span>
<span data-ttu-id="2746b-109">**新的 AzApiManagementCustomHostnameConfiguration** Cmdlet 是一個協助程式命令，可建立 **PsApiManagementCustomHostNameConfiguration** 的實例。</span><span class="sxs-lookup"><span data-stu-id="2746b-109">The **New-AzApiManagementCustomHostnameConfiguration** cmdlet is a helper command that creates an instance of **PsApiManagementCustomHostNameConfiguration**.</span></span>
<span data-ttu-id="2746b-110">此命令與 New-AzApiManagement 和 Set-AzApiManagement Cmdlet 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="2746b-110">This command is used with the New-AzApiManagement and Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="2746b-111">示例</span><span class="sxs-lookup"><span data-stu-id="2746b-111">EXAMPLES</span></span>

### <span data-ttu-id="2746b-112">範例1：使用來自檔案的 Ssl 憑證來建立和初始化 PsApiManagementCustomHostNameConfiguration 的實例</span><span class="sxs-lookup"><span data-stu-id="2746b-112">Example 1: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Ssl Certificate from file</span></span>
```powershell
PS C:\>$portal = New-AzApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -PfxPath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111" -DefaultSslBinding
PS C:\>$customConfig = @($portal)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -CustomHostnameConfiguration $customConfig
```

<span data-ttu-id="2746b-113">這個命令會為入口網站建立並初始化 **PsApiManagementCustomHostNameConfiguration** 的實例。</span><span class="sxs-lookup"><span data-stu-id="2746b-113">This command creates and initializes an instance of **PsApiManagementCustomHostNameConfiguration** for Portal.</span></span> <span data-ttu-id="2746b-114">接著，它會使用自訂主機名稱設定來建立新的 ApiManagement 服務。</span><span class="sxs-lookup"><span data-stu-id="2746b-114">Then it creates a new ApiManagement service with custom hostname configuration.</span></span>

### <span data-ttu-id="2746b-115">範例2：使用 KeyVault 資源中的秘密來建立和初始化 PsApiManagementCustomHostNameConfiguration 的實例</span><span class="sxs-lookup"><span data-stu-id="2746b-115">Example 2: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Secret from KeyVault Resource</span></span>
```powershell
PS C:\>$portal = New-AzApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/api-portal-custom-ssl.pfx"

PS C:\>$customConfig = @($portal)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -CustomHostnameConfiguration $customConfig -SystemAssignedIdentity
```

<span data-ttu-id="2746b-116">這個命令會建立並初始化 **PsApiManagementCustomHostNameConfiguration** 的實例。</span><span class="sxs-lookup"><span data-stu-id="2746b-116">This command creates and initializes an instance of **PsApiManagementCustomHostNameConfiguration**.</span></span>

## <span data-ttu-id="2746b-117">參數</span><span class="sxs-lookup"><span data-stu-id="2746b-117">PARAMETERS</span></span>

### <span data-ttu-id="2746b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2746b-118">-DefaultProfile</span></span>
<span data-ttu-id="2746b-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2746b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2746b-120">-DefaultSslBinding</span><span class="sxs-lookup"><span data-stu-id="2746b-120">-DefaultSslBinding</span></span>
<span data-ttu-id="2746b-121">判斷值是否為秘密，且應該加密。</span><span class="sxs-lookup"><span data-stu-id="2746b-121">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="2746b-122">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="2746b-122">This parameter is optional.</span></span>
<span data-ttu-id="2746b-123">預設值為 false。</span><span class="sxs-lookup"><span data-stu-id="2746b-123">Default Value is false.</span></span>

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

### <span data-ttu-id="2746b-124">-Hostname</span><span class="sxs-lookup"><span data-stu-id="2746b-124">-Hostname</span></span>
<span data-ttu-id="2746b-125">自訂主機名稱</span><span class="sxs-lookup"><span data-stu-id="2746b-125">Custom Hostname</span></span>

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

### <span data-ttu-id="2746b-126">-HostNameCertificateInformation</span><span class="sxs-lookup"><span data-stu-id="2746b-126">-HostNameCertificateInformation</span></span>
<span data-ttu-id="2746b-127">現有的憑證配置。</span><span class="sxs-lookup"><span data-stu-id="2746b-127">Existing Certificate Configuration.</span></span>

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

### <span data-ttu-id="2746b-128">-HostnameType</span><span class="sxs-lookup"><span data-stu-id="2746b-128">-HostnameType</span></span>
<span data-ttu-id="2746b-129">Hostname 類型</span><span class="sxs-lookup"><span data-stu-id="2746b-129">Hostname Type</span></span>

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

### <span data-ttu-id="2746b-130">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="2746b-130">-KeyVaultId</span></span>
<span data-ttu-id="2746b-131">KeyVaultId 至儲存自訂 SSL 憑證的秘密。</span><span class="sxs-lookup"><span data-stu-id="2746b-131">KeyVaultId to the secret storing the Custom SSL Certificate.</span></span>

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

### <span data-ttu-id="2746b-132">-NegotiateClientCertificate</span><span class="sxs-lookup"><span data-stu-id="2746b-132">-NegotiateClientCertificate</span></span>
<span data-ttu-id="2746b-133">判斷值是否為秘密，且應該加密。</span><span class="sxs-lookup"><span data-stu-id="2746b-133">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="2746b-134">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="2746b-134">This parameter is optional.</span></span>
<span data-ttu-id="2746b-135">預設值為 false。</span><span class="sxs-lookup"><span data-stu-id="2746b-135">Default Value is false.</span></span>

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

### <span data-ttu-id="2746b-136">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="2746b-136">-PfxPassword</span></span>
<span data-ttu-id="2746b-137">.Pfx 憑證檔案的密碼。</span><span class="sxs-lookup"><span data-stu-id="2746b-137">Password for the .pfx certificate file.</span></span>

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

### <span data-ttu-id="2746b-138">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="2746b-138">-PfxPath</span></span>
<span data-ttu-id="2746b-139">.Pfx 憑證檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="2746b-139">Path to a .pfx certificate file.</span></span>

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

### <span data-ttu-id="2746b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2746b-140">CommonParameters</span></span>
<span data-ttu-id="2746b-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2746b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2746b-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2746b-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2746b-143">輸入</span><span class="sxs-lookup"><span data-stu-id="2746b-143">INPUTS</span></span>

### <span data-ttu-id="2746b-144">PsApiManagementCertificateInformation 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="2746b-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCertificateInformation</span></span>

## <span data-ttu-id="2746b-145">輸出</span><span class="sxs-lookup"><span data-stu-id="2746b-145">OUTPUTS</span></span>

### <span data-ttu-id="2746b-146">PsApiManagementCustomHostNameConfiguration 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="2746b-146">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration</span></span>

## <span data-ttu-id="2746b-147">筆記</span><span class="sxs-lookup"><span data-stu-id="2746b-147">NOTES</span></span>

## <span data-ttu-id="2746b-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="2746b-148">RELATED LINKS</span></span>

[<span data-ttu-id="2746b-149">新-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="2746b-149">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="2746b-150">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="2746b-150">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)