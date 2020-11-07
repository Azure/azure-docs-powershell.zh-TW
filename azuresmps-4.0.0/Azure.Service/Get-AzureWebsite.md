---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E4B1AA31-1185-4035-86E6-2BB2587285C6
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8273613081ab6bab0c9c3481df90f5b680b3355
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967720"
---
# <span data-ttu-id="08e79-101">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="08e79-101">Get-AzureWebsite</span></span>

## <span data-ttu-id="08e79-102">摘要</span><span class="sxs-lookup"><span data-stu-id="08e79-102">SYNOPSIS</span></span>
<span data-ttu-id="08e79-103">取得目前訂閱中的 Azure 網站。</span><span class="sxs-lookup"><span data-stu-id="08e79-103">Gets Azure websites in the current subscription.</span></span>

## <span data-ttu-id="08e79-104">句法</span><span class="sxs-lookup"><span data-stu-id="08e79-104">SYNTAX</span></span>

```
Get-AzureWebsite [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="08e79-105">說明</span><span class="sxs-lookup"><span data-stu-id="08e79-105">DESCRIPTION</span></span>
<span data-ttu-id="08e79-106">**AzureWebsite** Cmdlet 會取得目前訂閱中 Azure 網站的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="08e79-106">The **Get-AzureWebsite** cmdlet gets information about Azure websites in the current subscription.</span></span>

<span data-ttu-id="08e79-107">根據預設， **AzureWebsite** 會取得目前訂閱中的所有 Azure 網站，並傳回提供網站基本資訊的物件。</span><span class="sxs-lookup"><span data-stu-id="08e79-107">By default, **Get-AzureWebsite** gets all Azure websites in the current subscription and returns an object that provides basic information about the sites.</span></span>
<span data-ttu-id="08e79-108">當您使用 *Name* 參數時， **AzureWebsite** 會傳回包含大量資訊的物件，包括設定詳細資料。</span><span class="sxs-lookup"><span data-stu-id="08e79-108">When you use the *Name* parameter, **Get-AzureWebsite** returns an object with extensive information, including configuration details.</span></span>

<span data-ttu-id="08e79-109">目前的訂閱是指派為「目前」的訂閱。</span><span class="sxs-lookup"><span data-stu-id="08e79-109">The current subscription is the subscription that is designated as "current."</span></span> <span data-ttu-id="08e79-110">若要尋找目前的訂閱，請使用 [AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397623) Cmdlet 的 *目前* 參數。</span><span class="sxs-lookup"><span data-stu-id="08e79-110">To find the current subscription, use the *Current* parameter of the [Get-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397623) cmdlet.</span></span>
<span data-ttu-id="08e79-111">若要變更目前的訂閱，請使用 [AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397628) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="08e79-111">To change the current subscription, use the [Select-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397628) cmdlet.</span></span>

<span data-ttu-id="08e79-112">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="08e79-112">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="08e79-113">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="08e79-113">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="08e79-114">示例</span><span class="sxs-lookup"><span data-stu-id="08e79-114">EXAMPLES</span></span>

### <span data-ttu-id="08e79-115">範例1：取得訂閱中的所有網站</span><span class="sxs-lookup"><span data-stu-id="08e79-115">Example 1: Get all websites in the subscription</span></span>
```
PS C:\> Get-AzureWebsite
```

<span data-ttu-id="08e79-116">這個命令會取得目前訂閱中的所有 Azure 網站。</span><span class="sxs-lookup"><span data-stu-id="08e79-116">This command gets all Azure websites in the current subscription.</span></span>

### <span data-ttu-id="08e79-117">範例2：依名稱取得網站</span><span class="sxs-lookup"><span data-stu-id="08e79-117">Example 2: Get a website by name</span></span>
```
PS C:\> Get-AzureWebsite -Name ContosoWeb
```

<span data-ttu-id="08e79-118">這個命令會取得 ContosoWeb Azure 網站的詳細資訊，包括設定資訊。</span><span class="sxs-lookup"><span data-stu-id="08e79-118">This command gets detailed information about the ContosoWeb Azure website, including configuration information.</span></span>
<span data-ttu-id="08e79-119">當您使用 *Name* 參數時， **AzureWebsite** 會傳回含有網站延伸資訊的 **SiteWithConfig** 物件。</span><span class="sxs-lookup"><span data-stu-id="08e79-119">When you use the *Name* parameter, **Get-AzureWebsite** returns a **SiteWithConfig** object with extended information about the website.</span></span>

### <span data-ttu-id="08e79-120">範例3：取得所有網站的詳細資訊</span><span class="sxs-lookup"><span data-stu-id="08e79-120">Example 3: Get detailed information about all websites</span></span>
```
PS C:\> Get-AzureWebsite | ForEach-Object {Get-AzureWebsite -Name $_.Name}
```

<span data-ttu-id="08e79-121">這個命令會取得訂閱中所有網站的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="08e79-121">This command gets detailed information about all websites in the subscription.</span></span>
<span data-ttu-id="08e79-122">它會使用 **AzureWebsite** 命令來取得所有網站，然後使用 **ForEach 物件** Cmdlet，透過名稱取得每個網站。</span><span class="sxs-lookup"><span data-stu-id="08e79-122">It uses a **Get-AzureWebsite** command to get all websites and then uses the **ForEach-Object** cmdlet to get each website by name.</span></span>

### <span data-ttu-id="08e79-123">範例4：取得有關部署槽的資訊</span><span class="sxs-lookup"><span data-stu-id="08e79-123">Example 4: Get information about a deployment slot</span></span>
```
PS C:\> Get-AzureWebsite -Name ContosoWeb -Slot Staging
```

<span data-ttu-id="08e79-124">這個命令會取得 ContosoWeb 網站的暫存部署槽。</span><span class="sxs-lookup"><span data-stu-id="08e79-124">This command gets the Staging deployment slot of the ContosoWeb website.</span></span>
<span data-ttu-id="08e79-125">部署槽可讓您測試 Azure 網站的不同版本，而不需將其釋放到公用。</span><span class="sxs-lookup"><span data-stu-id="08e79-125">Deployment slots let you test different versions of your Azure website without releasing them to the public.</span></span>

### <span data-ttu-id="08e79-126">範例5：取得網站實例</span><span class="sxs-lookup"><span data-stu-id="08e79-126">Example 5: Get website instances</span></span>
```
PS C:\>(Get-AzureWebsite -Name ContosoWeb).Instances

