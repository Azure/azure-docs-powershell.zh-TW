---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/get-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderTemplate.md
ms.openlocfilehash: d159a59f6fb94523868b4aa6109553900f1b289d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98438220"
---
# <span data-ttu-id="5a632-101">Get-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="5a632-101">Get-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="5a632-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5a632-102">SYNOPSIS</span></span>
<span data-ttu-id="5a632-103">取得虛擬機器影像範本的相關資訊</span><span class="sxs-lookup"><span data-stu-id="5a632-103">Get information about a virtual machine image template</span></span>

## <span data-ttu-id="5a632-104">句法</span><span class="sxs-lookup"><span data-stu-id="5a632-104">SYNTAX</span></span>

### <span data-ttu-id="5a632-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="5a632-105">List (Default)</span></span>
```
Get-AzImageBuilderTemplate [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5a632-106">獲取</span><span class="sxs-lookup"><span data-stu-id="5a632-106">Get</span></span>
```
Get-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5a632-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5a632-107">GetViaIdentity</span></span>
```
Get-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="5a632-108">List1</span><span class="sxs-lookup"><span data-stu-id="5a632-108">List1</span></span>
```
Get-AzImageBuilderTemplate -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5a632-109">說明</span><span class="sxs-lookup"><span data-stu-id="5a632-109">DESCRIPTION</span></span>
<span data-ttu-id="5a632-110">取得虛擬機器影像範本的相關資訊</span><span class="sxs-lookup"><span data-stu-id="5a632-110">Get information about a virtual machine image template</span></span>

## <span data-ttu-id="5a632-111">示例</span><span class="sxs-lookup"><span data-stu-id="5a632-111">EXAMPLES</span></span>

### <span data-ttu-id="5a632-112">範例1：列出訂閱下的所有範本</span><span class="sxs-lookup"><span data-stu-id="5a632-112">Example 1: List all template under a subscription</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate

Location Name                      Type
-------- ----                      ----
eastus   HelloImageTemplateLinux01 Microsoft.VirtualMachineImages/imageTemplates
eastus   lucas-imagetemplate       Microsoft.VirtualMachineImages/imageTemplates
eastus   test-imagebuilder         Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="5a632-113">這個命令會列出訂閱下的所有範本。</span><span class="sxs-lookup"><span data-stu-id="5a632-113">This command lists all template under a subscription.</span></span>

### <span data-ttu-id="5a632-114">範例2：列出資源群組底下的所有範本</span><span class="sxs-lookup"><span data-stu-id="5a632-114">Example 2: List all template under a resource group</span></span>
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

<span data-ttu-id="5a632-115">這個命令會列出 [資源] 群組底下的所有範本。</span><span class="sxs-lookup"><span data-stu-id="5a632-115">This command lists all template under a resource group.</span></span>

### <span data-ttu-id="5a632-116">範例3：在資源群組下取得範本</span><span class="sxs-lookup"><span data-stu-id="5a632-116">Example 3: Get a template under a resource group</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate -ImageTemplateName lucas-imagetemplate -ResourceGroupName wyunchi-imagebuilder

Location Name                Type
-------- ----                ----
eastus   lucas-imagetemplate Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="5a632-117">這個命令會在資源群組下取得範本。</span><span class="sxs-lookup"><span data-stu-id="5a632-117">This command gets a template under a resource group.</span></span>

### <span data-ttu-id="5a632-118">範例4：在資源群組下取得範本</span><span class="sxs-lookup"><span data-stu-id="5a632-118">Example 4: Get a template under a resource group</span></span>
```powershell
PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -ImageTemplateName template-name-ep5z7v
PS C:\> Get-AzImageBuilderTemplate -InputObject $template

Location Name                 Type
-------- ----                 ----
eastus   template-name-ep5z7v Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="5a632-119">這個命令會在資源群組下取得範本。</span><span class="sxs-lookup"><span data-stu-id="5a632-119">This command gets a template under a resource group.</span></span>

## <span data-ttu-id="5a632-120">參數</span><span class="sxs-lookup"><span data-stu-id="5a632-120">PARAMETERS</span></span>

### <span data-ttu-id="5a632-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a632-121">-DefaultProfile</span></span>
<span data-ttu-id="5a632-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5a632-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a632-123">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="5a632-123">-ImageTemplateName</span></span>
<span data-ttu-id="5a632-124">影像範本的名稱</span><span class="sxs-lookup"><span data-stu-id="5a632-124">The name of the image Template</span></span>

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

### <span data-ttu-id="5a632-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a632-125">-InputObject</span></span>
<span data-ttu-id="5a632-126">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="5a632-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5a632-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a632-127">-ResourceGroupName</span></span>
<span data-ttu-id="5a632-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5a632-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="5a632-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5a632-129">-SubscriptionId</span></span>
<span data-ttu-id="5a632-130">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="5a632-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5a632-131">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="5a632-131">The subscription Id forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5a632-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a632-132">CommonParameters</span></span>
<span data-ttu-id="5a632-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5a632-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a632-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5a632-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a632-135">輸入</span><span class="sxs-lookup"><span data-stu-id="5a632-135">INPUTS</span></span>

### <span data-ttu-id="5a632-136">IImageBuilderIdentity （ImageBuilder）的</span><span class="sxs-lookup"><span data-stu-id="5a632-136">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="5a632-137">輸出</span><span class="sxs-lookup"><span data-stu-id="5a632-137">OUTPUTS</span></span>

### <span data-ttu-id="5a632-138">IImageTemplate （ImageBuilder）。 Api20200214。</span><span class="sxs-lookup"><span data-stu-id="5a632-138">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplate</span></span>

## <span data-ttu-id="5a632-139">筆記</span><span class="sxs-lookup"><span data-stu-id="5a632-139">NOTES</span></span>

<span data-ttu-id="5a632-140">別名</span><span class="sxs-lookup"><span data-stu-id="5a632-140">ALIASES</span></span>

<span data-ttu-id="5a632-141">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="5a632-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5a632-142">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="5a632-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5a632-143">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="5a632-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5a632-144">INPUTOBJECT <IImageBuilderIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="5a632-144">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5a632-145">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="5a632-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5a632-146">`[ImageTemplateName <String>]`：影像範本的名稱</span><span class="sxs-lookup"><span data-stu-id="5a632-146">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="5a632-147">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5a632-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="5a632-148">`[RunOutputName <String>]`：執行輸出的名稱</span><span class="sxs-lookup"><span data-stu-id="5a632-148">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="5a632-149">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="5a632-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="5a632-150">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="5a632-150">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="5a632-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="5a632-151">RELATED LINKS</span></span>

