---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 6185C6BA-460E-4EEA-B1EF-CD67629AA75E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 51c20ef378cd2629ea96f236339a97172fb3038e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967396"
---
# <span data-ttu-id="73b09-101">Set-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="73b09-101">Set-AzureSubscription</span></span>

## <span data-ttu-id="73b09-102">摘要</span><span class="sxs-lookup"><span data-stu-id="73b09-102">SYNOPSIS</span></span>
<span data-ttu-id="73b09-103">變更 Azure 訂閱。</span><span class="sxs-lookup"><span data-stu-id="73b09-103">Changes an Azure subscription.</span></span>

## <span data-ttu-id="73b09-104">句法</span><span class="sxs-lookup"><span data-stu-id="73b09-104">SYNTAX</span></span>

### <span data-ttu-id="73b09-105">UpdateSubscriptionByIdParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="73b09-105">UpdateSubscriptionByIdParameterSetName (Default)</span></span>
```
Set-AzureSubscription -SubscriptionId <String> [-Certificate <X509Certificate2>] [-ServiceEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>] [-Context <AzureStorageContext>]
 [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="73b09-106">UpdateSubscriptionByNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="73b09-106">UpdateSubscriptionByNameParameterSetName</span></span>
```
Set-AzureSubscription -SubscriptionName <String> [-Certificate <X509Certificate2>] [-ServiceEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>] [-Context <AzureStorageContext>]
 [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="73b09-107">AddSubscriptionParameterSetName</span><span class="sxs-lookup"><span data-stu-id="73b09-107">AddSubscriptionParameterSetName</span></span>
```
Set-AzureSubscription -SubscriptionName <String> -SubscriptionId <String> -Certificate <X509Certificate2>
 [-ServiceEndpoint <String>] [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>]
 [-Context <AzureStorageContext>] [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="73b09-108">說明</span><span class="sxs-lookup"><span data-stu-id="73b09-108">DESCRIPTION</span></span>
<span data-ttu-id="73b09-109">**AzureSubscription** Cmdlet 會建立並變更 Azure 訂閱物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="73b09-109">The **Set-AzureSubscription** cmdlet establishes and changes the properties of an Azure subscription object.</span></span>
<span data-ttu-id="73b09-110">您可以使用這個 Cmdlet，在非預設訂閱的 Azure 訂閱中工作，或是變更您目前的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="73b09-110">You can use this cmdlet to work in an Azure subscription that is not your default subscription or to change your current storage account.</span></span>
<span data-ttu-id="73b09-111">如需目前及預設訂閱的相關資訊，請參閱 **AzureSubscription** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="73b09-111">For information about current and default subscriptions, see the **Select-AzureSubscription** cmdlet.</span></span>

<span data-ttu-id="73b09-112">這個 Cmdlet 在 Azure 訂閱物件上執行，而不是您實際的 Azure 訂閱。</span><span class="sxs-lookup"><span data-stu-id="73b09-112">This cmdlet operates on an Azure subscription object, not your actual Azure subscription.</span></span>
<span data-ttu-id="73b09-113">若要建立和置備 Azure 訂閱，請造訪 [Azure 入口網站](https://azure.microsoft.com/) (https://azure.microsoft.com/) 。</span><span class="sxs-lookup"><span data-stu-id="73b09-113">To create and provision an Azure subscription, visit the [Azure Portal](https://azure.microsoft.com/) (https://azure.microsoft.com/).</span></span>

<span data-ttu-id="73b09-114">這個 Cmdlet 會變更您在使用 [ **AzureAccount** ] 或 [匯 **入 AzurePublishSettingsFile** ] Cmdlet 將 Azure 帳戶新增至 Windows PowerShell 時所建立的訂閱資料檔案中的資料。</span><span class="sxs-lookup"><span data-stu-id="73b09-114">This cmdlet changes the data in the subscription data file that you create when you use the **Add-AzureAccount** or **Import-AzurePublishSettingsFile** cmdlet to add an Azure account to Windows PowerShell.</span></span>

<span data-ttu-id="73b09-115">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="73b09-115">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="73b09-116">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="73b09-116">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="73b09-117">示例</span><span class="sxs-lookup"><span data-stu-id="73b09-117">EXAMPLES</span></span>

### <span data-ttu-id="73b09-118">範例1：變更現有的 subscription1</span><span class="sxs-lookup"><span data-stu-id="73b09-118">Example 1: Change an existing subscription1</span></span>
```
C:\PS> $thumbprint = <Thumbprint-2>
C:\PS> $differentCert = Get-Item cert:\\CurrentUser\My\$thumbprint 
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -Certificate $differentCert
```

<span data-ttu-id="73b09-119">這個範例會變更名為 ContosoEngineering 之訂閱的憑證。</span><span class="sxs-lookup"><span data-stu-id="73b09-119">This example changes the certificate for the subscription named ContosoEngineering.</span></span>

### <span data-ttu-id="73b09-120">範例2：變更服務端點</span><span class="sxs-lookup"><span data-stu-id="73b09-120">Example 2: Change the service endpoint</span></span>
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -ServiceEndpoint "https://management.core.contoso.com"
```

<span data-ttu-id="73b09-121">這個命令會為 ContosoEngineering 訂閱新增或變更自訂服務端點。</span><span class="sxs-lookup"><span data-stu-id="73b09-121">This command adds or changes a custom service endpoint for the ContosoEngineering subscription.</span></span>

### <span data-ttu-id="73b09-122">範例3：清除屬性值</span><span class="sxs-lookup"><span data-stu-id="73b09-122">Example 3: Clear property values</span></span>
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -Certificate $null -ResourceManagerEndpoint $Null
```

<span data-ttu-id="73b09-123">這個命令會將憑證和 ResourceManagerEndpoint 屬性的值設定為 null ($Null) 。</span><span class="sxs-lookup"><span data-stu-id="73b09-123">This command sets the values of the Certificate and ResourceManagerEndpoint properties to null ($Null).</span></span>
<span data-ttu-id="73b09-124">這會清除這些屬性的值，而不會變更其他設定。</span><span class="sxs-lookup"><span data-stu-id="73b09-124">This clears the values of those properties without changing other settings.</span></span>

### <span data-ttu-id="73b09-125">範例4：使用替代訂閱資料檔案</span><span class="sxs-lookup"><span data-stu-id="73b09-125">Example 4: Use an alternate subscription data file</span></span>
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoFinance -SubscriptionDataFile C:\Azure\SubscriptionData.xml -CurrentStorageAccount ContosoStorage01
```

<span data-ttu-id="73b09-126">這個命令會將 ContosoFinance 訂閱的目前儲存空間帳戶變更為 ContosoStorage01。</span><span class="sxs-lookup"><span data-stu-id="73b09-126">This command changes the current storage account of the ContosoFinance subscription to ContosoStorage01.</span></span>
<span data-ttu-id="73b09-127">此命令會使用 **SubscriptionDataFile** 參數來變更 C:\Azure\SubscriptionData.xml 訂閱資料檔案中的資料。</span><span class="sxs-lookup"><span data-stu-id="73b09-127">The command uses the **SubscriptionDataFile** parameter to change the data in the C:\Azure\SubscriptionData.xml subscription data file.</span></span>
<span data-ttu-id="73b09-128">根據預設， **AzureSubscription** 會使用漫遊使用者設定檔中的預設訂閱資料檔案。</span><span class="sxs-lookup"><span data-stu-id="73b09-128">By default, **Set-AzureSubscription** uses the default subscription data file in your roaming user profile.</span></span>

## <span data-ttu-id="73b09-129">參數</span><span class="sxs-lookup"><span data-stu-id="73b09-129">PARAMETERS</span></span>

### <span data-ttu-id="73b09-130">-Certificate</span><span class="sxs-lookup"><span data-stu-id="73b09-130">-Certificate</span></span>
```yaml
Type: X509Certificate2
Parameter Sets: UpdateSubscriptionByIdParameterSetName, UpdateSubscriptionByNameParameterSetName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: X509Certificate2
Parameter Sets: AddSubscriptionParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73b09-131">-內容</span><span class="sxs-lookup"><span data-stu-id="73b09-131">-Context</span></span>
```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73b09-132">-CurrentStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="73b09-132">-CurrentStorageAccountName</span></span>
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

### <span data-ttu-id="73b09-133">-環境</span><span class="sxs-lookup"><span data-stu-id="73b09-133">-Environment</span></span>
<span data-ttu-id="73b09-134">指定 Azure 環境。</span><span class="sxs-lookup"><span data-stu-id="73b09-134">Specifies an Azure environment.</span></span>

<span data-ttu-id="73b09-135">Azure 環境是獨立部署的 Microsoft Azure，例如針對全域 Azure 的 AzureCloud，以及由中國由世紀運營之 AzureChinaCloud 的 Azure。</span><span class="sxs-lookup"><span data-stu-id="73b09-135">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="73b09-136">您也可以使用 Azure Pack 和 WAPack Cmdlet，建立內部部署的 Azure 環境。</span><span class="sxs-lookup"><span data-stu-id="73b09-136">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="73b09-137">如需詳細資訊，請參閱 [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="73b09-137">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

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

### <span data-ttu-id="73b09-138">-PassThru</span><span class="sxs-lookup"><span data-stu-id="73b09-138">-PassThru</span></span>
<span data-ttu-id="73b09-139">如果命令成功，則傳回 $True，且 $False 失敗。</span><span class="sxs-lookup"><span data-stu-id="73b09-139">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="73b09-140">根據預設，這個 Cmdlet 不會傳回任何輸出。</span><span class="sxs-lookup"><span data-stu-id="73b09-140">By default, this cmdlet does not return any output.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73b09-141">-設定檔</span><span class="sxs-lookup"><span data-stu-id="73b09-141">-Profile</span></span>
<span data-ttu-id="73b09-142">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="73b09-142">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="73b09-143">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="73b09-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="73b09-144">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="73b09-144">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="73b09-145">指定 Azure 資源管理器資料的端點，包括與該帳戶相關聯之資源群組的資料。</span><span class="sxs-lookup"><span data-stu-id="73b09-145">Specifies the endpoint for Azure Resource Manager data, including data about resource groups associated with the account.</span></span>
<span data-ttu-id="73b09-146">如需有關 Azure 資源管理員的詳細資訊，請參閱 [Azure 資源管理器 Cmdlet](https://go.microsoft.com/fwlink/?LinkID=394765)  (https://go.microsoft.com/fwlink/?LinkID=394765) 並 [使用 Windows PowerShell 與資源管理員](https://go.microsoft.com/fwlink/?LinkID=394767)  (https://go.microsoft.com/fwlink/?LinkID=394767) 。</span><span class="sxs-lookup"><span data-stu-id="73b09-146">For more information about Azure Resource Manager, see [Azure Resource Manager Cmdlets](https://go.microsoft.com/fwlink/?LinkID=394765)  (https://go.microsoft.com/fwlink/?LinkID=394765) and [Using Windows PowerShell with Resource Manager](https://go.microsoft.com/fwlink/?LinkID=394767)  (https://go.microsoft.com/fwlink/?LinkID=394767).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73b09-147">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="73b09-147">-ServiceEndpoint</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73b09-148">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="73b09-148">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: UpdateSubscriptionByIdParameterSetName, AddSubscriptionParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73b09-149">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="73b09-149">-SubscriptionName</span></span>
```yaml
Type: String
Parameter Sets: UpdateSubscriptionByNameParameterSetName, AddSubscriptionParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73b09-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73b09-150">CommonParameters</span></span>
<span data-ttu-id="73b09-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="73b09-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73b09-152">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="73b09-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73b09-153">輸入</span><span class="sxs-lookup"><span data-stu-id="73b09-153">INPUTS</span></span>

### <span data-ttu-id="73b09-154">所有</span><span class="sxs-lookup"><span data-stu-id="73b09-154">None</span></span>
<span data-ttu-id="73b09-155">您可以透過屬性名稱（而不是依值），將輸入管到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="73b09-155">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="73b09-156">輸出</span><span class="sxs-lookup"><span data-stu-id="73b09-156">OUTPUTS</span></span>

### <span data-ttu-id="73b09-157">None 或 System.object</span><span class="sxs-lookup"><span data-stu-id="73b09-157">None or System.Boolean</span></span>
<span data-ttu-id="73b09-158">當您使用 *PassThru* 參數時，這個 Cmdlet 會傳回布林值。</span><span class="sxs-lookup"><span data-stu-id="73b09-158">When you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="73b09-159">根據預設，這個 Cmdlet 不會傳回任何輸出。</span><span class="sxs-lookup"><span data-stu-id="73b09-159">By default, this cmdlet does not return any output.</span></span>

## <span data-ttu-id="73b09-160">筆記</span><span class="sxs-lookup"><span data-stu-id="73b09-160">NOTES</span></span>

## <span data-ttu-id="73b09-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="73b09-161">RELATED LINKS</span></span>

[<span data-ttu-id="73b09-162">附加 AzureAccount</span><span class="sxs-lookup"><span data-stu-id="73b09-162">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="73b09-163">AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="73b09-163">Get-AzureSubscription</span></span>](./Get-AzureSubscription.md)

[<span data-ttu-id="73b09-164">匯入-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="73b09-164">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="73b09-165">移除-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="73b09-165">Remove-AzureSubscription</span></span>](./Remove-AzureSubscription.md)

[<span data-ttu-id="73b09-166">選取-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="73b09-166">Select-AzureSubscription</span></span>](./Select-AzureSubscription.md)


