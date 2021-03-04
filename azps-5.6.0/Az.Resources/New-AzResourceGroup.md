---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
ms.openlocfilehash: e32d5f53b13b26a93f23e4e557c6bad20911a776
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916502"
---
# <span data-ttu-id="30269-101">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="30269-101">New-AzResourceGroup</span></span>

## <span data-ttu-id="30269-102">簡介</span><span class="sxs-lookup"><span data-stu-id="30269-102">SYNOPSIS</span></span>
<span data-ttu-id="30269-103">建立 Azure 資源群組。</span><span class="sxs-lookup"><span data-stu-id="30269-103">Creates an Azure resource group.</span></span>

## <span data-ttu-id="30269-104">語法</span><span class="sxs-lookup"><span data-stu-id="30269-104">SYNTAX</span></span>

```
New-AzResourceGroup [-Name] <String> [-Location] <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30269-105">描述</span><span class="sxs-lookup"><span data-stu-id="30269-105">DESCRIPTION</span></span>
<span data-ttu-id="30269-106">**New-AzResourceGroup** Cmdlet 會建立 Azure 資源群組。</span><span class="sxs-lookup"><span data-stu-id="30269-106">The **New-AzResourceGroup** cmdlet creates an Azure resource group.</span></span>
<span data-ttu-id="30269-107">您可以只使用名稱和位置來建立資源群組，然後使用 New-AzResource Cmdlet 來建立資源以新增到資源群組。</span><span class="sxs-lookup"><span data-stu-id="30269-107">You can create a resource group by using just a name and location, and then use the New-AzResource cmdlet to create resources to add to the resource group.</span></span>
<span data-ttu-id="30269-108">若要新增部署至現有的資源群組，請使用 New-AzResourceGroupDeployment Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="30269-108">To add a deployment to an existing resource group, use the New-AzResourceGroupDeployment cmdlet.</span></span> <span data-ttu-id="30269-109">若要將資源新增到現有的資源群組，請使用 **New-AzResource** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="30269-109">To add a resource to an existing resource group, use the **New-AzResource** cmdlet.</span></span> <span data-ttu-id="30269-110">Azure 資源是使用者管理的 Azure 實體，例如資料庫伺服器、資料庫或網站。</span><span class="sxs-lookup"><span data-stu-id="30269-110">An Azure resource is a user-managed Azure entity, such as a database server, database, or website.</span></span> <span data-ttu-id="30269-111">Azure 資源群組是部署為一個單位的 Azure 資源集合。</span><span class="sxs-lookup"><span data-stu-id="30269-111">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>

## <span data-ttu-id="30269-112">例子</span><span class="sxs-lookup"><span data-stu-id="30269-112">EXAMPLES</span></span>

### <span data-ttu-id="30269-113">範例 1：建立空白資源群組</span><span class="sxs-lookup"><span data-stu-id="30269-113">Example 1: Create an empty resource group</span></span>
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US"
```

<span data-ttu-id="30269-114">此命令會建立一個沒有資源的資源群組。</span><span class="sxs-lookup"><span data-stu-id="30269-114">This command creates a resource group that has no resources.</span></span> <span data-ttu-id="30269-115">您可以使用 **New-AzResource** 或 **New-AzResourceGroupDeployment** Cmdlet 來新增資源與部署至此資源群組。</span><span class="sxs-lookup"><span data-stu-id="30269-115">You can use the **New-AzResource** or **New-AzResourceGroupDeployment** cmdlets to add resources and deployments to this resource group.</span></span>

### <span data-ttu-id="30269-116">範例 2：使用位置參數建立空白資源群組</span><span class="sxs-lookup"><span data-stu-id="30269-116">Example 2: Create an empty resource group using positional parameters</span></span>
```
PS> New-AzResourceGroup RG01 "South Central US"
```

<span data-ttu-id="30269-117">此命令會建立一個沒有資源的資源群組。</span><span class="sxs-lookup"><span data-stu-id="30269-117">This command creates a resource group that has no resources.</span></span>

