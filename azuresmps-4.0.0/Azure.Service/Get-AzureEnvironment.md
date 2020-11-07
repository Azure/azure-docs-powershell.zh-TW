---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: BF5E3E1A-14B6-4630-8168-628057009D5E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 284d1601746254b2e10fdfe042e5882e94ca1bd9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967798"
---
# <span data-ttu-id="a804f-101">Get-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="a804f-101">Get-AzureEnvironment</span></span>

## <span data-ttu-id="a804f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a804f-102">SYNOPSIS</span></span>
<span data-ttu-id="a804f-103">取得 Azure 環境</span><span class="sxs-lookup"><span data-stu-id="a804f-103">Gets Azure environments</span></span>

## <span data-ttu-id="a804f-104">句法</span><span class="sxs-lookup"><span data-stu-id="a804f-104">SYNTAX</span></span>

```
Get-AzureEnvironment [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a804f-105">說明</span><span class="sxs-lookup"><span data-stu-id="a804f-105">DESCRIPTION</span></span>
<span data-ttu-id="a804f-106">**AzureEnvironment** Cmdlet 會取得適用于 Windows PowerShell 的 Azure 環境。</span><span class="sxs-lookup"><span data-stu-id="a804f-106">The **Get-AzureEnvironment** cmdlet gets the Azure environments that are available to Windows PowerShell.</span></span>

<span data-ttu-id="a804f-107">Azure 環境是獨立部署的 Microsoft Azure，例如針對全域 Azure 的 AzureCloud，以及由中國由世紀運營之 AzureChinaCloud 的 Azure。</span><span class="sxs-lookup"><span data-stu-id="a804f-107">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="a804f-108">您也可以使用 Azure Pack 和 WAPack Cmdlet，建立內部部署的 Azure 環境。</span><span class="sxs-lookup"><span data-stu-id="a804f-108">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="a804f-109">如需詳細資訊，請參閱 [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="a804f-109">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

<span data-ttu-id="a804f-110">**AzureEnvironment** Cmdlet 會從您的訂閱資料檔案（而不是從 Azure）取得環境。</span><span class="sxs-lookup"><span data-stu-id="a804f-110">The **Get-AzureEnvironment** cmdlet gets environments from your subscription data file, not from Azure.</span></span>
<span data-ttu-id="a804f-111">如果訂閱資料檔案已過時，請執行 **AzureAccount** 或 **Import PublishSettingsFile** Cmdlet 來重新整理。</span><span class="sxs-lookup"><span data-stu-id="a804f-111">If the subscription data file is outdated, run the **Add-AzureAccount** or **Import-PublishSettingsFile** cmdlet to refresh it.</span></span>

<span data-ttu-id="a804f-112">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a804f-112">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="a804f-113">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="a804f-113">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="a804f-114">示例</span><span class="sxs-lookup"><span data-stu-id="a804f-114">EXAMPLES</span></span>

### <span data-ttu-id="a804f-115">範例1：取得所有環境</span><span class="sxs-lookup"><span data-stu-id="a804f-115">Example 1: Get all environments</span></span>
```
PS C:\> Get-AzureEnvironment

EnvironmentName               ServiceEndpoint               ResourceManagerEndpoint       PublishSettingsFileUrl
---------------               ---------------               -----------------------       ----------------------

AzureCloud                    https://management.core.wi... https://management.azure.com/ https://go.microsoft.com/fw... 
AzureChinaCloud               https://management.core.ch... https://not-supported-serv... https://go.microsoft.com/fw...
```

<span data-ttu-id="a804f-116">這個命令會取得可供 Windows PowerShell 使用的所有環境。</span><span class="sxs-lookup"><span data-stu-id="a804f-116">This command gets all environments that are available to Windows PowerShell.</span></span>

### <span data-ttu-id="a804f-117">範例2：依名稱取得環境</span><span class="sxs-lookup"><span data-stu-id="a804f-117">Example 2: Get an environment by name</span></span>
```
PS C:\> Get-AzureEnvironment -Name AzureCloud

Name                          : AzureCloud

PublishSettingsFileUrl        : https://go.microsoft.com/fwlink/?LinkID=301775

ServiceEndpoint               : https://management.core.windows.net/

ResourceManagerEndpoint       : https://management.azure.com/

ManagementPortalUrl           : https://go.microsoft.com/fwlink/?LinkId=254433

ActiveDirectoryEndpoint       : https://login.windows.net/

ActiveDirectoryCommonTenantId : common

StorageEndpointSuffix         : core.windows.net

StorageBlobEndpointFormat     : {0}://{1}.blob.core.windows.net/

StorageQueueEndpointFormat    : {0}://{1}.queue.core.windows.net/

StorageTableEndpointFormat    : {0}://{1}.table.core.windows.net/

