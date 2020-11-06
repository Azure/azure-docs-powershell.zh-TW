---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 880D321E-30F2-4CAE-B14A-5F6DD8E1DB99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroup.md
ms.openlocfilehash: ce028e52d893372f4a668a278466d4cdc51655f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450501"
---
# <span data-ttu-id="fdb9a-101">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fdb9a-101">Remove-AzureRmResourceGroup</span></span>

## <span data-ttu-id="fdb9a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fdb9a-102">SYNOPSIS</span></span>
<span data-ttu-id="fdb9a-103">移除 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="fdb9a-103">Removes a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdb9a-104">句法</span><span class="sxs-lookup"><span data-stu-id="fdb9a-104">SYNTAX</span></span>

### <span data-ttu-id="fdb9a-105">RemoveByResourceGroupName (預設) </span><span class="sxs-lookup"><span data-stu-id="fdb9a-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzureRmResourceGroup [-Name] <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdb9a-106">RemoveByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="fdb9a-106">RemoveByResourceGroupId</span></span>
```
Remove-AzureRmResourceGroup [-Id] <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdb9a-107">說明</span><span class="sxs-lookup"><span data-stu-id="fdb9a-107">DESCRIPTION</span></span>
<span data-ttu-id="fdb9a-108">**AzureRmResourceGroup** Cmdlet 會從目前的訂閱中移除 Azure 資源群組及其資源。</span><span class="sxs-lookup"><span data-stu-id="fdb9a-108">The **Remove-AzureRmResourceGroup** cmdlet removes an Azure resource group and its resources from the current subscription.</span></span>
<span data-ttu-id="fdb9a-109">若要刪除資源，但要保留資源群組，請使用 Remove-AzureRmResource Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fdb9a-109">To delete a resource, but leave the resource group, use the Remove-AzureRmResource cmdlet.</span></span>

## <span data-ttu-id="fdb9a-110">示例</span><span class="sxs-lookup"><span data-stu-id="fdb9a-110">EXAMPLES</span></span>

### <span data-ttu-id="fdb9a-111">範例1：移除資源群組</span><span class="sxs-lookup"><span data-stu-id="fdb9a-111">Example 1: Remove a resource group</span></span>
```
PS C:\>Remove-AzureRmResourceGroup -Name "ContosoRG01"
```

<span data-ttu-id="fdb9a-112">這個命令會從訂閱中移除 ContosoRG01 資源群組。</span><span class="sxs-lookup"><span data-stu-id="fdb9a-112">This command removes the ContosoRG01 resource group from the subscription.</span></span>
<span data-ttu-id="fdb9a-113">此 Cmdlet 會提示您進行確認，且不會傳回輸出。</span><span class="sxs-lookup"><span data-stu-id="fdb9a-113">The cmdlet prompts you for confirmation and returns no output.</span></span>

### <span data-ttu-id="fdb9a-114">範例2：移除資源群組而不進行確認</span><span class="sxs-lookup"><span data-stu-id="fdb9a-114">Example 2: Remove a resource group without confirmation</span></span>
```
PS C:\>Get-AzureRmResourceGroup -Name "ContosoRG01" | Remove-AzureRmResourceGroup -Verbose -Force
```

<span data-ttu-id="fdb9a-115">這個命令會使用 Get-AzureRmResourceGroup Cmdlet 來取得資源群組 ContosoRG01，然後透過使用管線運算子將它傳遞給 **Remove-AzureRmResourceGroup** 。</span><span class="sxs-lookup"><span data-stu-id="fdb9a-115">This command uses the Get-AzureRmResourceGroup cmdlet to get the resource group ContosoRG01, and then passes it to **Remove-AzureRmResourceGroup** by using the pipeline operator.</span></span>
<span data-ttu-id="fdb9a-116">*詳細* 的常見參數會取得操作的狀態資訊，而 *Force* 參數則會取消確認提示。</span><span class="sxs-lookup"><span data-stu-id="fdb9a-116">The *Verbose* common parameter gets status information about the operation, and the *Force* parameter suppresses the confirmation prompt.</span></span>

### <span data-ttu-id="fdb9a-117">範例3：移除所有資源群組</span><span class="sxs-lookup"><span data-stu-id="fdb9a-117">Example 3: Remove all resource groups</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Remove-AzureRmResourceGroup
```

