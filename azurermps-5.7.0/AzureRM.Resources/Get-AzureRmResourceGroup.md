---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroup.md
ms.openlocfilehash: f3924115d68d7e844503e076a214c95bf3d2239d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454139"
---
# <span data-ttu-id="5ebbb-101">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5ebbb-101">Get-AzureRmResourceGroup</span></span>

## <span data-ttu-id="5ebbb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5ebbb-102">SYNOPSIS</span></span>
<span data-ttu-id="5ebbb-103">取得資源群組。</span><span class="sxs-lookup"><span data-stu-id="5ebbb-103">Gets resource groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ebbb-104">句法</span><span class="sxs-lookup"><span data-stu-id="5ebbb-104">SYNTAX</span></span>

### <span data-ttu-id="5ebbb-105">GetByResourceGroupName (預設) </span><span class="sxs-lookup"><span data-stu-id="5ebbb-105">GetByResourceGroupName (Default)</span></span>
```
Get-AzureRmResourceGroup [-Name <String>] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ebbb-106">GetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="5ebbb-106">GetByResourceGroupId</span></span>
```
Get-AzureRmResourceGroup [-Location <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ebbb-107">說明</span><span class="sxs-lookup"><span data-stu-id="5ebbb-107">DESCRIPTION</span></span>
<span data-ttu-id="5ebbb-108">**AzureRmResourceGroup** Cmdlet 會在目前的訂閱中取得 Azure 資源群組。</span><span class="sxs-lookup"><span data-stu-id="5ebbb-108">The **Get-AzureRmResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="5ebbb-109">您可以取得所有資源群組，或是依名稱或其他屬性來指定資源群組。</span><span class="sxs-lookup"><span data-stu-id="5ebbb-109">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="5ebbb-110">根據預設，這個 Cmdlet 會取得目前訂閱中的所有資源群組。</span><span class="sxs-lookup"><span data-stu-id="5ebbb-110">By default, this cmdlet gets all resource groups in the current subscription.</span></span>

<span data-ttu-id="5ebbb-111">如需有關 Azure 資源和 Azure 資源群組的詳細資訊，請參閱 New-AzureRmResourceGroup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5ebbb-111">For more information about Azure resources and Azure resource groups, see the New-AzureRmResourceGroup cmdlet.</span></span>

## <span data-ttu-id="5ebbb-112">示例</span><span class="sxs-lookup"><span data-stu-id="5ebbb-112">EXAMPLES</span></span>

### <span data-ttu-id="5ebbb-113">範例1：依名稱取得資源群組</span><span class="sxs-lookup"><span data-stu-id="5ebbb-113">Example 1: Get a resource group by name</span></span>
```
PS C:\>Get-AzureRmResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="5ebbb-114">這個命令會在您的訂閱中取得名為 EngineerBlog 的 Azure 資源群組。</span><span class="sxs-lookup"><span data-stu-id="5ebbb-114">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="5ebbb-115">範例2：取得資源群組的所有標籤</span><span class="sxs-lookup"><span data-stu-id="5ebbb-115">Example 2: Get all tags of a resource group</span></span>
```
PS C:\>(Get-AzureRmResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="5ebbb-116">這個命令會取得名為 ContosoRG 的資源群組，並顯示與該群組相關聯的標籤。</span><span class="sxs-lookup"><span data-stu-id="5ebbb-116">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

### <span data-ttu-id="5ebbb-117">範例3：依位置顯示資源群組</span><span class="sxs-lookup"><span data-stu-id="5ebbb-117">Example 3: Show the Resource groups by location</span></span>
```
PS C:\> Get-AzureRmResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### <span data-ttu-id="5ebbb-118">範例4：顯示特定位置中所有資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="5ebbb-118">Example 4: Show the names of all the Resource groups in a particular location</span></span>
```
PS C:\> Get-AzureRmResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### <span data-ttu-id="5ebbb-119">範例5：顯示其名稱以 Web 內容開頭的資源群組</span><span class="sxs-lookup"><span data-stu-id="5ebbb-119">Example 5: Show the Resource groups whose names begin with WebServer</span></span>
```
PS C:\> Get-AzureRmResourceGroup | Where ResourceGroupName -like WebServer*
```

## <span data-ttu-id="5ebbb-120">參數</span><span class="sxs-lookup"><span data-stu-id="5ebbb-120">PARAMETERS</span></span>

### <span data-ttu-id="5ebbb-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5ebbb-121">-ApiVersion</span></span>
<span data-ttu-id="5ebbb-122">指定資源提供者支援的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="5ebbb-122">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="5ebbb-123">您可以指定不同于預設版本的版本。</span><span class="sxs-lookup"><span data-stu-id="5ebbb-123">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="5ebbb-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ebbb-124">-DefaultProfile</span></span>
<span data-ttu-id="5ebbb-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="5ebbb-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ebbb-126">-識別碼</span><span class="sxs-lookup"><span data-stu-id="5ebbb-126">-Id</span></span>
<span data-ttu-id="5ebbb-127">指定要取得之資源群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5ebbb-127">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="5ebbb-128">不允許通配字元。</span><span class="sxs-lookup"><span data-stu-id="5ebbb-128">Wildcard characters are not permitted.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ebbb-129">-位置</span><span class="sxs-lookup"><span data-stu-id="5ebbb-129">-Location</span></span>
<span data-ttu-id="5ebbb-130">指定要取得之資源群組的位置。</span><span class="sxs-lookup"><span data-stu-id="5ebbb-130">Specifies the location of the resource group to get.</span></span>

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

### <span data-ttu-id="5ebbb-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="5ebbb-131">-Name</span></span>
<span data-ttu-id="5ebbb-132">指定要取得之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ebbb-132">Specifies the name of the resource group to get.</span></span>
<span data-ttu-id="5ebbb-133">不允許通配字元。</span><span class="sxs-lookup"><span data-stu-id="5ebbb-133">Wildcard characters are not permitted.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceGroupName
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ebbb-134">-預先</span><span class="sxs-lookup"><span data-stu-id="5ebbb-134">-Pre</span></span>
<span data-ttu-id="5ebbb-135">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="5ebbb-135">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="5ebbb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ebbb-136">CommonParameters</span></span>
<span data-ttu-id="5ebbb-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5ebbb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ebbb-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5ebbb-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ebbb-139">輸入</span><span class="sxs-lookup"><span data-stu-id="5ebbb-139">INPUTS</span></span>

### <span data-ttu-id="5ebbb-140">字串</span><span class="sxs-lookup"><span data-stu-id="5ebbb-140">String</span></span>
<span data-ttu-id="5ebbb-141">您可以透過屬性名稱將輸入輸送至 Cmdlet，但不能依值進行。</span><span class="sxs-lookup"><span data-stu-id="5ebbb-141">You can pipe input to the cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="5ebbb-142">輸出</span><span class="sxs-lookup"><span data-stu-id="5ebbb-142">OUTPUTS</span></span>

### <span data-ttu-id="5ebbb-143">PSResourceGroup 中的 ResourceManagement</span><span class="sxs-lookup"><span data-stu-id="5ebbb-143">Microsoft.Azure.Commands.ResourceManagement.PSResourceGroup</span></span>
<span data-ttu-id="5ebbb-144">這個 Cmdlet 會傳回資源群組。</span><span class="sxs-lookup"><span data-stu-id="5ebbb-144">This cmdlet returns resource groups.</span></span>

## <span data-ttu-id="5ebbb-145">筆記</span><span class="sxs-lookup"><span data-stu-id="5ebbb-145">NOTES</span></span>

## <span data-ttu-id="5ebbb-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="5ebbb-146">RELATED LINKS</span></span>

[<span data-ttu-id="5ebbb-147">新-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5ebbb-147">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="5ebbb-148">移除-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5ebbb-148">Remove-AzureRmResourceGroup</span></span>](./Remove-AzureRmResourceGroup.md)

[<span data-ttu-id="5ebbb-149">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5ebbb-149">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)