### <span data-ttu-id="30269-118">範例 3：建立具有標記的資源群組</span><span class="sxs-lookup"><span data-stu-id="30269-118">Example 3: Create a resource group with tags</span></span>
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US" -Tag @{Empty=$null; Department="Marketing"}
```

<span data-ttu-id="30269-119">此命令會建立空白資源群組。</span><span class="sxs-lookup"><span data-stu-id="30269-119">This command creates an empty resource group.</span></span> <span data-ttu-id="30269-120">此命令與範例 1 中的命令相同，但它會指派標記給資源群組。</span><span class="sxs-lookup"><span data-stu-id="30269-120">This command is the same as the command in Example 1, except that it assigns tags to the resource group.</span></span> <span data-ttu-id="30269-121">第一個稱為 Empty 的標記可用來識別沒有資源的資源群組。</span><span class="sxs-lookup"><span data-stu-id="30269-121">The first tag, named Empty, can be used to identify resource groups that have no resources.</span></span> <span data-ttu-id="30269-122">第二個標記名為部門，且具有行銷值。</span><span class="sxs-lookup"><span data-stu-id="30269-122">The second tag is named Department and has a value of Marketing.</span></span> <span data-ttu-id="30269-123">您可以使用這個標記來將資源群組分類，以便管理或預算。</span><span class="sxs-lookup"><span data-stu-id="30269-123">You can use a tag such as this one to categorize resource groups for administration or budgeting.</span></span>

## <span data-ttu-id="30269-124">參數</span><span class="sxs-lookup"><span data-stu-id="30269-124">PARAMETERS</span></span>

### <span data-ttu-id="30269-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="30269-125">-ApiVersion</span></span>
<span data-ttu-id="30269-126">指定資源提供者支援的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="30269-126">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="30269-127">您可以指定與預設版本不同的版本。</span><span class="sxs-lookup"><span data-stu-id="30269-127">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30269-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30269-128">-DefaultProfile</span></span>
<span data-ttu-id="30269-129">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="30269-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="30269-130">-強制</span><span class="sxs-lookup"><span data-stu-id="30269-130">-Force</span></span>
<span data-ttu-id="30269-131">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="30269-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="30269-132">-位置</span><span class="sxs-lookup"><span data-stu-id="30269-132">-Location</span></span>
<span data-ttu-id="30269-133">指定資源群組的位置。</span><span class="sxs-lookup"><span data-stu-id="30269-133">Specifies the location of the resource group.</span></span> <span data-ttu-id="30269-134">指定 Azure 資料中心位置，例如美國西部或東南亞。</span><span class="sxs-lookup"><span data-stu-id="30269-134">Specify an Azure data center location, such as West US or Southeast Asia.</span></span> <span data-ttu-id="30269-135">您可以將資源群組放在任何位置。</span><span class="sxs-lookup"><span data-stu-id="30269-135">You can place a resource group in any location.</span></span> <span data-ttu-id="30269-136">資源群組不一定位於 Azure 訂閱的相同位置，也不一定位於與資源相同的位置。</span><span class="sxs-lookup"><span data-stu-id="30269-136">The resource group does not have to be in the same location your Azure subscription or in the same location as its resources.</span></span>
<span data-ttu-id="30269-137">若要判斷哪個位置支援每種資源類型，請使用Get-AzResourceProvider ProviderNamespace 參數的 *Cmdlet。*</span><span class="sxs-lookup"><span data-stu-id="30269-137">To determine which location supports each resource type, use the Get-AzResourceProvider cmdlet with the *ProviderNamespace* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30269-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="30269-138">-Name</span></span>
<span data-ttu-id="30269-139">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="30269-139">Specifies a name for the resource group.</span></span> <span data-ttu-id="30269-140">資源名稱在訂閱中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="30269-140">The resource name must be unique in the subscription.</span></span> <span data-ttu-id="30269-141">如果具有該名稱的資源群組已存在，命令會提示您確認，然後再取代現有的資源群組。</span><span class="sxs-lookup"><span data-stu-id="30269-141">If a resource group that has that name already exists, the command prompts you for confirmation before replacing the existing resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30269-142">-Pre</span><span class="sxs-lookup"><span data-stu-id="30269-142">-Pre</span></span>
<span data-ttu-id="30269-143">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="30269-143">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="30269-144">-標記</span><span class="sxs-lookup"><span data-stu-id="30269-144">-Tag</span></span>
<span data-ttu-id="30269-145">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="30269-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="30269-146">例如：@{key0="value0";key1=$null;key2="value2"} 若要新增或變更標記，您必須取代資源群組的標記集合。</span><span class="sxs-lookup"><span data-stu-id="30269-146">For example: @{key0="value0";key1=$null;key2="value2"} To add or change a tag, you must replace the collection of tags for the resource group.</span></span>
<span data-ttu-id="30269-147">將標記指派給資源和群組後，您可以使用 Get-AzResource 和Get-AzResourceGroup 的 Tag 參數，以標記名稱或名稱和值來搜尋資源和群組。</span><span class="sxs-lookup"><span data-stu-id="30269-147">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzResource and Get-AzResourceGroup to search for resources and groups by tag name or by name and value.</span></span> <span data-ttu-id="30269-148">您可以使用標記來分類資源，例如按照部門或成本中心，或追蹤資源的附注或批註。</span><span class="sxs-lookup"><span data-stu-id="30269-148">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>
<span data-ttu-id="30269-149">若要取得預先定義的標籤，請使用 Get-AzTag Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="30269-149">To get your predefined tags, use the Get-AzTag cmdlet.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30269-150">-確認</span><span class="sxs-lookup"><span data-stu-id="30269-150">-Confirm</span></span>
<span data-ttu-id="30269-151">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="30269-151">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30269-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30269-152">-WhatIf</span></span>
<span data-ttu-id="30269-153">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="30269-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30269-154">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="30269-154">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30269-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30269-155">CommonParameters</span></span>
<span data-ttu-id="30269-156">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="30269-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30269-157">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30269-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30269-158">輸入</span><span class="sxs-lookup"><span data-stu-id="30269-158">INPUTS</span></span>

### <span data-ttu-id="30269-159">System.String</span><span class="sxs-lookup"><span data-stu-id="30269-159">System.String</span></span>

### <span data-ttu-id="30269-160">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="30269-160">System.Collections.Hashtable</span></span>

## <span data-ttu-id="30269-161">輸出</span><span class="sxs-lookup"><span data-stu-id="30269-161">OUTPUTS</span></span>

### <span data-ttu-id="30269-162">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="30269-162">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="30269-163">筆記</span><span class="sxs-lookup"><span data-stu-id="30269-163">NOTES</span></span>

## <span data-ttu-id="30269-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="30269-164">RELATED LINKS</span></span>

[<span data-ttu-id="30269-165">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="30269-165">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="30269-166">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="30269-166">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="30269-167">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="30269-167">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="30269-168">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="30269-168">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="30269-169">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="30269-169">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)

[<span data-ttu-id="30269-170">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="30269-170">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)
