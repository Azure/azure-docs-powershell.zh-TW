---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/powershell/module/az.imagebuilder/remove-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Remove-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Remove-AzImageBuilderTemplate.md
ms.openlocfilehash: 3d22fa9626d7e0e6de8baf36a07ae679ffb9ed0a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917177"
---
# <span data-ttu-id="c48bf-101">Remove-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="c48bf-101">Remove-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="c48bf-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c48bf-102">SYNOPSIS</span></span>
<span data-ttu-id="c48bf-103">刪除虛擬機器映射範本</span><span class="sxs-lookup"><span data-stu-id="c48bf-103">Delete a virtual machine image template</span></span>

## <span data-ttu-id="c48bf-104">語法</span><span class="sxs-lookup"><span data-stu-id="c48bf-104">SYNTAX</span></span>

### <span data-ttu-id="c48bf-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="c48bf-105">Delete (Default)</span></span>
```
Remove-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="c48bf-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c48bf-106">DeleteViaIdentity</span></span>
```
Remove-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c48bf-107">描述</span><span class="sxs-lookup"><span data-stu-id="c48bf-107">DESCRIPTION</span></span>
<span data-ttu-id="c48bf-108">刪除虛擬機器映射範本</span><span class="sxs-lookup"><span data-stu-id="c48bf-108">Delete a virtual machine image template</span></span>

## <span data-ttu-id="c48bf-109">例子</span><span class="sxs-lookup"><span data-stu-id="c48bf-109">EXAMPLES</span></span>

### <span data-ttu-id="c48bf-110">範例 1：移除圖像範本</span><span class="sxs-lookup"><span data-stu-id="c48bf-110">Example 1: Remove a image template</span></span>
```powershell
PS C:\> Remove-AzImageBuilderTemplate -ImageTemplateName template-name-dmt6ze -ResourceGroupName wyunchi-imagebuilder

```

<span data-ttu-id="c48bf-111">此命令會移除圖像範本。</span><span class="sxs-lookup"><span data-stu-id="c48bf-111">This command removes a image template.</span></span>

### <span data-ttu-id="c48bf-112">範例 2：移除圖像範本</span><span class="sxs-lookup"><span data-stu-id="c48bf-112">Example 2: Remove a image template</span></span>
```powershell
PS C:\> $template = Get-AzImageBuilderTemplate -ImageTemplateName template-name-3uo8p6 -ResourceGroupName wyunchi-imagebuilder
PS C:\> Remove-AzImageBuilderTemplate -InputObject $template

```

<span data-ttu-id="c48bf-113">此命令會移除圖像範本。</span><span class="sxs-lookup"><span data-stu-id="c48bf-113">This command removes a image template.</span></span>

## <span data-ttu-id="c48bf-114">參數</span><span class="sxs-lookup"><span data-stu-id="c48bf-114">PARAMETERS</span></span>

### <span data-ttu-id="c48bf-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c48bf-115">-AsJob</span></span>
<span data-ttu-id="c48bf-116">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="c48bf-116">Run the command as a job</span></span>

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

### <span data-ttu-id="c48bf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c48bf-117">-DefaultProfile</span></span>
<span data-ttu-id="c48bf-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c48bf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c48bf-119">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="c48bf-119">-ImageTemplateName</span></span>
<span data-ttu-id="c48bf-120">圖像範本的名稱</span><span class="sxs-lookup"><span data-stu-id="c48bf-120">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c48bf-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c48bf-121">-InputObject</span></span>
<span data-ttu-id="c48bf-122">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="c48bf-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c48bf-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c48bf-123">-NoWait</span></span>
<span data-ttu-id="c48bf-124">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="c48bf-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c48bf-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c48bf-125">-PassThru</span></span>
<span data-ttu-id="c48bf-126">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="c48bf-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c48bf-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c48bf-127">-ResourceGroupName</span></span>
<span data-ttu-id="c48bf-128">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c48bf-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c48bf-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c48bf-129">-SubscriptionId</span></span>
<span data-ttu-id="c48bf-130">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="c48bf-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c48bf-131">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="c48bf-131">The subscription Id forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c48bf-132">-確認</span><span class="sxs-lookup"><span data-stu-id="c48bf-132">-Confirm</span></span>
<span data-ttu-id="c48bf-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c48bf-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c48bf-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c48bf-134">-WhatIf</span></span>
<span data-ttu-id="c48bf-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c48bf-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c48bf-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c48bf-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c48bf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c48bf-137">CommonParameters</span></span>
<span data-ttu-id="c48bf-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c48bf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c48bf-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c48bf-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c48bf-140">輸入</span><span class="sxs-lookup"><span data-stu-id="c48bf-140">INPUTS</span></span>

### <span data-ttu-id="c48bf-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.models.IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="c48bf-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="c48bf-142">輸出</span><span class="sxs-lookup"><span data-stu-id="c48bf-142">OUTPUTS</span></span>

### <span data-ttu-id="c48bf-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c48bf-143">System.Boolean</span></span>

## <span data-ttu-id="c48bf-144">筆記</span><span class="sxs-lookup"><span data-stu-id="c48bf-144">NOTES</span></span>

<span data-ttu-id="c48bf-145">別名</span><span class="sxs-lookup"><span data-stu-id="c48bf-145">ALIASES</span></span>

<span data-ttu-id="c48bf-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="c48bf-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c48bf-147">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="c48bf-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c48bf-148">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="c48bf-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c48bf-149">INPUTOBJECT： <IImageBuilderIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="c48bf-149">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c48bf-150">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="c48bf-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c48bf-151">`[ImageTemplateName <String>]`：圖像範本的名稱</span><span class="sxs-lookup"><span data-stu-id="c48bf-151">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="c48bf-152">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c48bf-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="c48bf-153">`[RunOutputName <String>]`：執行輸出的名稱</span><span class="sxs-lookup"><span data-stu-id="c48bf-153">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="c48bf-154">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="c48bf-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c48bf-155">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="c48bf-155">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="c48bf-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="c48bf-156">RELATED LINKS</span></span>

