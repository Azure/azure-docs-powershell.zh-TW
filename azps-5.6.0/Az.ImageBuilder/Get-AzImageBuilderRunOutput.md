---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/powershell/module/az.imagebuilder/get-azimagebuilderrunoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderRunOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderRunOutput.md
ms.openlocfilehash: 4f1c88e48847c1ecf560d7ed9d390131455b1d39
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917193"
---
# <span data-ttu-id="b8a39-101">Get-AzImageBuilderRunOutput</span><span class="sxs-lookup"><span data-stu-id="b8a39-101">Get-AzImageBuilderRunOutput</span></span>

## <span data-ttu-id="b8a39-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b8a39-102">SYNOPSIS</span></span>
<span data-ttu-id="b8a39-103">取得指定圖像範本資源的指定執行輸出</span><span class="sxs-lookup"><span data-stu-id="b8a39-103">Get the specified run output for the specified image template resource</span></span>

## <span data-ttu-id="b8a39-104">語法</span><span class="sxs-lookup"><span data-stu-id="b8a39-104">SYNTAX</span></span>

### <span data-ttu-id="b8a39-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="b8a39-105">List (Default)</span></span>
```
Get-AzImageBuilderRunOutput -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b8a39-106">獲取</span><span class="sxs-lookup"><span data-stu-id="b8a39-106">Get</span></span>
```
Get-AzImageBuilderRunOutput -ImageTemplateName <String> -ResourceGroupName <String> -RunOutputName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b8a39-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b8a39-107">GetViaIdentity</span></span>
```
Get-AzImageBuilderRunOutput -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b8a39-108">描述</span><span class="sxs-lookup"><span data-stu-id="b8a39-108">DESCRIPTION</span></span>
<span data-ttu-id="b8a39-109">取得指定圖像範本資源的指定執行輸出</span><span class="sxs-lookup"><span data-stu-id="b8a39-109">Get the specified run output for the specified image template resource</span></span>

## <span data-ttu-id="b8a39-110">例子</span><span class="sxs-lookup"><span data-stu-id="b8a39-110">EXAMPLES</span></span>

### <span data-ttu-id="b8a39-111">範例 1：在範本下列出所有執行結果</span><span class="sxs-lookup"><span data-stu-id="b8a39-111">Example 1: List all run results under a template</span></span>
```powershell
PS C:\> Get-AzImageBuilderRunOutput -ImageTemplateName lucas-imagetemplate -ResourceGroupName wyunchi-imagebuilder

Name          Type
----          ----
image_lucas_1 Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="b8a39-112">此命令會列出範本下的所有執行結果。</span><span class="sxs-lookup"><span data-stu-id="b8a39-112">This command lists all run results under a template.</span></span>

### <span data-ttu-id="b8a39-113">範例 2：在範本下取得執行結果</span><span class="sxs-lookup"><span data-stu-id="b8a39-113">Example 2: Get a run result under a template</span></span>
```powershell
PS C:\> Get-AzImageBuilderRunOutput -ImageTemplateName template-name-u7gjqx -ResourceGroupName wyunchi-imagebuilder -RunOutputName runout-template-name-u7gjqx 

Name                        Type
----                        ----
runout-template-name-u7gjqx Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="b8a39-114">此命令在範本下取得執行結果。</span><span class="sxs-lookup"><span data-stu-id="b8a39-114">This command gets a run result under a template.</span></span>

### <span data-ttu-id="b8a39-115">範例 3：在範本下取得執行結果</span><span class="sxs-lookup"><span data-stu-id="b8a39-115">Example 3: Get a run result under a template</span></span>
```powershell
PS C:\> $result = Get-AzImageBuilderRunOutput -ImageTemplateName template-name-u7gjqx -ResourceGroupName wyunchi-imagebuilder -RunOutputName runout-template-name-u7gjqx
PS C:\> Get-AzImageBuilderRunOutput -InputObject $result

Name                        Type
----                        ----
runout-template-name-u7gjqx Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="b8a39-116">此命令在範本下取得執行結果。</span><span class="sxs-lookup"><span data-stu-id="b8a39-116">This command gets a run result under a template.</span></span>

## <span data-ttu-id="b8a39-117">參數</span><span class="sxs-lookup"><span data-stu-id="b8a39-117">PARAMETERS</span></span>

### <span data-ttu-id="b8a39-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8a39-118">-DefaultProfile</span></span>
<span data-ttu-id="b8a39-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b8a39-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8a39-120">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="b8a39-120">-ImageTemplateName</span></span>
<span data-ttu-id="b8a39-121">圖像範本的名稱</span><span class="sxs-lookup"><span data-stu-id="b8a39-121">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8a39-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8a39-122">-InputObject</span></span>
<span data-ttu-id="b8a39-123">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b8a39-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8a39-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8a39-124">-ResourceGroupName</span></span>
<span data-ttu-id="b8a39-125">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b8a39-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8a39-126">-RunOutputName</span><span class="sxs-lookup"><span data-stu-id="b8a39-126">-RunOutputName</span></span>
<span data-ttu-id="b8a39-127">執行輸出的名稱</span><span class="sxs-lookup"><span data-stu-id="b8a39-127">The name of the run output</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8a39-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b8a39-128">-SubscriptionId</span></span>
<span data-ttu-id="b8a39-129">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="b8a39-129">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b8a39-130">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="b8a39-130">The subscription Id forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8a39-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8a39-131">CommonParameters</span></span>
<span data-ttu-id="b8a39-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b8a39-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8a39-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b8a39-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8a39-134">輸入</span><span class="sxs-lookup"><span data-stu-id="b8a39-134">INPUTS</span></span>

### <span data-ttu-id="b8a39-135">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.models.IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="b8a39-135">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="b8a39-136">輸出</span><span class="sxs-lookup"><span data-stu-id="b8a39-136">OUTPUTS</span></span>

### <span data-ttu-id="b8a39-137">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IRunOutput</span><span class="sxs-lookup"><span data-stu-id="b8a39-137">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IRunOutput</span></span>

## <span data-ttu-id="b8a39-138">筆記</span><span class="sxs-lookup"><span data-stu-id="b8a39-138">NOTES</span></span>

<span data-ttu-id="b8a39-139">別名</span><span class="sxs-lookup"><span data-stu-id="b8a39-139">ALIASES</span></span>

<span data-ttu-id="b8a39-140">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="b8a39-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b8a39-141">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b8a39-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b8a39-142">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="b8a39-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b8a39-143">INPUTOBJECT： <IImageBuilderIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="b8a39-143">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b8a39-144">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="b8a39-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b8a39-145">`[ImageTemplateName <String>]`：圖像範本的名稱</span><span class="sxs-lookup"><span data-stu-id="b8a39-145">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="b8a39-146">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b8a39-146">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="b8a39-147">`[RunOutputName <String>]`：執行輸出的名稱</span><span class="sxs-lookup"><span data-stu-id="b8a39-147">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="b8a39-148">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="b8a39-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b8a39-149">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="b8a39-149">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="b8a39-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="b8a39-150">RELATED LINKS</span></span>

