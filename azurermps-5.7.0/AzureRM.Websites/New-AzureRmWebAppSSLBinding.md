---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 910239BE-9E48-4DC5-85EA-CC6D466FE62F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSSLBinding.md
ms.openlocfilehash: d3971c2838b3fed04e1aa38d96e2cd27b2e8276e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452939"
---
# <span data-ttu-id="efda5-101">New-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="efda5-101">New-AzureRmWebAppSSLBinding</span></span>

## <span data-ttu-id="efda5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="efda5-102">SYNOPSIS</span></span>
<span data-ttu-id="efda5-103">針對 Azure Web App 建立 SSL 憑證系結。</span><span class="sxs-lookup"><span data-stu-id="efda5-103">Creates an SSL certificate binding for an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="efda5-104">句法</span><span class="sxs-lookup"><span data-stu-id="efda5-104">SYNTAX</span></span>

### <span data-ttu-id="efda5-105">S1</span><span class="sxs-lookup"><span data-stu-id="efda5-105">S1</span></span>
```
New-AzureRmWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-Name] <String> [[-SslState] <SslState>] [-CertificateFilePath] <String> [-CertificatePassword] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="efda5-106">S2</span><span class="sxs-lookup"><span data-stu-id="efda5-106">S2</span></span>
```
New-AzureRmWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="efda5-107">S3</span><span class="sxs-lookup"><span data-stu-id="efda5-107">S3</span></span>
```
New-AzureRmWebAppSSLBinding [-WebApp] <Site> [-Name] <String> [[-SslState] <SslState>]
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="efda5-108">喚醒</span><span class="sxs-lookup"><span data-stu-id="efda5-108">S4</span></span>
```
New-AzureRmWebAppSSLBinding [-WebApp] <Site> [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="efda5-109">說明</span><span class="sxs-lookup"><span data-stu-id="efda5-109">DESCRIPTION</span></span>
<span data-ttu-id="efda5-110">**新的-AzureRmWebAppSSLBinding** Cmdlet 會針對 Azure Web APP (SSL) 憑證系結建立安全通訊端層。</span><span class="sxs-lookup"><span data-stu-id="efda5-110">The **New-AzureRmWebAppSSLBinding** cmdlet creates a Secure Socket Layer (SSL) certificate binding for an Azure Web App.</span></span>
<span data-ttu-id="efda5-111">這個 Cmdlet 以兩種方式建立 SSL 系結：</span><span class="sxs-lookup"><span data-stu-id="efda5-111">The cmdlet creates an SSL binding in two ways:</span></span> 

- <span data-ttu-id="efda5-112">您可以將 Web 應用程式系結到現有的憑證。</span><span class="sxs-lookup"><span data-stu-id="efda5-112">You can bind a Web App to an existing certificate.</span></span>
- <span data-ttu-id="efda5-113">您可以上傳新的憑證，然後將 Web App 系結到這個新的憑證。</span><span class="sxs-lookup"><span data-stu-id="efda5-113">You can upload a new certificate and then bind the Web App to this new certificate.</span></span>

<span data-ttu-id="efda5-114">無論您使用何種方法，證書和 Web 應用程式必須與相同的 Azure 資源群組相關聯。</span><span class="sxs-lookup"><span data-stu-id="efda5-114">Regardless of which approach you use, the certificate and the Web App must be associated with the same Azure resource group.</span></span>
<span data-ttu-id="efda5-115">如果您在 [資源群組 A] 中有 Web 應用程式，而您想要將該 Web App 系結至資源群組 B 中的憑證，唯一的方法就是將憑證複本上傳至資源群組 A。</span><span class="sxs-lookup"><span data-stu-id="efda5-115">If you have a Web App in Resource Group A and you want to bind that Web App to a certificate in Resource Group B, the only way to do that is to upload a copy of the certificate to Resource Group A.</span></span>

<span data-ttu-id="efda5-116">如果您上傳新的憑證，請記住 Azure SSL 憑證的下列需求：</span><span class="sxs-lookup"><span data-stu-id="efda5-116">If you upload a new certificate, keep in mind the following requirements for an Azure SSL certificate:</span></span> 

- <span data-ttu-id="efda5-117">憑證必須包含私用金鑰。</span><span class="sxs-lookup"><span data-stu-id="efda5-117">The certificate must contain a private key.</span></span> 
- <span data-ttu-id="efda5-118">憑證必須使用個人資訊交換 (PFX) 格式。</span><span class="sxs-lookup"><span data-stu-id="efda5-118">The certificate must use the Personal Information Exchange (PFX) format.</span></span> 
- <span data-ttu-id="efda5-119">憑證的受領人名稱必須與用來存取 Web 應用程式的網域相符。</span><span class="sxs-lookup"><span data-stu-id="efda5-119">The certificate's subject name must match the domain used to access the Web App.</span></span> 
- <span data-ttu-id="efda5-120">憑證必須使用最低的2048位加密。</span><span class="sxs-lookup"><span data-stu-id="efda5-120">The certificate must use a minimum of 2048-bit encryption.</span></span>

## <span data-ttu-id="efda5-121">示例</span><span class="sxs-lookup"><span data-stu-id="efda5-121">EXAMPLES</span></span>

### <span data-ttu-id="efda5-122">範例1：將憑證系結到 Web App</span><span class="sxs-lookup"><span data-stu-id="efda5-122">Example 1: Bind a certificate to a Web App</span></span>
```
PS C:\>New-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com"
```

<span data-ttu-id="efda5-123">這個命令會將現有的 Azure 憑證 (與指紋 E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) 的憑證系結到名為 ContosoWebApp 的 web app。</span><span class="sxs-lookup"><span data-stu-id="efda5-123">This command binds an existing Azure certificate (a certificate with the Thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) to the web app named ContosoWebApp.</span></span>

## <span data-ttu-id="efda5-124">參數</span><span class="sxs-lookup"><span data-stu-id="efda5-124">PARAMETERS</span></span>

### <span data-ttu-id="efda5-125">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="efda5-125">-CertificateFilePath</span></span>
<span data-ttu-id="efda5-126">指定要上傳之憑證的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="efda5-126">Specifies the file path for the certificate to be uploaded.</span></span>

<span data-ttu-id="efda5-127">只有證書尚未上傳到 Azure 時，才需要 *CertificateFilePath* 參數。</span><span class="sxs-lookup"><span data-stu-id="efda5-127">The *CertificateFilePath* parameter is only required if the certificate has not yet been uploaded to Azure.</span></span>

```yaml
Type: String
Parameter Sets: S1, S3
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efda5-128">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="efda5-128">-CertificatePassword</span></span>
<span data-ttu-id="efda5-129">指定憑證的解密密碼。</span><span class="sxs-lookup"><span data-stu-id="efda5-129">Specifies the decryption password for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: S1, S3
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efda5-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efda5-130">-DefaultProfile</span></span>
<span data-ttu-id="efda5-131">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="efda5-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efda5-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="efda5-132">-Name</span></span>
<span data-ttu-id="efda5-133">指定 Web 應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="efda5-133">Specifies the name of the Web App.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efda5-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efda5-134">-ResourceGroupName</span></span>
<span data-ttu-id="efda5-135">指定指派憑證的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="efda5-135">Specifies the name of the resource group that the certificate is assigned to.</span></span>

<span data-ttu-id="efda5-136">您無法在同一命令中使用 *ResourceGroupName* 參數和 *WebApp* 參數。</span><span class="sxs-lookup"><span data-stu-id="efda5-136">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: S1, S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efda5-137">-槽</span><span class="sxs-lookup"><span data-stu-id="efda5-137">-Slot</span></span>
<span data-ttu-id="efda5-138">指定 Web 應用程式部署槽的名稱。</span><span class="sxs-lookup"><span data-stu-id="efda5-138">Specifies the name of the Web App deployment slot.</span></span>
<span data-ttu-id="efda5-139">您可以使用 Get-AzureRMWebAppSlot Cmdlet 來取得槽。</span><span class="sxs-lookup"><span data-stu-id="efda5-139">You can use the Get-AzureRMWebAppSlot cmdlet to get a slot.</span></span>

<span data-ttu-id="efda5-140">部署槽提供一種方法，讓您可以暫存並驗證 web 應用程式，而不需要透過網際網路存取這些 app。</span><span class="sxs-lookup"><span data-stu-id="efda5-140">Deployment slots provide a way for you to stage and validate web apps without those apps being accessible over the Internet.</span></span>
<span data-ttu-id="efda5-141">通常您會將所做的變更部署到分段網站、驗證這些變更，然後部署到生產 (可透過網際網路存取的) 網站。</span><span class="sxs-lookup"><span data-stu-id="efda5-141">Typically you will deploy your changes to a staging site, validate those changes, and then deploy to the production (Internet-accessible) site.</span></span>

```yaml
Type: String
Parameter Sets: S1, S2
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efda5-142">-SslState</span><span class="sxs-lookup"><span data-stu-id="efda5-142">-SslState</span></span>
<span data-ttu-id="efda5-143">指定是否已啟用證書。</span><span class="sxs-lookup"><span data-stu-id="efda5-143">Specifies whether the certificate is enabled.</span></span>
<span data-ttu-id="efda5-144">將 *SSLState* 參數設定為1以啟用憑證，或將 *SSLState* 設定為0以停用憑證。</span><span class="sxs-lookup"><span data-stu-id="efda5-144">Set the *SSLState* parameter to 1 to enable the certificate, or set *SSLState* to 0 to disable the certificate.</span></span>

```yaml
Type: SslState
Parameter Sets: (All)
Aliases: 
Accepted values: Disabled, SniEnabled, IpBasedEnabled

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efda5-145">-指紋</span><span class="sxs-lookup"><span data-stu-id="efda5-145">-Thumbprint</span></span>
<span data-ttu-id="efda5-146">指定憑證的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="efda5-146">Specifies the unique identifier for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: S2, S4
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efda5-147">-WebApp</span><span class="sxs-lookup"><span data-stu-id="efda5-147">-WebApp</span></span>
<span data-ttu-id="efda5-148">指定 Web 應用程式。</span><span class="sxs-lookup"><span data-stu-id="efda5-148">Specifies a Web App.</span></span>
<span data-ttu-id="efda5-149">若要取得 Web 應用程式，請使用 Get-AzureRmWebApp Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="efda5-149">To get a Web App, use the Get-AzureRmWebApp cmdlet.</span></span>

<span data-ttu-id="efda5-150">您無法在與 *ResourceGroupName* 參數和/或 *WebAppName* 相同的命令中使用 *WebApp* 參數。</span><span class="sxs-lookup"><span data-stu-id="efda5-150">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

```yaml
Type: Site
Parameter Sets: S3, S4
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="efda5-151">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="efda5-151">-WebAppName</span></span>
<span data-ttu-id="efda5-152">指定要建立新 SSL 系結的 Web App 名稱。</span><span class="sxs-lookup"><span data-stu-id="efda5-152">Specifies the name of the Web App for which the new SSL binding is being created.</span></span>

<span data-ttu-id="efda5-153">您無法在同一命令中使用 *WebAppName* 參數和 *WebApp* 參數。</span><span class="sxs-lookup"><span data-stu-id="efda5-153">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: S1, S2
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efda5-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efda5-154">CommonParameters</span></span>
<span data-ttu-id="efda5-155">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="efda5-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efda5-156">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="efda5-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efda5-157">輸入</span><span class="sxs-lookup"><span data-stu-id="efda5-157">INPUTS</span></span>

### <span data-ttu-id="efda5-158">網站地圖</span><span class="sxs-lookup"><span data-stu-id="efda5-158">Site</span></span>
<span data-ttu-id="efda5-159">形參 "WebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="efda5-159">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="efda5-160">輸出</span><span class="sxs-lookup"><span data-stu-id="efda5-160">OUTPUTS</span></span>

## <span data-ttu-id="efda5-161">筆記</span><span class="sxs-lookup"><span data-stu-id="efda5-161">NOTES</span></span>

## <span data-ttu-id="efda5-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="efda5-162">RELATED LINKS</span></span>

[<span data-ttu-id="efda5-163">AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="efda5-163">Get-AzureRmWebAppSSLBinding</span></span>](./Get-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="efda5-164">移除-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="efda5-164">Remove-AzureRmWebAppSSLBinding</span></span>](./Remove-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="efda5-165">AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="efda5-165">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="efda5-166">AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="efda5-166">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

