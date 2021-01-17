---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 880D321E-30F2-4CAE-B14A-5F6DD8E1DB99
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroup.md
ms.openlocfilehash: e53e5311b4553dc3803a4a6d9ac31d6a2569bbc0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98437188"
---
# <span data-ttu-id="c6108-101">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c6108-101">Remove-AzResourceGroup</span></span>

## <span data-ttu-id="c6108-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c6108-102">SYNOPSIS</span></span>
<span data-ttu-id="c6108-103">移除 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="c6108-103">Removes a resource group.</span></span>

## <span data-ttu-id="c6108-104">句法</span><span class="sxs-lookup"><span data-stu-id="c6108-104">SYNTAX</span></span>

### <span data-ttu-id="c6108-105">RemoveByResourceGroupName (預設) </span><span class="sxs-lookup"><span data-stu-id="c6108-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroup [-Name] <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6108-106">RemoveByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="c6108-106">RemoveByResourceGroupId</span></span>
```
Remove-AzResourceGroup -Id <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6108-107">說明</span><span class="sxs-lookup"><span data-stu-id="c6108-107">DESCRIPTION</span></span>
<span data-ttu-id="c6108-108">**AzResourceGroup** Cmdlet 會從目前的訂閱中移除 Azure 資源群組及其資源。</span><span class="sxs-lookup"><span data-stu-id="c6108-108">The **Remove-AzResourceGroup** cmdlet removes an Azure resource group and its resources from the current subscription.</span></span>
<span data-ttu-id="c6108-109">若要刪除資源，但要保留資源群組，請使用 Remove-AzResource Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c6108-109">To delete a resource, but leave the resource group, use the Remove-AzResource cmdlet.</span></span>

## <span data-ttu-id="c6108-110">示例</span><span class="sxs-lookup"><span data-stu-id="c6108-110">EXAMPLES</span></span>

### <span data-ttu-id="c6108-111">範例1：移除資源群組</span><span class="sxs-lookup"><span data-stu-id="c6108-111">Example 1: Remove a resource group</span></span>
```
PS C:\>Remove-AzResourceGroup -Name "ContosoRG01"
```

<span data-ttu-id="c6108-112">這個命令會從訂閱中移除 ContosoRG01 資源群組。</span><span class="sxs-lookup"><span data-stu-id="c6108-112">This command removes the ContosoRG01 resource group from the subscription.</span></span>
<span data-ttu-id="c6108-113">此 Cmdlet 會提示您進行確認，且不會傳回輸出。</span><span class="sxs-lookup"><span data-stu-id="c6108-113">The cmdlet prompts you for confirmation and returns no output.</span></span>

### <span data-ttu-id="c6108-114">範例2：移除資源群組而不進行確認</span><span class="sxs-lookup"><span data-stu-id="c6108-114">Example 2: Remove a resource group without confirmation</span></span>
```
PS C:\>Get-AzResourceGroup -Name "ContosoRG01" | Remove-AzResourceGroup -Force
```

<span data-ttu-id="c6108-115">這個命令會使用 Get-AzResourceGroup Cmdlet 來取得資源群組 ContosoRG01，然後透過使用管線運算子將它傳遞給 **Remove-AzResourceGroup** 。</span><span class="sxs-lookup"><span data-stu-id="c6108-115">This command uses the Get-AzResourceGroup cmdlet to get the resource group ContosoRG01, and then passes it to **Remove-AzResourceGroup** by using the pipeline operator.</span></span> <span data-ttu-id="c6108-116">*Force* 參數會取消確認提示。</span><span class="sxs-lookup"><span data-stu-id="c6108-116">The *Force* parameter suppresses the confirmation prompt.</span></span>

### <span data-ttu-id="c6108-117">範例3：移除所有資源群組</span><span class="sxs-lookup"><span data-stu-id="c6108-117">Example 3: Remove all resource groups</span></span>
```
PS C:\>Get-AzResourceGroup | Remove-AzResourceGroup
```

<span data-ttu-id="c6108-118">這個命令會使用 **AzResourceGroup** Cmdlet 取得所有資源群組，然後透過使用管線運算子將它們傳遞給 **Remove-AzResourceGroup** 。</span><span class="sxs-lookup"><span data-stu-id="c6108-118">This command uses the **Get-AzResourceGroup** cmdlet to get all resource groups, and then passes them to **Remove-AzResourceGroup** by using the pipeline operator.</span></span>

## <span data-ttu-id="c6108-119">參數</span><span class="sxs-lookup"><span data-stu-id="c6108-119">PARAMETERS</span></span>

### <span data-ttu-id="c6108-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c6108-120">-ApiVersion</span></span>
<span data-ttu-id="c6108-121">指定資源提供者支援的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="c6108-121">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="c6108-122">您可以指定不同于預設版本的版本。</span><span class="sxs-lookup"><span data-stu-id="c6108-122">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="c6108-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c6108-123">-AsJob</span></span>
<span data-ttu-id="c6108-124">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c6108-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c6108-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6108-125">-DefaultProfile</span></span>
<span data-ttu-id="c6108-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c6108-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c6108-127">-Force</span><span class="sxs-lookup"><span data-stu-id="c6108-127">-Force</span></span>
<span data-ttu-id="c6108-128">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="c6108-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c6108-129">-識別碼</span><span class="sxs-lookup"><span data-stu-id="c6108-129">-Id</span></span>
<span data-ttu-id="c6108-130">指定要移除之資源群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c6108-130">Specifies the ID of resource group to remove.</span></span>
<span data-ttu-id="c6108-131">不允許通配字元。</span><span class="sxs-lookup"><span data-stu-id="c6108-131">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6108-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="c6108-132">-Name</span></span>
<span data-ttu-id="c6108-133">指定要移除之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c6108-133">Specifies the names of resource groups to remove.</span></span>
<span data-ttu-id="c6108-134">不允許通配字元。</span><span class="sxs-lookup"><span data-stu-id="c6108-134">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6108-135">-預先</span><span class="sxs-lookup"><span data-stu-id="c6108-135">-Pre</span></span>
<span data-ttu-id="c6108-136">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="c6108-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c6108-137">-確認</span><span class="sxs-lookup"><span data-stu-id="c6108-137">-Confirm</span></span>
<span data-ttu-id="c6108-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c6108-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6108-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6108-139">-WhatIf</span></span>
<span data-ttu-id="c6108-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c6108-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6108-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c6108-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6108-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6108-142">CommonParameters</span></span>
<span data-ttu-id="c6108-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c6108-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6108-144">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c6108-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6108-145">輸入</span><span class="sxs-lookup"><span data-stu-id="c6108-145">INPUTS</span></span>

### <span data-ttu-id="c6108-146">System.object</span><span class="sxs-lookup"><span data-stu-id="c6108-146">System.String</span></span>

## <span data-ttu-id="c6108-147">輸出</span><span class="sxs-lookup"><span data-stu-id="c6108-147">OUTPUTS</span></span>

### <span data-ttu-id="c6108-148">System.object</span><span class="sxs-lookup"><span data-stu-id="c6108-148">System.Boolean</span></span>

## <span data-ttu-id="c6108-149">筆記</span><span class="sxs-lookup"><span data-stu-id="c6108-149">NOTES</span></span>

## <span data-ttu-id="c6108-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="c6108-150">RELATED LINKS</span></span>

[<span data-ttu-id="c6108-151">AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c6108-151">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="c6108-152">新-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c6108-152">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="c6108-153">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c6108-153">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)


