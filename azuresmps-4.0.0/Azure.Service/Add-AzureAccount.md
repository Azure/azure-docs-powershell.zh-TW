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
# <span data-ttu-id="f0cb8-101">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="f0cb8-101">Add-AzureAccount</span></span>

## <span data-ttu-id="f0cb8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f0cb8-102">SYNOPSIS</span></span>
<span data-ttu-id="f0cb8-103">將 Azure 帳戶新增至 Windows PowerShell。</span><span class="sxs-lookup"><span data-stu-id="f0cb8-103">Adds the Azure account to Windows PowerShell.</span></span>

## <span data-ttu-id="f0cb8-104">句法</span><span class="sxs-lookup"><span data-stu-id="f0cb8-104">SYNTAX</span></span>

### <span data-ttu-id="f0cb8-105">使用者 (預設) </span><span class="sxs-lookup"><span data-stu-id="f0cb8-105">User (Default)</span></span>
```
Add-AzureAccount [-Environment <String>] [-Credential <PSCredential>] [-Tenant <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f0cb8-106">ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f0cb8-106">ServicePrincipal</span></span>
```
Add-AzureAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f0cb8-107">說明</span><span class="sxs-lookup"><span data-stu-id="f0cb8-107">DESCRIPTION</span></span>
<span data-ttu-id="f0cb8-108">**AzureAccount** Cmdlet 會使您的 Azure 帳戶及其訂閱可在 Windows PowerShell 中使用。</span><span class="sxs-lookup"><span data-stu-id="f0cb8-108">The **Add-AzureAccount** cmdlet makes your Azure account and its subscriptions available in Windows PowerShell.</span></span>
<span data-ttu-id="f0cb8-109">就像是在 Windows PowerShell 中登入您的 Azure 帳戶一樣。</span><span class="sxs-lookup"><span data-stu-id="f0cb8-109">It's like logging into your Azure account in Windows PowerShell.</span></span>
<span data-ttu-id="f0cb8-110">若要登出帳戶，請使用 **AzureAccount** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f0cb8-110">To log out of the account, use the **Remove-AzureAccount** cmdlet.</span></span>

<span data-ttu-id="f0cb8-111">**載入 AzureAccount** 下載 Azure 帳戶的相關資訊，並將它儲存在您的漫遊使用者設定檔的訂閱資料檔中。</span><span class="sxs-lookup"><span data-stu-id="f0cb8-111">**Add-AzureAccount** downloads information about your Azure account and saves it in a subscription data file in your roaming user profile.</span></span>
<span data-ttu-id="f0cb8-112">它也會取得允許 Windows PowerShell 代表您存取 Azure 帳戶的存取權杖。</span><span class="sxs-lookup"><span data-stu-id="f0cb8-112">It also gets an access token that allows Windows PowerShell to access your Azure account on your behalf.</span></span>
<span data-ttu-id="f0cb8-113">當命令完成時，您可以在 Windows PowerShell 中管理您的 Azure 帳戶。</span><span class="sxs-lookup"><span data-stu-id="f0cb8-113">When the command completes, you can manage your Azure account in Windows PowerShell.</span></span>

