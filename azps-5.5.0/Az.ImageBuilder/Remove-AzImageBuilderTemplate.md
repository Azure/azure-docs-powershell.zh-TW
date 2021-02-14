---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/remove-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Remove-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Remove-AzImageBuilderTemplate.md
ms.openlocfilehash: 998c4f05e8b6a03749a4872e3f4b069e29ef634d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100136186"
---
# <span data-ttu-id="3df3a-101">Remove-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="3df3a-101">Remove-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="3df3a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3df3a-102">SYNOPSIS</span></span>
<span data-ttu-id="3df3a-103">刪除虛擬機器影像範本</span><span class="sxs-lookup"><span data-stu-id="3df3a-103">Delete a virtual machine image template</span></span>

## <span data-ttu-id="3df3a-104">句法</span><span class="sxs-lookup"><span data-stu-id="3df3a-104">SYNTAX</span></span>

### <span data-ttu-id="3df3a-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="3df3a-105">Delete (Default)</span></span>
```
Remove-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="3df3a-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3df3a-106">DeleteViaIdentity</span></span>
```
Remove-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3df3a-107">說明</span><span class="sxs-lookup"><span data-stu-id="3df3a-107">DESCRIPTION</span></span>
<span data-ttu-id="3df3a-108">刪除虛擬機器影像範本</span><span class="sxs-lookup"><span data-stu-id="3df3a-108">Delete a virtual machine image template</span></span>

## <span data-ttu-id="3df3a-109">示例</span><span class="sxs-lookup"><span data-stu-id="3df3a-109">EXAMPLES</span></span>

### <span data-ttu-id="3df3a-110">範例1：移除影像範本</span><span class="sxs-lookup"><span data-stu-id="3df3a-110">Example 1: Remove a image template</span></span>
```powershell
PS C:\> Remove-AzImageBuilderTemplate -ImageTemplateName template-name-dmt6ze -ResourceGroupName wyunchi-imagebuilder

```

<span data-ttu-id="3df3a-111">這個命令會移除影像範本。</span><span class="sxs-lookup"><span data-stu-id="3df3a-111">This command removes a image template.</span></span>

### <span data-ttu-id="3df3a-112">範例2：移除影像範本</span><span class="sxs-lookup"><span data-stu-id="3df3a-112">Example 2: Remove a image template</span></span>
```powershell
PS C:\> $template = Get-AzImageBuilderTemplate -ImageTemplateName template-name-3uo8p6 -ResourceGroupName wyunchi-imagebuilder
PS C:\> Remove-AzImageBuilderTemplate -InputObject $template

```

<span data-ttu-id="3df3a-113">這個命令會移除影像範本。</span><span class="sxs-lookup"><span data-stu-id="3df3a-113">This command removes a image template.</span></span>

## <span data-ttu-id="3df3a-114">參數</span><span class="sxs-lookup"><span data-stu-id="3df3a-114">PARAMETERS</span></span>

### <span data-ttu-id="3df3a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3df3a-115">-AsJob</span></span>
<span data-ttu-id="3df3a-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="3df3a-116">Run the command as a job</span></span>

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

### <span data-ttu-id="3df3a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3df3a-117">-DefaultProfile</span></span>
<span data-ttu-id="3df3a-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3df3a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3df3a-119">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="3df3a-119">-ImageTemplateName</span></span>
<span data-ttu-id="3df3a-120">影像範本的名稱</span><span class="sxs-lookup"><span data-stu-id="3df3a-120">The name of the image Template</span></span>

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

### <span data-ttu-id="3df3a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3df3a-121">-InputObject</span></span>
<span data-ttu-id="3df3a-122">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="3df3a-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3df3a-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3df3a-123">-NoWait</span></span>
<span data-ttu-id="3df3a-124">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="3df3a-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3df3a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3df3a-125">-PassThru</span></span>
<span data-ttu-id="3df3a-126">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="3df3a-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3df3a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3df3a-127">-ResourceGroupName</span></span>
<span data-ttu-id="3df3a-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3df3a-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="3df3a-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3df3a-129">-SubscriptionId</span></span>
<span data-ttu-id="3df3a-130">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="3df3a-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3df3a-131">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="3df3a-131">The subscription Id forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3df3a-132">-確認</span><span class="sxs-lookup"><span data-stu-id="3df3a-132">-Confirm</span></span>
<span data-ttu-id="3df3a-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3df3a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3df3a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3df3a-134">-WhatIf</span></span>
<span data-ttu-id="3df3a-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3df3a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3df3a-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3df3a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3df3a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3df3a-137">CommonParameters</span></span>
<span data-ttu-id="3df3a-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3df3a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3df3a-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3df3a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3df3a-140">輸入</span><span class="sxs-lookup"><span data-stu-id="3df3a-140">INPUTS</span></span>

### <span data-ttu-id="3df3a-141">IImageBuilderIdentity （ImageBuilder）的</span><span class="sxs-lookup"><span data-stu-id="3df3a-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="3df3a-142">輸出</span><span class="sxs-lookup"><span data-stu-id="3df3a-142">OUTPUTS</span></span>

### <span data-ttu-id="3df3a-143">System.object</span><span class="sxs-lookup"><span data-stu-id="3df3a-143">System.Boolean</span></span>

## <span data-ttu-id="3df3a-144">筆記</span><span class="sxs-lookup"><span data-stu-id="3df3a-144">NOTES</span></span>

<span data-ttu-id="3df3a-145">別名</span><span class="sxs-lookup"><span data-stu-id="3df3a-145">ALIASES</span></span>

<span data-ttu-id="3df3a-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="3df3a-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3df3a-147">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="3df3a-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3df3a-148">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="3df3a-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3df3a-149">INPUTOBJECT <IImageBuilderIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="3df3a-149">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3df3a-150">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="3df3a-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3df3a-151">`[ImageTemplateName <String>]`：影像範本的名稱</span><span class="sxs-lookup"><span data-stu-id="3df3a-151">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="3df3a-152">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3df3a-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="3df3a-153">`[RunOutputName <String>]`：執行輸出的名稱</span><span class="sxs-lookup"><span data-stu-id="3df3a-153">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="3df3a-154">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="3df3a-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="3df3a-155">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="3df3a-155">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="3df3a-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="3df3a-156">RELATED LINKS</span></span>

