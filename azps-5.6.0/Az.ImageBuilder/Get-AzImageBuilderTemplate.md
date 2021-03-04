---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/powershell/module/az.imagebuilder/get-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderTemplate.md
ms.openlocfilehash: 82730525f6330336be72e922881d743345515926
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917189"
---
# <span data-ttu-id="f8763-101">Get-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="f8763-101">Get-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="f8763-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f8763-102">SYNOPSIS</span></span>
<span data-ttu-id="f8763-103">取得虛擬機器映射範本相關資訊</span><span class="sxs-lookup"><span data-stu-id="f8763-103">Get information about a virtual machine image template</span></span>

## <span data-ttu-id="f8763-104">語法</span><span class="sxs-lookup"><span data-stu-id="f8763-104">SYNTAX</span></span>

### <span data-ttu-id="f8763-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="f8763-105">List (Default)</span></span>
```
Get-AzImageBuilderTemplate [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f8763-106">獲取</span><span class="sxs-lookup"><span data-stu-id="f8763-106">Get</span></span>
```
Get-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f8763-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f8763-107">GetViaIdentity</span></span>
```
Get-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="f8763-108">清單1</span><span class="sxs-lookup"><span data-stu-id="f8763-108">List1</span></span>
```
Get-AzImageBuilderTemplate -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f8763-109">描述</span><span class="sxs-lookup"><span data-stu-id="f8763-109">DESCRIPTION</span></span>
<span data-ttu-id="f8763-110">取得虛擬機器映射範本相關資訊</span><span class="sxs-lookup"><span data-stu-id="f8763-110">Get information about a virtual machine image template</span></span>

## <span data-ttu-id="f8763-111">例子</span><span class="sxs-lookup"><span data-stu-id="f8763-111">EXAMPLES</span></span>

### <span data-ttu-id="f8763-112">範例 1：列出訂閱下的所有範本</span><span class="sxs-lookup"><span data-stu-id="f8763-112">Example 1: List all template under a subscription</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate

Location Name                      Type
-------- ----                      ----
eastus   HelloImageTemplateLinux01 Microsoft.VirtualMachineImages/imageTemplates
eastus   lucas-imagetemplate       Microsoft.VirtualMachineImages/imageTemplates
eastus   test-imagebuilder         Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="f8763-113">此命令會列出訂閱下的所有範本。</span><span class="sxs-lookup"><span data-stu-id="f8763-113">This command lists all template under a subscription.</span></span>

### <span data-ttu-id="f8763-114">範例 2：在資源群組下列出所有範本</span><span class="sxs-lookup"><span data-stu-id="f8763-114">Example 2: List all template under a resource group</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder

Location Name                       Type
-------- ----                       ----
eastus   HelloImageTemplateLinux01  Microsoft.VirtualMachineImages/imageTemplates
eastus   template-name-ax01b7       Microsoft.VirtualMachineImages/imageTemplates
eastus   template-name-ep5z7v       Microsoft.VirtualMachineImages/imageTemplates
eastus   template-name-klcuav       Microsoft.VirtualMachineImages/imageTemplates
eastus   template-name-u7gjqx       Microsoft.VirtualMachineImages/imageTemplates
eastus   test-imagebuilder          Microsoft.VirtualMachineImages/imageTemplates
eastus   tmpl-managedimg-managedimg Microsoft.VirtualMachineImages/imageTemplates
eastus   tmpl-platform-managed      Microsoft.VirtualMachineImages/imageTemplates
eastus   tmpl-shareimg-managedimg   Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="f8763-115">此命令會列出資源群組下的所有範本。</span><span class="sxs-lookup"><span data-stu-id="f8763-115">This command lists all template under a resource group.</span></span>

### <span data-ttu-id="f8763-116">範例 3：在資源群組下取得範本</span><span class="sxs-lookup"><span data-stu-id="f8763-116">Example 3: Get a template under a resource group</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate -ImageTemplateName lucas-imagetemplate -ResourceGroupName wyunchi-imagebuilder

Location Name                Type
-------- ----                ----
eastus   lucas-imagetemplate Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="f8763-117">此命令會獲得資源群組下的範本。</span><span class="sxs-lookup"><span data-stu-id="f8763-117">This command gets a template under a resource group.</span></span>

### <span data-ttu-id="f8763-118">範例 4：在資源群組下取得範本</span><span class="sxs-lookup"><span data-stu-id="f8763-118">Example 4: Get a template under a resource group</span></span>
```powershell
PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -ImageTemplateName template-name-ep5z7v
PS C:\> Get-AzImageBuilderTemplate -InputObject $template

Location Name                 Type
-------- ----                 ----
eastus   template-name-ep5z7v Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="f8763-119">此命令會獲得資源群組下的範本。</span><span class="sxs-lookup"><span data-stu-id="f8763-119">This command gets a template under a resource group.</span></span>

## <span data-ttu-id="f8763-120">參數</span><span class="sxs-lookup"><span data-stu-id="f8763-120">PARAMETERS</span></span>

### <span data-ttu-id="f8763-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8763-121">-DefaultProfile</span></span>
<span data-ttu-id="f8763-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f8763-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8763-123">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="f8763-123">-ImageTemplateName</span></span>
<span data-ttu-id="f8763-124">圖像範本的名稱</span><span class="sxs-lookup"><span data-stu-id="f8763-124">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8763-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f8763-125">-InputObject</span></span>
<span data-ttu-id="f8763-126">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="f8763-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f8763-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8763-127">-ResourceGroupName</span></span>
<span data-ttu-id="f8763-128">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f8763-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8763-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f8763-129">-SubscriptionId</span></span>
<span data-ttu-id="f8763-130">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="f8763-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f8763-131">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="f8763-131">The subscription Id forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8763-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8763-132">CommonParameters</span></span>
<span data-ttu-id="f8763-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f8763-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8763-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f8763-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8763-135">輸入</span><span class="sxs-lookup"><span data-stu-id="f8763-135">INPUTS</span></span>

### <span data-ttu-id="f8763-136">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.models.IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="f8763-136">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="f8763-137">輸出</span><span class="sxs-lookup"><span data-stu-id="f8763-137">OUTPUTS</span></span>

### <span data-ttu-id="f8763-138">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplate</span><span class="sxs-lookup"><span data-stu-id="f8763-138">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplate</span></span>

## <span data-ttu-id="f8763-139">筆記</span><span class="sxs-lookup"><span data-stu-id="f8763-139">NOTES</span></span>

<span data-ttu-id="f8763-140">別名</span><span class="sxs-lookup"><span data-stu-id="f8763-140">ALIASES</span></span>

<span data-ttu-id="f8763-141">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="f8763-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f8763-142">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="f8763-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f8763-143">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="f8763-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f8763-144">INPUTOBJECT： <IImageBuilderIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="f8763-144">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f8763-145">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="f8763-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f8763-146">`[ImageTemplateName <String>]`：圖像範本的名稱</span><span class="sxs-lookup"><span data-stu-id="f8763-146">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="f8763-147">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f8763-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="f8763-148">`[RunOutputName <String>]`：執行輸出的名稱</span><span class="sxs-lookup"><span data-stu-id="f8763-148">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="f8763-149">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="f8763-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f8763-150">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="f8763-150">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f8763-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="f8763-151">RELATED LINKS</span></span>