InstanceId
----------
2d8e712fb8f85d061c30fd793a534e6700a175f9a9ab12ca55cb3b0edfcc10ee
5834916b8cef49249b18187708223a33fbbc4352d33b48369f3166644bdd3445

PS C:\>(Get-AzureWebsite -Name ContosoWeb).Instances.Count
2
```

<span data-ttu-id="08e79-127">這個範例中的命令使用 Azure 網站的實例屬性來取得目前執行的網站實例的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="08e79-127">The commands in this example use the Instances property of an Azure website to get information about currently running website instances.</span></span>
<span data-ttu-id="08e79-128">[ **範例** ] 屬性已新增至 Azure 模組版本0.8.3 中的 **SiteWithConfig** 物件。</span><span class="sxs-lookup"><span data-stu-id="08e79-128">The **Instances** property was added to the **SiteWithConfig** object in version 0.8.3 of the Azure module.</span></span>

<span data-ttu-id="08e79-129">第一個命令會取得網站所有目前執行實例的實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="08e79-129">The first command gets the instance IDs of all currently running instances of a website.</span></span>
<span data-ttu-id="08e79-130">第二個命令會取得網站執行中的實例數。</span><span class="sxs-lookup"><span data-stu-id="08e79-130">The second command gets the number of running instances of the website.</span></span>
<span data-ttu-id="08e79-131">您可以在任何陣列中使用 **Count** 屬性。</span><span class="sxs-lookup"><span data-stu-id="08e79-131">You can use the **Count** property on any array.</span></span>

## <span data-ttu-id="08e79-132">參數</span><span class="sxs-lookup"><span data-stu-id="08e79-132">PARAMETERS</span></span>

### <span data-ttu-id="08e79-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="08e79-133">-Name</span></span>
<span data-ttu-id="08e79-134">取得指定網站的詳細配置資訊。</span><span class="sxs-lookup"><span data-stu-id="08e79-134">Gets detailed configuration information about the specified website.</span></span>
<span data-ttu-id="08e79-135">輸入訂閱中某個網站的名稱。</span><span class="sxs-lookup"><span data-stu-id="08e79-135">Enter the name of one website in the subscription.</span></span>
<span data-ttu-id="08e79-136">根據預設， **AzureWebsite 會取得** 目前訂閱中的所有網站。</span><span class="sxs-lookup"><span data-stu-id="08e79-136">By default, **Get-AzureWebsite** gets all websites in the current subscription.</span></span>
<span data-ttu-id="08e79-137">[ *Name* ] （名稱）值不支援萬用字元字元。</span><span class="sxs-lookup"><span data-stu-id="08e79-137">The *Name* value does not support wildcard characters.</span></span>

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

### <span data-ttu-id="08e79-138">-設定檔</span><span class="sxs-lookup"><span data-stu-id="08e79-138">-Profile</span></span>
<span data-ttu-id="08e79-139">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="08e79-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="08e79-140">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="08e79-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="08e79-141">-槽</span><span class="sxs-lookup"><span data-stu-id="08e79-141">-Slot</span></span>
<span data-ttu-id="08e79-142">取得網站的指定部署槽。</span><span class="sxs-lookup"><span data-stu-id="08e79-142">Gets the specified deployment slot of the website.</span></span>
<span data-ttu-id="08e79-143">輸入插槽名稱，例如「分段」或「生產」。</span><span class="sxs-lookup"><span data-stu-id="08e79-143">Enter the slot name, such as "Staging" or "Production".</span></span>
<span data-ttu-id="08e79-144">如需部署槽的詳細資訊，請參閱 Microsoft Azure 網站上的分段部署 https://azure.microsoft.com/en-us/documentation/articles/web-sites-staged-publishing/ 。</span><span class="sxs-lookup"><span data-stu-id="08e79-144">For more information about deployment slots, see Staged Deployment on Microsoft Azure Web Siteshttps://azure.microsoft.com/en-us/documentation/articles/web-sites-staged-publishing/.</span></span>
<span data-ttu-id="08e79-145">若要將部署槽新增至現有的 Azure 網站，請使用 Set-AzureWebsite Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="08e79-145">To add a deployment slot to an existing Azure website, use the Set-AzureWebsite cmdlet.</span></span>

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

### <span data-ttu-id="08e79-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08e79-146">CommonParameters</span></span>
<span data-ttu-id="08e79-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="08e79-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08e79-148">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="08e79-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08e79-149">輸入</span><span class="sxs-lookup"><span data-stu-id="08e79-149">INPUTS</span></span>

### <span data-ttu-id="08e79-150">所有</span><span class="sxs-lookup"><span data-stu-id="08e79-150">None</span></span>
<span data-ttu-id="08e79-151">您可以透過屬性名稱（而不是依值），將輸入管到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="08e79-151">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="08e79-152">輸出</span><span class="sxs-lookup"><span data-stu-id="08e79-152">OUTPUTS</span></span>

### <span data-ttu-id="08e79-153">WindowsAzure. WebEntities. Site （公用網站）</span><span class="sxs-lookup"><span data-stu-id="08e79-153">Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.Site</span></span>
<span data-ttu-id="08e79-154">根據預設， **AzureWebsite** 會傳回 **網站** 物件的陣列。</span><span class="sxs-lookup"><span data-stu-id="08e79-154">By default, **Get-AzureWebsite** returns an array of **Site** objects.</span></span>

### <span data-ttu-id="08e79-155">WindowsAzure. WebEntities. SiteWithConfig （）</span><span class="sxs-lookup"><span data-stu-id="08e79-155">Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.SiteWithConfig</span></span>
<span data-ttu-id="08e79-156">當您使用 *Name* 參數時， **AzureWebsite** 會傳回 **SiteWithConfig** 物件。</span><span class="sxs-lookup"><span data-stu-id="08e79-156">When you use the *Name* parameter, **Get-AzureWebsite** returns a **SiteWithConfig** object.</span></span>

## <span data-ttu-id="08e79-157">筆記</span><span class="sxs-lookup"><span data-stu-id="08e79-157">NOTES</span></span>

## <span data-ttu-id="08e79-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="08e79-158">RELATED LINKS</span></span>

[<span data-ttu-id="08e79-159">新-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="08e79-159">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="08e79-160">移除-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="08e79-160">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="08e79-161">開始-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="08e79-161">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)

[<span data-ttu-id="08e79-162">停止 AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="08e79-162">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)

[<span data-ttu-id="08e79-163">顯示-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="08e79-163">Show-AzureWebsite</span></span>](./Show-AzureWebsite.md)