<span data-ttu-id="fdb9a-118">這個命令會使用 **AzureRmResourceGroup** Cmdlet 取得所有資源群組，然後透過使用管線運算子將它們傳遞給 **Remove-AzureRmResourceGroup** 。</span><span class="sxs-lookup"><span data-stu-id="fdb9a-118">This command uses the **Get-AzureRmResourceGroup** cmdlet to get all resource groups, and then passes them to **Remove-AzureRmResourceGroup** by using the pipeline operator.</span></span>

## <span data-ttu-id="fdb9a-119">參數</span><span class="sxs-lookup"><span data-stu-id="fdb9a-119">PARAMETERS</span></span>

### <span data-ttu-id="fdb9a-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="fdb9a-120">-ApiVersion</span></span>
<span data-ttu-id="fdb9a-121">指定資源提供者支援的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="fdb9a-121">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="fdb9a-122">您可以指定不同于預設版本的版本。</span><span class="sxs-lookup"><span data-stu-id="fdb9a-122">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="fdb9a-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fdb9a-123">-AsJob</span></span>
<span data-ttu-id="fdb9a-124">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="fdb9a-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fdb9a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdb9a-125">-DefaultProfile</span></span>
<span data-ttu-id="fdb9a-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="fdb9a-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fdb9a-127">-Force</span><span class="sxs-lookup"><span data-stu-id="fdb9a-127">-Force</span></span>
<span data-ttu-id="fdb9a-128">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="fdb9a-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fdb9a-129">-識別碼</span><span class="sxs-lookup"><span data-stu-id="fdb9a-129">-Id</span></span>
<span data-ttu-id="fdb9a-130">指定要移除之資源群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="fdb9a-130">Specifies the ID of resource group to remove.</span></span>
<span data-ttu-id="fdb9a-131">不允許通配字元。</span><span class="sxs-lookup"><span data-stu-id="fdb9a-131">Wildcard characters are not permitted.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdb9a-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="fdb9a-132">-Name</span></span>
<span data-ttu-id="fdb9a-133">指定要移除之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fdb9a-133">Specifies the names of resource groups to remove.</span></span>
<span data-ttu-id="fdb9a-134">不允許通配字元。</span><span class="sxs-lookup"><span data-stu-id="fdb9a-134">Wildcard characters are not permitted.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdb9a-135">-預先</span><span class="sxs-lookup"><span data-stu-id="fdb9a-135">-Pre</span></span>
<span data-ttu-id="fdb9a-136">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="fdb9a-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="fdb9a-137">-確認</span><span class="sxs-lookup"><span data-stu-id="fdb9a-137">-Confirm</span></span>
<span data-ttu-id="fdb9a-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fdb9a-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdb9a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdb9a-139">-WhatIf</span></span>
<span data-ttu-id="fdb9a-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fdb9a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fdb9a-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fdb9a-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdb9a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdb9a-142">CommonParameters</span></span>
<span data-ttu-id="fdb9a-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fdb9a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdb9a-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fdb9a-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdb9a-145">輸入</span><span class="sxs-lookup"><span data-stu-id="fdb9a-145">INPUTS</span></span>

### <span data-ttu-id="fdb9a-146">所有</span><span class="sxs-lookup"><span data-stu-id="fdb9a-146">None</span></span>

## <span data-ttu-id="fdb9a-147">輸出</span><span class="sxs-lookup"><span data-stu-id="fdb9a-147">OUTPUTS</span></span>

### <span data-ttu-id="fdb9a-148">所有</span><span class="sxs-lookup"><span data-stu-id="fdb9a-148">None</span></span>

## <span data-ttu-id="fdb9a-149">筆記</span><span class="sxs-lookup"><span data-stu-id="fdb9a-149">NOTES</span></span>

## <span data-ttu-id="fdb9a-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="fdb9a-150">RELATED LINKS</span></span>

[<span data-ttu-id="fdb9a-151">AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fdb9a-151">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="fdb9a-152">新-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fdb9a-152">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="fdb9a-153">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fdb9a-153">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)


