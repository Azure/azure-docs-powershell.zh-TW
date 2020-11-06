---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 880D321E-30F2-4CAE-B14A-5F6DD8E1DB99
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroup.md
ms.openlocfilehash: 6938cf80f3fa6fb20252e1e4a212133ecd1c62a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452367"
---
# <span data-ttu-id="f55b8-101">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f55b8-101">Remove-AzureRmResourceGroup</span></span>

## <span data-ttu-id="f55b8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f55b8-102">SYNOPSIS</span></span>
<span data-ttu-id="f55b8-103">移除 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="f55b8-103">Removes a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f55b8-104">句法</span><span class="sxs-lookup"><span data-stu-id="f55b8-104">SYNTAX</span></span>

### <span data-ttu-id="f55b8-105">根據名稱列出 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="f55b8-105">Lists the resource group based in the name.</span></span> <span data-ttu-id="f55b8-106"> (預設) </span><span class="sxs-lookup"><span data-stu-id="f55b8-106">(Default)</span></span>
```
Remove-AzureRmResourceGroup [-Name] <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f55b8-107">根據 [識別碼] 列出 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="f55b8-107">Lists the resource group based in the Id.</span></span>
```
Remove-AzureRmResourceGroup [-Id] <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f55b8-108">說明</span><span class="sxs-lookup"><span data-stu-id="f55b8-108">DESCRIPTION</span></span>
<span data-ttu-id="f55b8-109">**AzureRmResourceGroup** Cmdlet 會從目前的訂閱中移除 Azure 資源群組及其資源。</span><span class="sxs-lookup"><span data-stu-id="f55b8-109">The **Remove-AzureRmResourceGroup** cmdlet removes an Azure resource group and its resources from the current subscription.</span></span>
<span data-ttu-id="f55b8-110">若要刪除資源，但要保留資源群組，請使用 Remove-AzureRmResource Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f55b8-110">To delete a resource, but leave the resource group, use the Remove-AzureRmResource cmdlet.</span></span>

## <span data-ttu-id="f55b8-111">示例</span><span class="sxs-lookup"><span data-stu-id="f55b8-111">EXAMPLES</span></span>

### <span data-ttu-id="f55b8-112">範例1：移除資源群組</span><span class="sxs-lookup"><span data-stu-id="f55b8-112">Example 1: Remove a resource group</span></span>
```
PS C:\>Remove-AzureRmResourceGroup -Name "ContosoRG01"
```

<span data-ttu-id="f55b8-113">這個命令會從訂閱中移除 ContosoRG01 資源群組。</span><span class="sxs-lookup"><span data-stu-id="f55b8-113">This command removes the ContosoRG01 resource group from the subscription.</span></span>
<span data-ttu-id="f55b8-114">此 Cmdlet 會提示您進行確認，且不會傳回輸出。</span><span class="sxs-lookup"><span data-stu-id="f55b8-114">The cmdlet prompts you for confirmation and returns no output.</span></span>

### <span data-ttu-id="f55b8-115">範例2：移除資源群組而不進行確認</span><span class="sxs-lookup"><span data-stu-id="f55b8-115">Example 2: Remove a resource group without confirmation</span></span>
```
PS C:\>Get-AzureRmResourceGroup -Name "ContosoRG01" | Remove-AzureRmResourceGroup -Verbose -Force
```

<span data-ttu-id="f55b8-116">這個命令會使用 Get-AzureRmResourceGroup Cmdlet 來取得資源群組 ContosoRG01，然後透過使用管線運算子將它傳遞給 **Remove-AzureRmResourceGroup** 。</span><span class="sxs-lookup"><span data-stu-id="f55b8-116">This command uses the Get-AzureRmResourceGroup cmdlet to get the resource group ContosoRG01, and then passes it to **Remove-AzureRmResourceGroup** by using the pipeline operator.</span></span>
<span data-ttu-id="f55b8-117">*詳細* 的常見參數會取得操作的狀態資訊，而 *Force* 參數則會取消確認提示。</span><span class="sxs-lookup"><span data-stu-id="f55b8-117">The *Verbose* common parameter gets status information about the operation, and the *Force* parameter suppresses the confirmation prompt.</span></span>

