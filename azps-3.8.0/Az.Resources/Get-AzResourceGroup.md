---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
ms.openlocfilehash: dc619aacd4089ce854eb5d342c2308a38a60cb28
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959858"
---
# <span data-ttu-id="cfa13-101">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cfa13-101">Get-AzResourceGroup</span></span>

## <span data-ttu-id="cfa13-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cfa13-102">SYNOPSIS</span></span>
<span data-ttu-id="cfa13-103">取得資源群組。</span><span class="sxs-lookup"><span data-stu-id="cfa13-103">Gets resource groups.</span></span>

## <span data-ttu-id="cfa13-104">句法</span><span class="sxs-lookup"><span data-stu-id="cfa13-104">SYNTAX</span></span>

### <span data-ttu-id="cfa13-105">GetByResourceGroupName (預設) </span><span class="sxs-lookup"><span data-stu-id="cfa13-105">GetByResourceGroupName (Default)</span></span>
```
Get-AzResourceGroup [[-Name] <String>] [[-Location] <String>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cfa13-106">GetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="cfa13-106">GetByResourceGroupId</span></span>
```
Get-AzResourceGroup [[-Location] <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cfa13-107">說明</span><span class="sxs-lookup"><span data-stu-id="cfa13-107">DESCRIPTION</span></span>
<span data-ttu-id="cfa13-108">**AzResourceGroup** Cmdlet 會在目前的訂閱中取得 Azure 資源群組。</span><span class="sxs-lookup"><span data-stu-id="cfa13-108">The **Get-AzResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="cfa13-109">您可以取得所有資源群組，或是依名稱或其他屬性來指定資源群組。</span><span class="sxs-lookup"><span data-stu-id="cfa13-109">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="cfa13-110">根據預設，這個 Cmdlet 會取得目前訂閱中的所有資源群組。</span><span class="sxs-lookup"><span data-stu-id="cfa13-110">By default, this cmdlet gets all resource groups in the current subscription.</span></span>
<span data-ttu-id="cfa13-111">如需有關 Azure 資源和 Azure 資源群組的詳細資訊，請參閱 New-AzResourceGroup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cfa13-111">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>

## <span data-ttu-id="cfa13-112">示例</span><span class="sxs-lookup"><span data-stu-id="cfa13-112">EXAMPLES</span></span>

### <span data-ttu-id="cfa13-113">範例1：依名稱取得資源群組</span><span class="sxs-lookup"><span data-stu-id="cfa13-113">Example 1: Get a resource group by name</span></span>
```
PS C:\>Get-AzResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="cfa13-114">這個命令會在您的訂閱中取得名為 EngineerBlog 的 Azure 資源群組。</span><span class="sxs-lookup"><span data-stu-id="cfa13-114">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="cfa13-115">範例2：取得資源群組的所有標籤</span><span class="sxs-lookup"><span data-stu-id="cfa13-115">Example 2: Get all tags of a resource group</span></span>
```
PS C:\>(Get-AzResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="cfa13-116">這個命令會取得名為 ContosoRG 的資源群組，並顯示與該群組相關聯的標籤。</span><span class="sxs-lookup"><span data-stu-id="cfa13-116">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

### <span data-ttu-id="cfa13-117">範例3：依位置顯示資源群組</span><span class="sxs-lookup"><span data-stu-id="cfa13-117">Example 3: Show the Resource groups by location</span></span>
```
PS C:\> Get-AzResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### <span data-ttu-id="cfa13-118">範例4：顯示特定位置中所有資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="cfa13-118">Example 4: Show the names of all the Resource groups in a particular location</span></span>
```
PS C:\> Get-AzResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### <span data-ttu-id="cfa13-119">範例5：顯示其名稱以 Web 內容開頭的資源群組</span><span class="sxs-lookup"><span data-stu-id="cfa13-119">Example 5: Show the Resource groups whose names begin with WebServer</span></span>
```
PS C:\> Get-AzResourceGroup | Where ResourceGroupName -like WebServer*
```

### <span data-ttu-id="cfa13-120">範例6：依名稱取得資源群組</span><span class="sxs-lookup"><span data-stu-id="cfa13-120">Example 6: Get a resource group by name</span></span>
```
PS C:\> Get-AzResourceGroup -Name "EngineerBlog*"
```

<span data-ttu-id="cfa13-121">這個命令會在您的訂閱中取得以 "EngineerBlog" 開頭的 Azure 資源群組。</span><span class="sxs-lookup"><span data-stu-id="cfa13-121">This command gets the Azure resource group in your subscription that start with "EngineerBlog".</span></span>

## <span data-ttu-id="cfa13-122">參數</span><span class="sxs-lookup"><span data-stu-id="cfa13-122">PARAMETERS</span></span>

### <span data-ttu-id="cfa13-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="cfa13-123">-ApiVersion</span></span>
<span data-ttu-id="cfa13-124">指定資源提供者支援的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="cfa13-124">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="cfa13-125">您可以指定不同于預設版本的版本。</span><span class="sxs-lookup"><span data-stu-id="cfa13-125">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="cfa13-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfa13-126">-DefaultProfile</span></span>
<span data-ttu-id="cfa13-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="cfa13-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cfa13-128">-識別碼</span><span class="sxs-lookup"><span data-stu-id="cfa13-128">-Id</span></span>
<span data-ttu-id="cfa13-129">指定要取得之資源群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="cfa13-129">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="cfa13-130">不允許通配字元。</span><span class="sxs-lookup"><span data-stu-id="cfa13-130">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="cfa13-131">-位置</span><span class="sxs-lookup"><span data-stu-id="cfa13-131">-Location</span></span>
<span data-ttu-id="cfa13-132">指定要取得之資源群組的位置。</span><span class="sxs-lookup"><span data-stu-id="cfa13-132">Specifies the location of the resource group to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfa13-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="cfa13-133">-Name</span></span>
<span data-ttu-id="cfa13-134">指定要取得之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cfa13-134">Specifies the name of the resource group to get.</span></span> <span data-ttu-id="cfa13-135">這個參數支援字串開頭和/或結尾的萬用字元。</span><span class="sxs-lookup"><span data-stu-id="cfa13-135">This parameter supports wildcards at the beginning and/or the end of the string.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupName
Aliases: ResourceGroupName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="cfa13-136">-預先</span><span class="sxs-lookup"><span data-stu-id="cfa13-136">-Pre</span></span>
<span data-ttu-id="cfa13-137">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="cfa13-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="cfa13-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="cfa13-138">-Tag</span></span>
<span data-ttu-id="cfa13-139">[標記 hashtable] 來篩選資源群組的依據。</span><span class="sxs-lookup"><span data-stu-id="cfa13-139">The tag hashtable to filter resource groups by.</span></span>

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

### <span data-ttu-id="cfa13-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfa13-140">CommonParameters</span></span>
<span data-ttu-id="cfa13-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cfa13-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfa13-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cfa13-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfa13-143">輸入</span><span class="sxs-lookup"><span data-stu-id="cfa13-143">INPUTS</span></span>

### <span data-ttu-id="cfa13-144">System.object</span><span class="sxs-lookup"><span data-stu-id="cfa13-144">System.String</span></span>

### <span data-ttu-id="cfa13-145">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="cfa13-145">System.Collections.Hashtable</span></span>

## <span data-ttu-id="cfa13-146">輸出</span><span class="sxs-lookup"><span data-stu-id="cfa13-146">OUTPUTS</span></span>

### <span data-ttu-id="cfa13-147">PSResourceGroup 中的 SdkModels （）</span><span class="sxs-lookup"><span data-stu-id="cfa13-147">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="cfa13-148">筆記</span><span class="sxs-lookup"><span data-stu-id="cfa13-148">NOTES</span></span>

## <span data-ttu-id="cfa13-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="cfa13-149">RELATED LINKS</span></span>

[<span data-ttu-id="cfa13-150">新-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cfa13-150">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="cfa13-151">移除-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cfa13-151">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)

[<span data-ttu-id="cfa13-152">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cfa13-152">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)