GalleryEndpoint               : https://gallery.azure.com/
```

<span data-ttu-id="a804f-118">這個範例會取得 AzureCloud 環境。</span><span class="sxs-lookup"><span data-stu-id="a804f-118">This example gets the AzureCloud environment.</span></span>

### <span data-ttu-id="a804f-119">範例3：取得所有環境的所有屬性</span><span class="sxs-lookup"><span data-stu-id="a804f-119">Example 3: Get all properties of all environments</span></span>
```
PS C:\> Get-AzureEnvironment | ForEach-Object {Get-AzureEnvironment -Name $_.EnvironmentName}
```

<span data-ttu-id="a804f-120">這個命令會取得所有環境的所有屬性。</span><span class="sxs-lookup"><span data-stu-id="a804f-120">This command gets all properties of all environments.</span></span>

<span data-ttu-id="a804f-121">此命令使用 **AzureEnvironment** Cmdlet 來取得此帳戶的所有 Azure 環境。</span><span class="sxs-lookup"><span data-stu-id="a804f-121">The command uses the **Get-AzureEnvironment** cmdlet to get all Azure environments for this account.</span></span>
<span data-ttu-id="a804f-122">接著，它會使用 **Foreach 物件** Cmdlet 來執行 **AzureEnvironment** 命令，並在每個環境中使用 **Name** 參數。</span><span class="sxs-lookup"><span data-stu-id="a804f-122">Then, it uses the **Foreach-Object** cmdlet to run a **Get-AzureEnvironment** command with the **Name** parameter on each environment.</span></span>
<span data-ttu-id="a804f-123">**Name** 參數的值是每個環境的 **EnvironmentName** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a804f-123">The value of the **Name** parameter is the **EnvironmentName** property of each environment.</span></span>

<span data-ttu-id="a804f-124">如果沒有參數， **AzureEnvironment** 只會取得環境的選取屬性。</span><span class="sxs-lookup"><span data-stu-id="a804f-124">Without parameters, **Get-AzureEnvironment** gets only selected properties of an environment.</span></span>

## <span data-ttu-id="a804f-125">參數</span><span class="sxs-lookup"><span data-stu-id="a804f-125">PARAMETERS</span></span>

### <span data-ttu-id="a804f-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="a804f-126">-Name</span></span>
<span data-ttu-id="a804f-127">僅取得指定的環境。</span><span class="sxs-lookup"><span data-stu-id="a804f-127">Gets only the specified environment.</span></span>
<span data-ttu-id="a804f-128">輸入環境名稱。</span><span class="sxs-lookup"><span data-stu-id="a804f-128">Type the environment name.</span></span>
<span data-ttu-id="a804f-129">參數值區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="a804f-129">The parameter value is case-sensitive.</span></span>
<span data-ttu-id="a804f-130">不允許通配字元。</span><span class="sxs-lookup"><span data-stu-id="a804f-130">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="a804f-131">-設定檔</span><span class="sxs-lookup"><span data-stu-id="a804f-131">-Profile</span></span>
<span data-ttu-id="a804f-132">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="a804f-132">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="a804f-133">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="a804f-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a804f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a804f-134">CommonParameters</span></span>
<span data-ttu-id="a804f-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a804f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a804f-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a804f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a804f-137">輸入</span><span class="sxs-lookup"><span data-stu-id="a804f-137">INPUTS</span></span>

### <span data-ttu-id="a804f-138">所有</span><span class="sxs-lookup"><span data-stu-id="a804f-138">None</span></span>
<span data-ttu-id="a804f-139">您可以透過屬性名稱（而不是依值），將輸入管到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a804f-139">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="a804f-140">輸出</span><span class="sxs-lookup"><span data-stu-id="a804f-140">OUTPUTS</span></span>

### <span data-ttu-id="a804f-141">PSCustomObject 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="a804f-141">System.Management.Automation.PSCustomObject</span></span>
<span data-ttu-id="a804f-142">根據預設， **AzureEnvironment** 會傳回自訂物件。</span><span class="sxs-lookup"><span data-stu-id="a804f-142">By default, **Get-AzureEnvironment** returns a custom object.</span></span>

### <span data-ttu-id="a804f-143">WindowsAzure. 常見. WindowsAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="a804f-143">Microsoft.WindowsAzure.Commands.Utilities.Common.WindowsAzureEnvironment</span></span>
<span data-ttu-id="a804f-144">當您使用 **Name** 參數執行 **AzureEnvironment** 時，它會傳回 **WindowsAzureEnvironment** 物件。</span><span class="sxs-lookup"><span data-stu-id="a804f-144">When you run **Get-AzureEnvironment** with the **Name** parameter, it returns a  **WindowsAzureEnvironment** object.</span></span>

## <span data-ttu-id="a804f-145">筆記</span><span class="sxs-lookup"><span data-stu-id="a804f-145">NOTES</span></span>

## <span data-ttu-id="a804f-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="a804f-146">RELATED LINKS</span></span>

[<span data-ttu-id="a804f-147">附加 AzureAccount</span><span class="sxs-lookup"><span data-stu-id="a804f-147">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="a804f-148">附加 AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="a804f-148">Add-AzureEnvironment</span></span>](./Add-AzureEnvironment.md)

[<span data-ttu-id="a804f-149">AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="a804f-149">Get-AzurePublishSettingsFile</span></span>](./Get-AzurePublishSettingsFile.md)

[<span data-ttu-id="a804f-150">匯入-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="a804f-150">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="a804f-151">移除-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="a804f-151">Remove-AzureEnvironment</span></span>](./Remove-AzureEnvironment.md)

[<span data-ttu-id="a804f-152">Set-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="a804f-152">Set-AzureEnvironment</span></span>](./Set-AzureEnvironment.md)


