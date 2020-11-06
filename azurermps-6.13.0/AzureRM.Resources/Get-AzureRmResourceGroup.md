---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroup.md
ms.openlocfilehash: 73defde38ab34bc81adf904d5139308dfd556f79
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448256"
---
# <span data-ttu-id="be3ec-101">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="be3ec-101">Get-AzureRmResourceGroup</span></span>

## <span data-ttu-id="be3ec-102">摘要</span><span class="sxs-lookup"><span data-stu-id="be3ec-102">SYNOPSIS</span></span>
<span data-ttu-id="be3ec-103">取得資源群組。</span><span class="sxs-lookup"><span data-stu-id="be3ec-103">Gets resource groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be3ec-104">句法</span><span class="sxs-lookup"><span data-stu-id="be3ec-104">SYNTAX</span></span>

### <span data-ttu-id="be3ec-105">GetByResourceGroupName (預設) </span><span class="sxs-lookup"><span data-stu-id="be3ec-105">GetByResourceGroupName (Default)</span></span>
```
Get-AzureRmResourceGroup [-Name <String>] [-Location <String>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be3ec-106">GetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="be3ec-106">GetByResourceGroupId</span></span>
```
Get-AzureRmResourceGroup [-Location <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be3ec-107">說明</span><span class="sxs-lookup"><span data-stu-id="be3ec-107">DESCRIPTION</span></span>
<span data-ttu-id="be3ec-108">**AzureRmResourceGroup** Cmdlet 會在目前的訂閱中取得 Azure 資源群組。</span><span class="sxs-lookup"><span data-stu-id="be3ec-108">The **Get-AzureRmResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="be3ec-109">您可以取得所有資源群組，或是依名稱或其他屬性來指定資源群組。</span><span class="sxs-lookup"><span data-stu-id="be3ec-109">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="be3ec-110">根據預設，這個 Cmdlet 會取得目前訂閱中的所有資源群組。</span><span class="sxs-lookup"><span data-stu-id="be3ec-110">By default, this cmdlet gets all resource groups in the current subscription.</span></span>
<span data-ttu-id="be3ec-111">如需有關 Azure 資源和 Azure 資源群組的詳細資訊，請參閱 New-AzureRmResourceGroup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="be3ec-111">For more information about Azure resources and Azure resource groups, see the New-AzureRmResourceGroup cmdlet.</span></span>

## <span data-ttu-id="be3ec-112">示例</span><span class="sxs-lookup"><span data-stu-id="be3ec-112">EXAMPLES</span></span>

### <span data-ttu-id="be3ec-113">範例1：依名稱取得資源群組</span><span class="sxs-lookup"><span data-stu-id="be3ec-113">Example 1: Get a resource group by name</span></span>
```
PS C:\>Get-AzureRmResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="be3ec-114">這個命令會在您的訂閱中取得名為 EngineerBlog 的 Azure 資源群組。</span><span class="sxs-lookup"><span data-stu-id="be3ec-114">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="be3ec-115">範例2：取得資源群組的所有標籤</span><span class="sxs-lookup"><span data-stu-id="be3ec-115">Example 2: Get all tags of a resource group</span></span>
```
PS C:\>(Get-AzureRmResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="be3ec-116">這個命令會取得名為 ContosoRG 的資源群組，並顯示與該群組相關聯的標籤。</span><span class="sxs-lookup"><span data-stu-id="be3ec-116">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

### <span data-ttu-id="be3ec-117">範例3：依位置顯示資源群組</span><span class="sxs-lookup"><span data-stu-id="be3ec-117">Example 3: Show the Resource groups by location</span></span>
```
PS C:\> Get-AzureRmResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### <span data-ttu-id="be3ec-118">範例4：顯示特定位置中所有資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="be3ec-118">Example 4: Show the names of all the Resource groups in a particular location</span></span>
```
PS C:\> Get-AzureRmResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### <span data-ttu-id="be3ec-119">範例5：顯示其名稱以 Web 內容開頭的資源群組</span><span class="sxs-lookup"><span data-stu-id="be3ec-119">Example 5: Show the Resource groups whose names begin with WebServer</span></span>
```
PS C:\> Get-AzureRmResourceGroup | Where ResourceGroupName -like WebServer*
```

## <span data-ttu-id="be3ec-120">參數</span><span class="sxs-lookup"><span data-stu-id="be3ec-120">PARAMETERS</span></span>

### <span data-ttu-id="be3ec-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="be3ec-121">-ApiVersion</span></span>
<span data-ttu-id="be3ec-122">指定資源提供者支援的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="be3ec-122">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="be3ec-123">您可以指定不同于預設版本的版本。</span><span class="sxs-lookup"><span data-stu-id="be3ec-123">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="be3ec-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be3ec-124">-DefaultProfile</span></span>
<span data-ttu-id="be3ec-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="be3ec-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be3ec-126">-識別碼</span><span class="sxs-lookup"><span data-stu-id="be3ec-126">-Id</span></span>
<span data-ttu-id="be3ec-127">指定要取得之資源群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="be3ec-127">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="be3ec-128">不允許通配字元。</span><span class="sxs-lookup"><span data-stu-id="be3ec-128">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be3ec-129">-位置</span><span class="sxs-lookup"><span data-stu-id="be3ec-129">-Location</span></span>
<span data-ttu-id="be3ec-130">指定要取得之資源群組的位置。</span><span class="sxs-lookup"><span data-stu-id="be3ec-130">Specifies the location of the resource group to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be3ec-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="be3ec-131">-Name</span></span>
<span data-ttu-id="be3ec-132">指定要取得之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="be3ec-132">Specifies the name of the resource group to get.</span></span> <span data-ttu-id="be3ec-133">這個參數支援字串開頭和/或結尾的萬用字元。</span><span class="sxs-lookup"><span data-stu-id="be3ec-133">This parameter supports wildcards at the beginning and/or the end of the string.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupName
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be3ec-134">-預先</span><span class="sxs-lookup"><span data-stu-id="be3ec-134">-Pre</span></span>
<span data-ttu-id="be3ec-135">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="be3ec-135">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="be3ec-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="be3ec-136">-Tag</span></span>
<span data-ttu-id="be3ec-137">[標記 hashtable] 來篩選資源群組的依據。</span><span class="sxs-lookup"><span data-stu-id="be3ec-137">The tag hashtable to filter resource groups by.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: GetByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be3ec-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be3ec-138">CommonParameters</span></span>
<span data-ttu-id="be3ec-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="be3ec-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be3ec-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="be3ec-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be3ec-141">輸入</span><span class="sxs-lookup"><span data-stu-id="be3ec-141">INPUTS</span></span>

### <span data-ttu-id="be3ec-142">所有</span><span class="sxs-lookup"><span data-stu-id="be3ec-142">None</span></span>

## <span data-ttu-id="be3ec-143">輸出</span><span class="sxs-lookup"><span data-stu-id="be3ec-143">OUTPUTS</span></span>

### <span data-ttu-id="be3ec-144">PSResourceGroup 中的 ResourceManagement</span><span class="sxs-lookup"><span data-stu-id="be3ec-144">Microsoft.Azure.Commands.ResourceManagement.PSResourceGroup</span></span>

## <span data-ttu-id="be3ec-145">筆記</span><span class="sxs-lookup"><span data-stu-id="be3ec-145">NOTES</span></span>

## <span data-ttu-id="be3ec-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="be3ec-146">RELATED LINKS</span></span>

[<span data-ttu-id="be3ec-147">新-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="be3ec-147">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="be3ec-148">移除-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="be3ec-148">Remove-AzureRmResourceGroup</span></span>](./Remove-AzureRmResourceGroup.md)

[<span data-ttu-id="be3ec-149">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="be3ec-149">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)


