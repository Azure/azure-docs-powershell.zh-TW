---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.springcloud/remove-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloud.md
ms.openlocfilehash: 3e2bf7dc031f257849036a3482361f1647379795
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916697"
---
# <span data-ttu-id="7f4d3-101">Remove-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="7f4d3-101">Remove-AzSpringCloud</span></span>

## <span data-ttu-id="7f4d3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7f4d3-102">SYNOPSIS</span></span>
<span data-ttu-id="7f4d3-103">刪除服務的作業。</span><span class="sxs-lookup"><span data-stu-id="7f4d3-103">Operation to delete a Service.</span></span>

## <span data-ttu-id="7f4d3-104">語法</span><span class="sxs-lookup"><span data-stu-id="7f4d3-104">SYNTAX</span></span>

### <span data-ttu-id="7f4d3-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="7f4d3-105">Delete (Default)</span></span>
```
Remove-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7f4d3-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7f4d3-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloud -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7f4d3-107">描述</span><span class="sxs-lookup"><span data-stu-id="7f4d3-107">DESCRIPTION</span></span>
<span data-ttu-id="7f4d3-108">刪除服務的作業。</span><span class="sxs-lookup"><span data-stu-id="7f4d3-108">Operation to delete a Service.</span></span>

## <span data-ttu-id="7f4d3-109">例子</span><span class="sxs-lookup"><span data-stu-id="7f4d3-109">EXAMPLES</span></span>

### <span data-ttu-id="7f4d3-110">範例 1：根據名稱移除 Spring Cloud Service。</span><span class="sxs-lookup"><span data-stu-id="7f4d3-110">Example 1: Remove Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
```

<span data-ttu-id="7f4d3-111">按名稱移除春雲服務。</span><span class="sxs-lookup"><span data-stu-id="7f4d3-111">Remove Spring Cloud Service by name.</span></span>

### <span data-ttu-id="7f4d3-112">範例 2：從管道移除 Spring Cloud Service。</span><span class="sxs-lookup"><span data-stu-id="7f4d3-112">Example 2: Remove Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service | Remove-AzSpringCloud
```

<span data-ttu-id="7f4d3-113">從管道移除 Spring Cloud Service。</span><span class="sxs-lookup"><span data-stu-id="7f4d3-113">Remove Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="7f4d3-114">參數</span><span class="sxs-lookup"><span data-stu-id="7f4d3-114">PARAMETERS</span></span>

### <span data-ttu-id="7f4d3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7f4d3-115">-AsJob</span></span>
<span data-ttu-id="7f4d3-116">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="7f4d3-116">Run the command as a job</span></span>

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

### <span data-ttu-id="7f4d3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f4d3-117">-DefaultProfile</span></span>
<span data-ttu-id="7f4d3-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7f4d3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f4d3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f4d3-119">-InputObject</span></span>
<span data-ttu-id="7f4d3-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="7f4d3-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f4d3-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="7f4d3-121">-Name</span></span>
<span data-ttu-id="7f4d3-122">服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="7f4d3-122">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f4d3-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7f4d3-123">-NoWait</span></span>
<span data-ttu-id="7f4d3-124">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="7f4d3-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7f4d3-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7f4d3-125">-PassThru</span></span>
<span data-ttu-id="7f4d3-126">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="7f4d3-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="7f4d3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f4d3-127">-ResourceGroupName</span></span>
<span data-ttu-id="7f4d3-128">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="7f4d3-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="7f4d3-129">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="7f4d3-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="7f4d3-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7f4d3-130">-SubscriptionId</span></span>
<span data-ttu-id="7f4d3-131">獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="7f4d3-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="7f4d3-132">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="7f4d3-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7f4d3-133">-確認</span><span class="sxs-lookup"><span data-stu-id="7f4d3-133">-Confirm</span></span>
<span data-ttu-id="7f4d3-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7f4d3-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f4d3-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f4d3-135">-WhatIf</span></span>
<span data-ttu-id="7f4d3-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7f4d3-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f4d3-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7f4d3-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f4d3-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f4d3-138">CommonParameters</span></span>
<span data-ttu-id="7f4d3-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7f4d3-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f4d3-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f4d3-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f4d3-141">輸入</span><span class="sxs-lookup"><span data-stu-id="7f4d3-141">INPUTS</span></span>

### <span data-ttu-id="7f4d3-142">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="7f4d3-142">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="7f4d3-143">輸出</span><span class="sxs-lookup"><span data-stu-id="7f4d3-143">OUTPUTS</span></span>

### <span data-ttu-id="7f4d3-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7f4d3-144">System.Boolean</span></span>

## <span data-ttu-id="7f4d3-145">筆記</span><span class="sxs-lookup"><span data-stu-id="7f4d3-145">NOTES</span></span>

<span data-ttu-id="7f4d3-146">別名</span><span class="sxs-lookup"><span data-stu-id="7f4d3-146">ALIASES</span></span>

<span data-ttu-id="7f4d3-147">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="7f4d3-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7f4d3-148">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="7f4d3-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7f4d3-149">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="7f4d3-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7f4d3-150">INPUTOBJECT： <ISpringCloudIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="7f4d3-150">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7f4d3-151">`[AppName <String>]`：應用程式資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="7f4d3-151">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="7f4d3-152">`[BindingName <String>]`：裝訂資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="7f4d3-152">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="7f4d3-153">`[CertificateName <String>]`：憑證資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="7f4d3-153">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="7f4d3-154">`[DeploymentName <String>]`：部署資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="7f4d3-154">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="7f4d3-155">`[DomainName <String>]`：自訂網域資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="7f4d3-155">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="7f4d3-156">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="7f4d3-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7f4d3-157">`[Location <String>]`：地區</span><span class="sxs-lookup"><span data-stu-id="7f4d3-157">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="7f4d3-158">`[ResourceGroupName <String>]`：包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="7f4d3-158">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="7f4d3-159">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="7f4d3-159">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="7f4d3-160">`[ServiceName <String>]`：服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="7f4d3-160">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="7f4d3-161">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="7f4d3-161">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="7f4d3-162">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="7f4d3-162">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="7f4d3-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="7f4d3-163">RELATED LINKS</span></span>

