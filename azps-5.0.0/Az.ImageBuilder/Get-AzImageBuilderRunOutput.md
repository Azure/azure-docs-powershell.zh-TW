---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/get-azimagebuilderrunoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderRunOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderRunOutput.md
ms.openlocfilehash: 4cc45f3b4cd21e41f1b2e410dd2b76b9571a4431
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284420"
---
# <span data-ttu-id="3bbf1-101">Get-AzImageBuilderRunOutput</span><span class="sxs-lookup"><span data-stu-id="3bbf1-101">Get-AzImageBuilderRunOutput</span></span>

## <span data-ttu-id="3bbf1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3bbf1-102">SYNOPSIS</span></span>
<span data-ttu-id="3bbf1-103">取得指定影像範本資源的指定執行輸出</span><span class="sxs-lookup"><span data-stu-id="3bbf1-103">Get the specified run output for the specified image template resource</span></span>

## <span data-ttu-id="3bbf1-104">句法</span><span class="sxs-lookup"><span data-stu-id="3bbf1-104">SYNTAX</span></span>

### <span data-ttu-id="3bbf1-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="3bbf1-105">List (Default)</span></span>
```
Get-AzImageBuilderRunOutput -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3bbf1-106">獲取</span><span class="sxs-lookup"><span data-stu-id="3bbf1-106">Get</span></span>
```
Get-AzImageBuilderRunOutput -ImageTemplateName <String> -ResourceGroupName <String> -RunOutputName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3bbf1-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3bbf1-107">GetViaIdentity</span></span>
```
Get-AzImageBuilderRunOutput -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="3bbf1-108">說明</span><span class="sxs-lookup"><span data-stu-id="3bbf1-108">DESCRIPTION</span></span>
<span data-ttu-id="3bbf1-109">取得指定影像範本資源的指定執行輸出</span><span class="sxs-lookup"><span data-stu-id="3bbf1-109">Get the specified run output for the specified image template resource</span></span>

## <span data-ttu-id="3bbf1-110">示例</span><span class="sxs-lookup"><span data-stu-id="3bbf1-110">EXAMPLES</span></span>

### <span data-ttu-id="3bbf1-111">範例1：列出範本下的所有執行結果</span><span class="sxs-lookup"><span data-stu-id="3bbf1-111">Example 1: List all run results under a template</span></span>
```powershell
PS C:\> Get-AzImageBuilderRunOutput -ImageTemplateName lucas-imagetemplate -ResourceGroupName wyunchi-imagebuilder

Name          Type
----          ----
image_lucas_1 Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="3bbf1-112">這個命令會列出範本下的所有執行結果。</span><span class="sxs-lookup"><span data-stu-id="3bbf1-112">This command lists all run results under a template.</span></span>

### <span data-ttu-id="3bbf1-113">範例2：在範本下取得執行結果</span><span class="sxs-lookup"><span data-stu-id="3bbf1-113">Example 2: Get a run result under a template</span></span>
```powershell
PS C:\> Get-AzImageBuilderRunOutput -ImageTemplateName template-name-u7gjqx -ResourceGroupName wyunchi-imagebuilder -RunOutputName runout-template-name-u7gjqx 

Name                        Type
----                        ----
runout-template-name-u7gjqx Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="3bbf1-114">這個命令會在範本中取得執行結果。</span><span class="sxs-lookup"><span data-stu-id="3bbf1-114">This command gets a run result under a template.</span></span>

### <span data-ttu-id="3bbf1-115">範例3：在範本下取得執行結果</span><span class="sxs-lookup"><span data-stu-id="3bbf1-115">Example 3: Get a run result under a template</span></span>
```powershell
PS C:\> $result = Get-AzImageBuilderRunOutput -ImageTemplateName template-name-u7gjqx -ResourceGroupName wyunchi-imagebuilder -RunOutputName runout-template-name-u7gjqx
PS C:\> Get-AzImageBuilderRunOutput -InputObject $result

Name                        Type
----                        ----
runout-template-name-u7gjqx Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="3bbf1-116">這個命令會在範本中取得執行結果。</span><span class="sxs-lookup"><span data-stu-id="3bbf1-116">This command gets a run result under a template.</span></span>

## <span data-ttu-id="3bbf1-117">參數</span><span class="sxs-lookup"><span data-stu-id="3bbf1-117">PARAMETERS</span></span>

### <span data-ttu-id="3bbf1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bbf1-118">-DefaultProfile</span></span>
<span data-ttu-id="3bbf1-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3bbf1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bbf1-120">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="3bbf1-120">-ImageTemplateName</span></span>
<span data-ttu-id="3bbf1-121">影像範本的名稱</span><span class="sxs-lookup"><span data-stu-id="3bbf1-121">The name of the image Template</span></span>

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

### <span data-ttu-id="3bbf1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3bbf1-122">-InputObject</span></span>
<span data-ttu-id="3bbf1-123">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="3bbf1-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3bbf1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bbf1-124">-ResourceGroupName</span></span>
<span data-ttu-id="3bbf1-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3bbf1-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="3bbf1-126">-RunOutputName</span><span class="sxs-lookup"><span data-stu-id="3bbf1-126">-RunOutputName</span></span>
<span data-ttu-id="3bbf1-127">執行輸出的名稱</span><span class="sxs-lookup"><span data-stu-id="3bbf1-127">The name of the run output</span></span>

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

### <span data-ttu-id="3bbf1-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3bbf1-128">-SubscriptionId</span></span>
<span data-ttu-id="3bbf1-129">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="3bbf1-129">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3bbf1-130">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="3bbf1-130">The subscription Id forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3bbf1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bbf1-131">CommonParameters</span></span>
<span data-ttu-id="3bbf1-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3bbf1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bbf1-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3bbf1-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bbf1-134">輸入</span><span class="sxs-lookup"><span data-stu-id="3bbf1-134">INPUTS</span></span>

### <span data-ttu-id="3bbf1-135">IImageBuilderIdentity （ImageBuilder）的</span><span class="sxs-lookup"><span data-stu-id="3bbf1-135">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="3bbf1-136">輸出</span><span class="sxs-lookup"><span data-stu-id="3bbf1-136">OUTPUTS</span></span>

### <span data-ttu-id="3bbf1-137">IRunOutput （ImageBuilder）。 Api20200214。</span><span class="sxs-lookup"><span data-stu-id="3bbf1-137">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IRunOutput</span></span>

## <span data-ttu-id="3bbf1-138">筆記</span><span class="sxs-lookup"><span data-stu-id="3bbf1-138">NOTES</span></span>

<span data-ttu-id="3bbf1-139">別名</span><span class="sxs-lookup"><span data-stu-id="3bbf1-139">ALIASES</span></span>

<span data-ttu-id="3bbf1-140">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="3bbf1-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3bbf1-141">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="3bbf1-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3bbf1-142">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="3bbf1-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3bbf1-143">INPUTOBJECT <IImageBuilderIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="3bbf1-143">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3bbf1-144">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="3bbf1-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3bbf1-145">`[ImageTemplateName <String>]`：影像範本的名稱</span><span class="sxs-lookup"><span data-stu-id="3bbf1-145">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="3bbf1-146">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3bbf1-146">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="3bbf1-147">`[RunOutputName <String>]`：執行輸出的名稱</span><span class="sxs-lookup"><span data-stu-id="3bbf1-147">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="3bbf1-148">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="3bbf1-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="3bbf1-149">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="3bbf1-149">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="3bbf1-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="3bbf1-150">RELATED LINKS</span></span>

