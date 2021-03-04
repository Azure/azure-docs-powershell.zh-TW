---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 910239BE-9E48-4DC5-85EA-CC6D466FE62F
online version: https://docs.microsoft.com/powershell/module/az.websites/new-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
ms.openlocfilehash: 3429868b1d603606f64c75ec23505cf63f9ade03
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914241"
---
# <span data-ttu-id="63d2d-101">New-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="63d2d-101">New-AzWebAppSSLBinding</span></span>

## <span data-ttu-id="63d2d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="63d2d-102">SYNOPSIS</span></span>
<span data-ttu-id="63d2d-103">為 Azure Web App 建立 SSL 憑證綁定。</span><span class="sxs-lookup"><span data-stu-id="63d2d-103">Creates an SSL certificate binding for an Azure Web App.</span></span>

## <span data-ttu-id="63d2d-104">語法</span><span class="sxs-lookup"><span data-stu-id="63d2d-104">SYNTAX</span></span>

### <span data-ttu-id="63d2d-105">S1</span><span class="sxs-lookup"><span data-stu-id="63d2d-105">S1</span></span>
```
New-AzWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>] [-Name] <String>
 [[-SslState] <SslState>] [-CertificateFilePath] <String> [-CertificatePassword] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63d2d-106">S2</span><span class="sxs-lookup"><span data-stu-id="63d2d-106">S2</span></span>
```
New-AzWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>] [-Name] <String>
 [[-SslState] <SslState>] [-Thumbprint] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="63d2d-107">S3</span><span class="sxs-lookup"><span data-stu-id="63d2d-107">S3</span></span>
```
New-AzWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>]
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="63d2d-108">S4</span><span class="sxs-lookup"><span data-stu-id="63d2d-108">S4</span></span>
```
New-AzWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63d2d-109">描述</span><span class="sxs-lookup"><span data-stu-id="63d2d-109">DESCRIPTION</span></span>
<span data-ttu-id="63d2d-110">**New-AzWebAppSSLBinding** Cmdlet 會為 Azure Web App 建立安全通訊端層 (SSL) 憑證綁定。</span><span class="sxs-lookup"><span data-stu-id="63d2d-110">The **New-AzWebAppSSLBinding** cmdlet creates a Secure Socket Layer (SSL) certificate binding for an Azure Web App.</span></span>
<span data-ttu-id="63d2d-111">Cmdlet 會以兩種方式建立 SSL 綁定：</span><span class="sxs-lookup"><span data-stu-id="63d2d-111">The cmdlet creates an SSL binding in two ways:</span></span> 
- <span data-ttu-id="63d2d-112">您可以將 Web App 綁定至現有的憑證。</span><span class="sxs-lookup"><span data-stu-id="63d2d-112">You can bind a Web App to an existing certificate.</span></span>
- <span data-ttu-id="63d2d-113">您可以上傳新憑證，然後將 Web App 綁定至此新憑證。</span><span class="sxs-lookup"><span data-stu-id="63d2d-113">You can upload a new certificate and then bind the Web App to this new certificate.</span></span>
<span data-ttu-id="63d2d-114">無論您使用哪種方法，憑證和 Web App 都必須與相同的 Azure 資源群組相關聯。</span><span class="sxs-lookup"><span data-stu-id="63d2d-114">Regardless of which approach you use, the certificate and the Web App must be associated with the same Azure resource group.</span></span>
<span data-ttu-id="63d2d-115">如果您在資源群組 A 中擁有 Web App，而且想要將 Web App 綁定至資源群組 B 中的憑證，唯一的方法就是將憑證的一份副本上傳到資源群組 A。如果您上傳新的憑證，請記住 Azure SSL 憑證的下列需求：</span><span class="sxs-lookup"><span data-stu-id="63d2d-115">If you have a Web App in Resource Group A and you want to bind that Web App to a certificate in Resource Group B, the only way to do that is to upload a copy of the certificate to Resource Group A. If you upload a new certificate, keep in mind the following requirements for an Azure SSL certificate:</span></span> 
- <span data-ttu-id="63d2d-116">憑證必須包含私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="63d2d-116">The certificate must contain a private key.</span></span> 
- <span data-ttu-id="63d2d-117">憑證必須使用個人資訊 Exchange (PFX) 格式。</span><span class="sxs-lookup"><span data-stu-id="63d2d-117">The certificate must use the Personal Information Exchange (PFX) format.</span></span> 
- <span data-ttu-id="63d2d-118">憑證的主體名稱必須與用來存取 Web App 的網域相符。</span><span class="sxs-lookup"><span data-stu-id="63d2d-118">The certificate's subject name must match the domain used to access the Web App.</span></span> 
- <span data-ttu-id="63d2d-119">憑證必須至少使用 2048 位加密。</span><span class="sxs-lookup"><span data-stu-id="63d2d-119">The certificate must use a minimum of 2048-bit encryption.</span></span>

