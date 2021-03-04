---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/powershell/module/az.addomainservices/remove-azaddomainservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Remove-AzADDomainService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Remove-AzADDomainService.md
ms.openlocfilehash: 68631f106b795f42fa8ead1a6379ff9dbaa0f4ee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909866"
---
# <span data-ttu-id="6ac50-101">Remove-AzADDomainService</span><span class="sxs-lookup"><span data-stu-id="6ac50-101">Remove-AzADDomainService</span></span>

## <span data-ttu-id="6ac50-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6ac50-102">SYNOPSIS</span></span>
<span data-ttu-id="6ac50-103">刪除網域服務作業會刪除現有的網域服務。</span><span class="sxs-lookup"><span data-stu-id="6ac50-103">The Delete Domain Service operation deletes an existing Domain Service.</span></span>

## <span data-ttu-id="6ac50-104">語法</span><span class="sxs-lookup"><span data-stu-id="6ac50-104">SYNTAX</span></span>

### <span data-ttu-id="6ac50-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="6ac50-105">Delete (Default)</span></span>
```
Remove-AzADDomainService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6ac50-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6ac50-106">DeleteViaIdentity</span></span>
```
Remove-AzADDomainService -InputObject <IAdDomainServicesIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6ac50-107">描述</span><span class="sxs-lookup"><span data-stu-id="6ac50-107">DESCRIPTION</span></span>
<span data-ttu-id="6ac50-108">刪除網域服務作業會刪除現有的網域服務。</span><span class="sxs-lookup"><span data-stu-id="6ac50-108">The Delete Domain Service operation deletes an existing Domain Service.</span></span>

## <span data-ttu-id="6ac50-109">例子</span><span class="sxs-lookup"><span data-stu-id="6ac50-109">EXAMPLES</span></span>

### <span data-ttu-id="6ac50-110">範例 1：刪除 ResourceGroupName 和 Name 的 AzADDomain</span><span class="sxs-lookup"><span data-stu-id="6ac50-110">Example 1: Delete the AzADDomain by ResourceGroupName and Name</span></span>
```powershell
PS C:\> Remove-AzADDomainService -ResourceGroupName $env.ResourceGroupName -Name $env.ADdomainName

```

<span data-ttu-id="6ac50-111">刪除 ResourceGroupName 和 Name 的 AzADDomain</span><span class="sxs-lookup"><span data-stu-id="6ac50-111">Delete the AzADDomain by ResourceGroupName and Name</span></span>

### <span data-ttu-id="6ac50-112">範例 2：刪除 InputObject 的 AzADDomain</span><span class="sxs-lookup"><span data-stu-id="6ac50-112">Example 2: Delete the AzADDomain by InputObject</span></span>
```powershell
PS C:\> $GetADDomainExample = Get-AzADDomainService -ResourceGroupName $env.ResourceGroupName -Name $env.ADdomainName
Remove-AzADDomainService -InputObject $GetADDomainExample

```

<span data-ttu-id="6ac50-113">刪除 InputObject 的 AzADDomain</span><span class="sxs-lookup"><span data-stu-id="6ac50-113">Delete the AzADDomain by InputObject</span></span>

## <span data-ttu-id="6ac50-114">參數</span><span class="sxs-lookup"><span data-stu-id="6ac50-114">PARAMETERS</span></span>

### <span data-ttu-id="6ac50-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6ac50-115">-AsJob</span></span>
<span data-ttu-id="6ac50-116">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="6ac50-116">Run the command as a job</span></span>

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

### <span data-ttu-id="6ac50-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ac50-117">-DefaultProfile</span></span>
<span data-ttu-id="6ac50-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6ac50-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ac50-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ac50-119">-InputObject</span></span>
<span data-ttu-id="6ac50-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="6ac50-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ac50-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="6ac50-121">-Name</span></span>
<span data-ttu-id="6ac50-122">網域服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="6ac50-122">The name of the domain service.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DomainServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ac50-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6ac50-123">-NoWait</span></span>
<span data-ttu-id="6ac50-124">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="6ac50-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6ac50-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6ac50-125">-PassThru</span></span>
<span data-ttu-id="6ac50-126">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="6ac50-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6ac50-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ac50-127">-ResourceGroupName</span></span>
<span data-ttu-id="6ac50-128">使用者訂閱中資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6ac50-128">The name of the resource group within the user's subscription.</span></span>
<span data-ttu-id="6ac50-129">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="6ac50-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="6ac50-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6ac50-130">-SubscriptionId</span></span>
<span data-ttu-id="6ac50-131">獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="6ac50-131">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="6ac50-132">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="6ac50-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6ac50-133">-確認</span><span class="sxs-lookup"><span data-stu-id="6ac50-133">-Confirm</span></span>
<span data-ttu-id="6ac50-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6ac50-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ac50-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ac50-135">-WhatIf</span></span>
<span data-ttu-id="6ac50-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6ac50-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ac50-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6ac50-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ac50-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ac50-138">CommonParameters</span></span>
<span data-ttu-id="6ac50-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6ac50-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ac50-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6ac50-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ac50-141">輸入</span><span class="sxs-lookup"><span data-stu-id="6ac50-141">INPUTS</span></span>

### <span data-ttu-id="6ac50-142">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.models.IAdDomainServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="6ac50-142">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span></span>

## <span data-ttu-id="6ac50-143">輸出</span><span class="sxs-lookup"><span data-stu-id="6ac50-143">OUTPUTS</span></span>

### <span data-ttu-id="6ac50-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6ac50-144">System.Boolean</span></span>

## <span data-ttu-id="6ac50-145">筆記</span><span class="sxs-lookup"><span data-stu-id="6ac50-145">NOTES</span></span>

<span data-ttu-id="6ac50-146">別名</span><span class="sxs-lookup"><span data-stu-id="6ac50-146">ALIASES</span></span>

<span data-ttu-id="6ac50-147">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="6ac50-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6ac50-148">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="6ac50-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6ac50-149">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="6ac50-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6ac50-150">INPUTOBJECT： <IAdDomainServicesIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="6ac50-150">INPUTOBJECT <IAdDomainServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6ac50-151">`[DomainServiceName <String>]`：網域服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="6ac50-151">`[DomainServiceName <String>]`: The name of the domain service.</span></span>
  - <span data-ttu-id="6ac50-152">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="6ac50-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6ac50-153">`[ResourceGroupName <String>]`：使用者訂閱中的資源組名。</span><span class="sxs-lookup"><span data-stu-id="6ac50-153">`[ResourceGroupName <String>]`: The name of the resource group within the user's subscription.</span></span> <span data-ttu-id="6ac50-154">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="6ac50-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="6ac50-155">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="6ac50-155">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="6ac50-156">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="6ac50-156">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="6ac50-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="6ac50-157">RELATED LINKS</span></span>