<span data-ttu-id="f0cb8-114">您可以透過兩種不同的方式，讓您的 Azure 帳戶可供 Windows PowerShell 使用。</span><span class="sxs-lookup"><span data-stu-id="f0cb8-114">There are two different ways to make your Azure account available to Windows PowerShell.</span></span>
<span data-ttu-id="f0cb8-115">您可以使用 **AzureAccount** Cmdlet，使用 Azure Active Directory (azure AD) 驗證存取權杖，或使用管理憑證的匯 **入-AzurePublishSettingsFile** 。</span><span class="sxs-lookup"><span data-stu-id="f0cb8-115">You can use the **Add-AzureAccount** cmdlet, which uses Azure Active Directory (Azure AD) authentication access tokens, or **Import-AzurePublishSettingsFile** , which uses a management certificate.</span></span>
<span data-ttu-id="f0cb8-116">如需使用何種方法的指導方針，請參閱 [如何：連線至您的訂閱](https://azure.microsoft.com/documentation/articles/install-configure-powershell) (https://azure.microsoft.com/documentation/articles/install-configure-powershell/#Connect) 。</span><span class="sxs-lookup"><span data-stu-id="f0cb8-116">For guidance on which method to use, see [How to: Connect to your subscription](https://azure.microsoft.com/documentation/articles/install-configure-powershell) (https://azure.microsoft.com/documentation/articles/install-configure-powershell/#Connect).</span></span>

<span data-ttu-id="f0cb8-117">當您執行 [ **載入 AzureAccount** ] 時，會顯示互動式視窗，提示您登入您的 Azure 帳戶。</span><span class="sxs-lookup"><span data-stu-id="f0cb8-117">When you run **Add-AzureAccount** , it displays an interactive window that prompts you to sign into your Azure account.</span></span>
<span data-ttu-id="f0cb8-118">此登入一直有效，直到存取權杖到期為止。</span><span class="sxs-lookup"><span data-stu-id="f0cb8-118">This sign-in is valid until the access token expires.</span></span>
<span data-ttu-id="f0cb8-119">當它到期時，需要存取您帳戶的 Cmdlet 會提示您再次執行 **AzureAccount 附加程式** 。</span><span class="sxs-lookup"><span data-stu-id="f0cb8-119">When it expires, cmdlets that require access to your account prompt you to run **Add-AzureAccount** again.</span></span>

<span data-ttu-id="f0cb8-120">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f0cb8-120">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="f0cb8-121">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="f0cb8-121">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="f0cb8-122">示例</span><span class="sxs-lookup"><span data-stu-id="f0cb8-122">EXAMPLES</span></span>

### <span data-ttu-id="f0cb8-123">範例1：新增帳戶</span><span class="sxs-lookup"><span data-stu-id="f0cb8-123">Example 1: Add an account</span></span>
```
PS C:\> Add-AzureAccount
```

<span data-ttu-id="f0cb8-124">這個命令會將 Azure 帳戶新增至 Windows PowerShell。</span><span class="sxs-lookup"><span data-stu-id="f0cb8-124">This command adds an Azure account to Windows PowerShell.</span></span>
<span data-ttu-id="f0cb8-125">當您執行命令時，windows 會彈出來要求帳戶的使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="f0cb8-125">When you run the command, a windows pops up to request the user name and password of the account.</span></span>

### <span data-ttu-id="f0cb8-126">範例2：使用替代訂閱資料檔案</span><span class="sxs-lookup"><span data-stu-id="f0cb8-126">Example 2: Use an alternate subscription data file</span></span>
```
PS C:\> Add-AzureAccount -SubscriptionDataFile C:\Testing\SDF.xml
```

<span data-ttu-id="f0cb8-127">這個命令使用 **SubscriptionDataFile** 參數來直接 **AzureAccount 將** 帳戶資料儲存在 C:\Testing\SDF.xml 檔案中，而不是預設檔案。</span><span class="sxs-lookup"><span data-stu-id="f0cb8-127">This command uses the **SubscriptionDataFile** parameter to direct **Add-AzureAccount** to store the account data in the C:\Testing\SDF.xml file, instead of the default file.</span></span>

## <span data-ttu-id="f0cb8-128">參數</span><span class="sxs-lookup"><span data-stu-id="f0cb8-128">PARAMETERS</span></span>

### <span data-ttu-id="f0cb8-129">-認證</span><span class="sxs-lookup"><span data-stu-id="f0cb8-129">-Credential</span></span>
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

### <span data-ttu-id="f0cb8-130">-環境</span><span class="sxs-lookup"><span data-stu-id="f0cb8-130">-Environment</span></span>
<span data-ttu-id="f0cb8-131">指定 Azure 環境。</span><span class="sxs-lookup"><span data-stu-id="f0cb8-131">Specifies an Azure environment.</span></span>

<span data-ttu-id="f0cb8-132">Azure 環境是獨立部署的 Microsoft Azure，例如針對全域 Azure 的 AzureCloud，以及由中國由世紀運營之 AzureChinaCloud 的 Azure。</span><span class="sxs-lookup"><span data-stu-id="f0cb8-132">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="f0cb8-133">您也可以使用 Azure Pack 和 WAPack Cmdlet，建立內部部署的 Azure 環境。</span><span class="sxs-lookup"><span data-stu-id="f0cb8-133">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="f0cb8-134">如需詳細資訊，請參閱 [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="f0cb8-134">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

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

### <span data-ttu-id="f0cb8-135">-設定檔</span><span class="sxs-lookup"><span data-stu-id="f0cb8-135">-Profile</span></span>
<span data-ttu-id="f0cb8-136">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="f0cb8-136">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="f0cb8-137">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="f0cb8-137">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f0cb8-138">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f0cb8-138">-ServicePrincipal</span></span>
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

### <span data-ttu-id="f0cb8-139">-租使用者</span><span class="sxs-lookup"><span data-stu-id="f0cb8-139">-Tenant</span></span>
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

### <span data-ttu-id="f0cb8-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0cb8-140">CommonParameters</span></span>
<span data-ttu-id="f0cb8-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f0cb8-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0cb8-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f0cb8-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0cb8-143">輸入</span><span class="sxs-lookup"><span data-stu-id="f0cb8-143">INPUTS</span></span>

### <span data-ttu-id="f0cb8-144">所有</span><span class="sxs-lookup"><span data-stu-id="f0cb8-144">None</span></span>
<span data-ttu-id="f0cb8-145">您無法將輸入管到這個 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f0cb8-145">You cannot pipe input to this cmdlet</span></span>

## <span data-ttu-id="f0cb8-146">輸出</span><span class="sxs-lookup"><span data-stu-id="f0cb8-146">OUTPUTS</span></span>

### <span data-ttu-id="f0cb8-147">所有</span><span class="sxs-lookup"><span data-stu-id="f0cb8-147">None</span></span>
<span data-ttu-id="f0cb8-148">這個 Cmdlet 不會傳回任何輸出。</span><span class="sxs-lookup"><span data-stu-id="f0cb8-148">This cmdlet does not return any output.</span></span>

## <span data-ttu-id="f0cb8-149">筆記</span><span class="sxs-lookup"><span data-stu-id="f0cb8-149">NOTES</span></span>
* <span data-ttu-id="f0cb8-150">**載入 AzureAccount** (和 Azure AD 驗證方法) 優先于 **Import AzurePublishSettings** (且管理憑證方法) 。</span><span class="sxs-lookup"><span data-stu-id="f0cb8-150">**Add-AzureAccount** (and the Azure AD authentication method) takes precedence over **Import-AzurePublishSettings** (and the management certificate method).</span></span> <span data-ttu-id="f0cb8-151">如果您在帳戶上使用 **Add-AzureAccount** ，則會使用 Azure AD 驗證方法，且系統會忽略管理憑證。</span><span class="sxs-lookup"><span data-stu-id="f0cb8-151">If you use **Add-AzureAccount** even once on your account, the Azure AD authentication method is used and the management certificate is ignored.</span></span> <span data-ttu-id="f0cb8-152">若要移除 Azure AD 權杖並還原管理證書方法，請使用 **AzureAccount** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f0cb8-152">To remove the Azure AD token and restore the management certificate method, use the **Remove-AzureAccount** cmdlet.</span></span> <span data-ttu-id="f0cb8-153">如需詳細資訊，請輸入： **Get-help 移除-AzureAccount** 。</span><span class="sxs-lookup"><span data-stu-id="f0cb8-153">For more information, type: **Get-Help Remove-AzureAccount**.</span></span>
* <span data-ttu-id="f0cb8-154">錯誤，"您的認證已過期。</span><span class="sxs-lookup"><span data-stu-id="f0cb8-154">The error, "Your credentials have expired.</span></span> <span data-ttu-id="f0cb8-155">請使用 Add-AzureAccount 再次登入。」</span><span class="sxs-lookup"><span data-stu-id="f0cb8-155">Please use Add-AzureAccount to log in again."</span></span> <span data-ttu-id="f0cb8-156">表示您的存取權杖已過期，且 Windows PowerShell 無法存取您的 Azure 帳戶。</span><span class="sxs-lookup"><span data-stu-id="f0cb8-156">indicates that your access token is expired and Windows PowerShell cannot access your Azure account.</span></span> <span data-ttu-id="f0cb8-157">若要還原您帳戶的存取權，請再次執行 [ **載入 AzureAccount** ]。</span><span class="sxs-lookup"><span data-stu-id="f0cb8-157">To restore access to your account, run **Add-AzureAccount** again.</span></span>
* <span data-ttu-id="f0cb8-158">Azure PowerShell 帳戶和訂閱 Cmdlet 會從訂閱資料檔案取得資料，而不是從實際的 Azure 帳戶取得。</span><span class="sxs-lookup"><span data-stu-id="f0cb8-158">The Azure PowerShell account and subscription cmdlets get their data from the  subscription data file, not from the live Azure account.</span></span> <span data-ttu-id="f0cb8-159">如果您在 Windows PowerShell 之外變更您的帳戶或訂閱（例如使用 Azure 管理入口網站），請再次執行 [ **載入 AzureAccount** ] 以重新整理訂閱資料檔案。</span><span class="sxs-lookup"><span data-stu-id="f0cb8-159">If you change your account or subscriptions outside of Windows PowerShell, such as by using the Azure Management Portal, run **Add-AzureAccount** again to refresh the subscription data file.</span></span>

## <span data-ttu-id="f0cb8-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="f0cb8-160">RELATED LINKS</span></span>

[<span data-ttu-id="f0cb8-161">附加 AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="f0cb8-161">Add-AzureEnvironment</span></span>](./Add-AzureEnvironment.md)

[<span data-ttu-id="f0cb8-162">AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="f0cb8-162">Get-AzureEnvironment</span></span>](./Get-AzureEnvironment.md)

[<span data-ttu-id="f0cb8-163">匯入-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="f0cb8-163">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="f0cb8-164">AzureAccount</span><span class="sxs-lookup"><span data-stu-id="f0cb8-164">Get-AzureAccount</span></span>](./Get-AzureAccount.md)

[<span data-ttu-id="f0cb8-165">移除-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="f0cb8-165">Remove-AzureAccount</span></span>](./Remove-AzureAccount.md)