## <span data-ttu-id="63d2d-120">例子</span><span class="sxs-lookup"><span data-stu-id="63d2d-120">EXAMPLES</span></span>

### <span data-ttu-id="63d2d-121">範例 1：將憑證綁定至 Web App</span><span class="sxs-lookup"><span data-stu-id="63d2d-121">Example 1: Bind a certificate to a Web App</span></span>
```powershell
PS C:\>New-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com"
```

<span data-ttu-id="63d2d-122">此命令會使用 Thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) 將現有的 (Azure 憑證) 與名為 ContosoWebApp 的憑證綁定。</span><span class="sxs-lookup"><span data-stu-id="63d2d-122">This command binds an existing Azure certificate (a certificate with the Thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) to the web app named ContosoWebApp.</span></span>

### <span data-ttu-id="63d2d-123">範例 2</span><span class="sxs-lookup"><span data-stu-id="63d2d-123">Example 2</span></span>

<span data-ttu-id="63d2d-124">為 Azure Web App 建立 SSL 憑證綁定。</span><span class="sxs-lookup"><span data-stu-id="63d2d-124">Creates an SSL certificate binding for an Azure Web App.</span></span> <span data-ttu-id="63d2d-125"> (自動) </span><span class="sxs-lookup"><span data-stu-id="63d2d-125">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzWebAppSSLBinding -Name 'www.contoso.com' -ResourceGroupName 'ContosoResourceGroup' -SslState Disabled -Thumbprint 'E3A38EBA60CAA1C162785A2E1C44A15AD450199C3' -WebAppName 'ContosoWebApp'
```

## <span data-ttu-id="63d2d-126">參數</span><span class="sxs-lookup"><span data-stu-id="63d2d-126">PARAMETERS</span></span>

### <span data-ttu-id="63d2d-127">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="63d2d-127">-CertificateFilePath</span></span>
<span data-ttu-id="63d2d-128">指定要上傳之憑證的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="63d2d-128">Specifies the file path for the certificate to be uploaded.</span></span>
<span data-ttu-id="63d2d-129">只有在憑證尚未上傳到 Azure 時，才需要 *CertificateFilePath* 參數。</span><span class="sxs-lookup"><span data-stu-id="63d2d-129">The *CertificateFilePath* parameter is only required if the certificate has not yet been uploaded to Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S3
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63d2d-130">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="63d2d-130">-CertificatePassword</span></span>
<span data-ttu-id="63d2d-131">指定憑證的解密密碼。</span><span class="sxs-lookup"><span data-stu-id="63d2d-131">Specifies the decryption password for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S3
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63d2d-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63d2d-132">-DefaultProfile</span></span>
<span data-ttu-id="63d2d-133">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="63d2d-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63d2d-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="63d2d-134">-Name</span></span>
<span data-ttu-id="63d2d-135">指定 Web App 的名稱。</span><span class="sxs-lookup"><span data-stu-id="63d2d-135">Specifies the name of the Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63d2d-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63d2d-136">-ResourceGroupName</span></span>
<span data-ttu-id="63d2d-137">指定憑證指派給的資源組名。</span><span class="sxs-lookup"><span data-stu-id="63d2d-137">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="63d2d-138">您無法在同一 *個命令中使用 ResourceGroupName* 參數和 *WebApp* 參數。</span><span class="sxs-lookup"><span data-stu-id="63d2d-138">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63d2d-139">-Slot</span><span class="sxs-lookup"><span data-stu-id="63d2d-139">-Slot</span></span>
<span data-ttu-id="63d2d-140">指定 Web App 部署時段的名稱。</span><span class="sxs-lookup"><span data-stu-id="63d2d-140">Specifies the name of the Web App deployment slot.</span></span>
<span data-ttu-id="63d2d-141">您可以使用 Cmdlet Get-AzWebAppSlot取得插槽。</span><span class="sxs-lookup"><span data-stu-id="63d2d-141">You can use the Get-AzWebAppSlot cmdlet to get a slot.</span></span>
<span data-ttu-id="63d2d-142">部署插槽提供一種方式，方便您進行階段和驗證 Web App，而不需要這些 App 可經由網際網路進行。</span><span class="sxs-lookup"><span data-stu-id="63d2d-142">Deployment slots provide a way for you to stage and validate web apps without those apps being accessible over the Internet.</span></span>
<span data-ttu-id="63d2d-143">一般來說，您將將變更部署到暫存網站、驗證這些變更，然後部署到可 (網際網路) 生產。</span><span class="sxs-lookup"><span data-stu-id="63d2d-143">Typically you will deploy your changes to a staging site, validate those changes, and then deploy to the production (Internet-accessible) site.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S2
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63d2d-144">-SslState</span><span class="sxs-lookup"><span data-stu-id="63d2d-144">-SslState</span></span>
<span data-ttu-id="63d2d-145">指定憑證是否已啟用。</span><span class="sxs-lookup"><span data-stu-id="63d2d-145">Specifies whether the certificate is enabled.</span></span>
<span data-ttu-id="63d2d-146">將 *SSLState* 參數設為 1 以啟用憑證，或將 *SSLState 設為* 0 以停用憑證。</span><span class="sxs-lookup"><span data-stu-id="63d2d-146">Set the *SSLState* parameter to 1 to enable the certificate, or set *SSLState* to 0 to disable the certificate.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.WebSites.Models.SslState]
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, SniEnabled, IpBasedEnabled

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63d2d-147">-拇指列印</span><span class="sxs-lookup"><span data-stu-id="63d2d-147">-Thumbprint</span></span>
<span data-ttu-id="63d2d-148">指定憑證的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="63d2d-148">Specifies the unique identifier for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: S2, S4
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63d2d-149">-WebApp</span><span class="sxs-lookup"><span data-stu-id="63d2d-149">-WebApp</span></span>
<span data-ttu-id="63d2d-150">指定 Web App。</span><span class="sxs-lookup"><span data-stu-id="63d2d-150">Specifies a Web App.</span></span>
<span data-ttu-id="63d2d-151">若要取得 Web App，請使用 Get-AzWebApp Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="63d2d-151">To get a Web App, use the Get-AzWebApp cmdlet.</span></span>
<span data-ttu-id="63d2d-152">您無法在 *ResourceGroupName* 參數和/或 *WebAppName* 的相同命令中，使用 WebApp 參數。 </span><span class="sxs-lookup"><span data-stu-id="63d2d-152">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S3, S4
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63d2d-153">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="63d2d-153">-WebAppName</span></span>
<span data-ttu-id="63d2d-154">指定要建立新 SSL 裝訂的 Web App 名稱。</span><span class="sxs-lookup"><span data-stu-id="63d2d-154">Specifies the name of the Web App for which the new SSL binding is being created.</span></span>
<span data-ttu-id="63d2d-155">您無法在同一個命令中使用 *WebAppName* 參數和 *WebApp* 參數。</span><span class="sxs-lookup"><span data-stu-id="63d2d-155">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S2
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63d2d-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63d2d-156">CommonParameters</span></span>
<span data-ttu-id="63d2d-157">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="63d2d-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63d2d-158">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="63d2d-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63d2d-159">輸入</span><span class="sxs-lookup"><span data-stu-id="63d2d-159">INPUTS</span></span>

### <span data-ttu-id="63d2d-160">Microsoft.Azure.Commands.WebApps.models.PSSite</span><span class="sxs-lookup"><span data-stu-id="63d2d-160">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="63d2d-161">輸出</span><span class="sxs-lookup"><span data-stu-id="63d2d-161">OUTPUTS</span></span>

### <span data-ttu-id="63d2d-162">Microsoft.Azure.management.Websites.models.HostNameSslState</span><span class="sxs-lookup"><span data-stu-id="63d2d-162">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span></span>

## <span data-ttu-id="63d2d-163">筆記</span><span class="sxs-lookup"><span data-stu-id="63d2d-163">NOTES</span></span>

## <span data-ttu-id="63d2d-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="63d2d-164">RELATED LINKS</span></span>

[<span data-ttu-id="63d2d-165">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="63d2d-165">Get-AzWebAppSSLBinding</span></span>](./Get-AzWebAppSSLBinding.md)

[<span data-ttu-id="63d2d-166">Remove-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="63d2d-166">Remove-AzWebAppSSLBinding</span></span>](./Remove-AzWebAppSSLBinding.md)

[<span data-ttu-id="63d2d-167">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="63d2d-167">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="63d2d-168">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="63d2d-168">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


