---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.addomainservices/remove-azaddomainservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Remove-AzADDomainService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Remove-AzADDomainService.md
ms.openlocfilehash: f29fbbdd805abb9891f707ed983bcf8aebefc46c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127310"
---
# <span data-ttu-id="c27eb-101">Remove-AzADDomainService</span><span class="sxs-lookup"><span data-stu-id="c27eb-101">Remove-AzADDomainService</span></span>

## <span data-ttu-id="c27eb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c27eb-102">SYNOPSIS</span></span>
<span data-ttu-id="c27eb-103">[刪除網域服務] 作業會刪除現有的網域服務。</span><span class="sxs-lookup"><span data-stu-id="c27eb-103">The Delete Domain Service operation deletes an existing Domain Service.</span></span>

## <span data-ttu-id="c27eb-104">句法</span><span class="sxs-lookup"><span data-stu-id="c27eb-104">SYNTAX</span></span>

### <span data-ttu-id="c27eb-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="c27eb-105">Delete (Default)</span></span>
```
Remove-AzADDomainService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c27eb-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c27eb-106">DeleteViaIdentity</span></span>
```
Remove-AzADDomainService -InputObject <IAdDomainServicesIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c27eb-107">說明</span><span class="sxs-lookup"><span data-stu-id="c27eb-107">DESCRIPTION</span></span>
<span data-ttu-id="c27eb-108">[刪除網域服務] 作業會刪除現有的網域服務。</span><span class="sxs-lookup"><span data-stu-id="c27eb-108">The Delete Domain Service operation deletes an existing Domain Service.</span></span>

## <span data-ttu-id="c27eb-109">示例</span><span class="sxs-lookup"><span data-stu-id="c27eb-109">EXAMPLES</span></span>

### <span data-ttu-id="c27eb-110">範例1：依 ResourceGroupName 和 Name 刪除 AzADDomain</span><span class="sxs-lookup"><span data-stu-id="c27eb-110">Example 1: Delete the AzADDomain by ResourceGroupName and Name</span></span>
```powershell
PS C:\> Remove-AzADDomainService -ResourceGroupName $env.ResourceGroupName -Name $env.ADdomainName

```

<span data-ttu-id="c27eb-111">依 ResourceGroupName 和 Name 刪除 AzADDomain</span><span class="sxs-lookup"><span data-stu-id="c27eb-111">Delete the AzADDomain by ResourceGroupName and Name</span></span>

### <span data-ttu-id="c27eb-112">範例2：刪除 AzADDomain by InputObject</span><span class="sxs-lookup"><span data-stu-id="c27eb-112">Example 2: Delete the AzADDomain by InputObject</span></span>
```powershell
PS C:\> $GetADDomainExample = Get-AzADDomainService -ResourceGroupName $env.ResourceGroupName -Name $env.ADdomainName
Remove-AzADDomainService -InputObject $GetADDomainExample

```

<span data-ttu-id="c27eb-113">刪除 AzADDomain by InputObject</span><span class="sxs-lookup"><span data-stu-id="c27eb-113">Delete the AzADDomain by InputObject</span></span>

## <span data-ttu-id="c27eb-114">參數</span><span class="sxs-lookup"><span data-stu-id="c27eb-114">PARAMETERS</span></span>

### <span data-ttu-id="c27eb-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c27eb-115">-AsJob</span></span>
<span data-ttu-id="c27eb-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="c27eb-116">Run the command as a job</span></span>

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

### <span data-ttu-id="c27eb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c27eb-117">-DefaultProfile</span></span>
<span data-ttu-id="c27eb-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c27eb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c27eb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c27eb-119">-InputObject</span></span>
<span data-ttu-id="c27eb-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="c27eb-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c27eb-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="c27eb-121">-Name</span></span>
<span data-ttu-id="c27eb-122">網域服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="c27eb-122">The name of the domain service.</span></span>

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

### <span data-ttu-id="c27eb-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c27eb-123">-NoWait</span></span>
<span data-ttu-id="c27eb-124">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="c27eb-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c27eb-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c27eb-125">-PassThru</span></span>
<span data-ttu-id="c27eb-126">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="c27eb-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c27eb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c27eb-127">-ResourceGroupName</span></span>
<span data-ttu-id="c27eb-128">使用者訂閱中資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c27eb-128">The name of the resource group within the user's subscription.</span></span>
<span data-ttu-id="c27eb-129">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="c27eb-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c27eb-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c27eb-130">-SubscriptionId</span></span>
<span data-ttu-id="c27eb-131">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="c27eb-131">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="c27eb-132">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="c27eb-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c27eb-133">-確認</span><span class="sxs-lookup"><span data-stu-id="c27eb-133">-Confirm</span></span>
<span data-ttu-id="c27eb-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c27eb-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c27eb-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c27eb-135">-WhatIf</span></span>
<span data-ttu-id="c27eb-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c27eb-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c27eb-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c27eb-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c27eb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c27eb-138">CommonParameters</span></span>
<span data-ttu-id="c27eb-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c27eb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c27eb-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c27eb-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c27eb-141">輸入</span><span class="sxs-lookup"><span data-stu-id="c27eb-141">INPUTS</span></span>

### <span data-ttu-id="c27eb-142">IAdDomainServicesIdentity （ADDomainServices）的</span><span class="sxs-lookup"><span data-stu-id="c27eb-142">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span></span>

## <span data-ttu-id="c27eb-143">輸出</span><span class="sxs-lookup"><span data-stu-id="c27eb-143">OUTPUTS</span></span>

### <span data-ttu-id="c27eb-144">System.object</span><span class="sxs-lookup"><span data-stu-id="c27eb-144">System.Boolean</span></span>

## <span data-ttu-id="c27eb-145">筆記</span><span class="sxs-lookup"><span data-stu-id="c27eb-145">NOTES</span></span>

<span data-ttu-id="c27eb-146">別名</span><span class="sxs-lookup"><span data-stu-id="c27eb-146">ALIASES</span></span>

<span data-ttu-id="c27eb-147">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="c27eb-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c27eb-148">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="c27eb-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c27eb-149">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="c27eb-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c27eb-150">INPUTOBJECT <IAdDomainServicesIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="c27eb-150">INPUTOBJECT <IAdDomainServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c27eb-151">`[DomainServiceName <String>]`：網域服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="c27eb-151">`[DomainServiceName <String>]`: The name of the domain service.</span></span>
  - <span data-ttu-id="c27eb-152">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="c27eb-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c27eb-153">`[ResourceGroupName <String>]`：使用者訂閱中資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c27eb-153">`[ResourceGroupName <String>]`: The name of the resource group within the user's subscription.</span></span> <span data-ttu-id="c27eb-154">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="c27eb-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="c27eb-155">`[SubscriptionId <String>]`：取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="c27eb-155">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="c27eb-156">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="c27eb-156">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="c27eb-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="c27eb-157">RELATED LINKS</span></span>