### <span data-ttu-id="f55b8-118">範例3：移除所有資源群組</span><span class="sxs-lookup"><span data-stu-id="f55b8-118">Example 3: Remove all resource groups</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Remove-AzureRmResourceGroup
```

<span data-ttu-id="f55b8-119">這個命令會使用 **AzureRmResourceGroup** Cmdlet 取得所有資源群組，然後透過使用管線運算子將它們傳遞給 **Remove-AzureRmResourceGroup** 。</span><span class="sxs-lookup"><span data-stu-id="f55b8-119">This command uses the **Get-AzureRmResourceGroup** cmdlet to get all resource groups, and then passes them to **Remove-AzureRmResourceGroup** by using the pipeline operator.</span></span>

## <span data-ttu-id="f55b8-120">參數</span><span class="sxs-lookup"><span data-stu-id="f55b8-120">PARAMETERS</span></span>

### <span data-ttu-id="f55b8-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f55b8-121">-ApiVersion</span></span>
<span data-ttu-id="f55b8-122">指定資源提供者支援的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="f55b8-122">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="f55b8-123">您可以指定不同于預設版本的版本。</span><span class="sxs-lookup"><span data-stu-id="f55b8-123">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="f55b8-124">-Force</span><span class="sxs-lookup"><span data-stu-id="f55b8-124">-Force</span></span>
<span data-ttu-id="f55b8-125">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="f55b8-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f55b8-126">-識別碼</span><span class="sxs-lookup"><span data-stu-id="f55b8-126">-Id</span></span>
<span data-ttu-id="f55b8-127">指定要移除之資源群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f55b8-127">Specifies the ID of resource group to remove.</span></span>
<span data-ttu-id="f55b8-128">不允許通配字元。</span><span class="sxs-lookup"><span data-stu-id="f55b8-128">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based in the Id.
Aliases: ResourceGroupId, ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f55b8-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="f55b8-129">-Name</span></span>
<span data-ttu-id="f55b8-130">指定要移除之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f55b8-130">Specifies the names of resource groups to remove.</span></span>
<span data-ttu-id="f55b8-131">不允許通配字元。</span><span class="sxs-lookup"><span data-stu-id="f55b8-131">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based in the name.
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f55b8-132">-預先</span><span class="sxs-lookup"><span data-stu-id="f55b8-132">-Pre</span></span>
<span data-ttu-id="f55b8-133">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="f55b8-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f55b8-134">-確認</span><span class="sxs-lookup"><span data-stu-id="f55b8-134">-Confirm</span></span>
<span data-ttu-id="f55b8-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f55b8-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f55b8-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f55b8-136">-WhatIf</span></span>
<span data-ttu-id="f55b8-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f55b8-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f55b8-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f55b8-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f55b8-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f55b8-139">-DefaultProfile</span></span>
<span data-ttu-id="f55b8-140">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f55b8-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f55b8-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f55b8-141">CommonParameters</span></span>
<span data-ttu-id="f55b8-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f55b8-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f55b8-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f55b8-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f55b8-144">輸入</span><span class="sxs-lookup"><span data-stu-id="f55b8-144">INPUTS</span></span>

### <span data-ttu-id="f55b8-145">所有</span><span class="sxs-lookup"><span data-stu-id="f55b8-145">None</span></span>

## <span data-ttu-id="f55b8-146">輸出</span><span class="sxs-lookup"><span data-stu-id="f55b8-146">OUTPUTS</span></span>

### <span data-ttu-id="f55b8-147">所有</span><span class="sxs-lookup"><span data-stu-id="f55b8-147">None</span></span>

## <span data-ttu-id="f55b8-148">筆記</span><span class="sxs-lookup"><span data-stu-id="f55b8-148">NOTES</span></span>

## <span data-ttu-id="f55b8-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="f55b8-149">RELATED LINKS</span></span>

[<span data-ttu-id="f55b8-150">AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f55b8-150">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="f55b8-151">新-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f55b8-151">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="f55b8-152">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f55b8-152">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)


