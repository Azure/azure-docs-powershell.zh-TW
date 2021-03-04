---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/start-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Start-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Start-AzCloudService.md
ms.openlocfilehash: 7bbd639c670112a227e90ee1f9a4b07171673fbd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910529"
---
# <span data-ttu-id="2b067-101">Start-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="2b067-101">Start-AzCloudService</span></span>

## <span data-ttu-id="2b067-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2b067-102">SYNOPSIS</span></span>
<span data-ttu-id="2b067-103">啟動雲端服務。</span><span class="sxs-lookup"><span data-stu-id="2b067-103">Starts the cloud service.</span></span>

## <span data-ttu-id="2b067-104">語法</span><span class="sxs-lookup"><span data-stu-id="2b067-104">SYNTAX</span></span>

### <span data-ttu-id="2b067-105">啟動 (預設) </span><span class="sxs-lookup"><span data-stu-id="2b067-105">Start (Default)</span></span>
```
Start-AzCloudService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2b067-106">StartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2b067-106">StartViaIdentity</span></span>
```
Start-AzCloudService -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2b067-107">描述</span><span class="sxs-lookup"><span data-stu-id="2b067-107">DESCRIPTION</span></span>
<span data-ttu-id="2b067-108">啟動雲端服務。</span><span class="sxs-lookup"><span data-stu-id="2b067-108">Starts the cloud service.</span></span>

## <span data-ttu-id="2b067-109">例子</span><span class="sxs-lookup"><span data-stu-id="2b067-109">EXAMPLES</span></span>

### <span data-ttu-id="2b067-110">範例 1：啟動雲端服務</span><span class="sxs-lookup"><span data-stu-id="2b067-110">Example 1: Start cloud service</span></span>
```powershell
PS C:\> Start-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"
```

<span data-ttu-id="2b067-111">此命令會啟動所有屬於名為 ContosoCS 之雲端服務的角色實例。</span><span class="sxs-lookup"><span data-stu-id="2b067-111">This command starts all the role instances that belong to the the cloud service named ContosoCS.</span></span>

## <span data-ttu-id="2b067-112">參數</span><span class="sxs-lookup"><span data-stu-id="2b067-112">PARAMETERS</span></span>

### <span data-ttu-id="2b067-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2b067-113">-AsJob</span></span>
<span data-ttu-id="2b067-114">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="2b067-114">Run the command as a job</span></span>

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

### <span data-ttu-id="2b067-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b067-115">-DefaultProfile</span></span>
<span data-ttu-id="2b067-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2b067-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b067-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b067-117">-InputObject</span></span>
<span data-ttu-id="2b067-118">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="2b067-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: StartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b067-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="2b067-119">-Name</span></span>
<span data-ttu-id="2b067-120">雲端服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b067-120">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b067-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2b067-121">-NoWait</span></span>
<span data-ttu-id="2b067-122">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="2b067-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2b067-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2b067-123">-PassThru</span></span>
<span data-ttu-id="2b067-124">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="2b067-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2b067-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b067-125">-ResourceGroupName</span></span>
<span data-ttu-id="2b067-126">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b067-126">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b067-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2b067-127">-SubscriptionId</span></span>
<span data-ttu-id="2b067-128">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="2b067-128">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2b067-129">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="2b067-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b067-130">-確認</span><span class="sxs-lookup"><span data-stu-id="2b067-130">-Confirm</span></span>
<span data-ttu-id="2b067-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2b067-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b067-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b067-132">-WhatIf</span></span>
<span data-ttu-id="2b067-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2b067-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b067-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2b067-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b067-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b067-135">CommonParameters</span></span>
<span data-ttu-id="2b067-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2b067-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b067-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2b067-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b067-138">輸入</span><span class="sxs-lookup"><span data-stu-id="2b067-138">INPUTS</span></span>

### <span data-ttu-id="2b067-139">Microsoft.Azure.PowerShell.Cmdlets.CloudService.models.iCloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="2b067-139">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="2b067-140">輸出</span><span class="sxs-lookup"><span data-stu-id="2b067-140">OUTPUTS</span></span>

### <span data-ttu-id="2b067-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2b067-141">System.Boolean</span></span>

## <span data-ttu-id="2b067-142">筆記</span><span class="sxs-lookup"><span data-stu-id="2b067-142">NOTES</span></span>

<span data-ttu-id="2b067-143">別名</span><span class="sxs-lookup"><span data-stu-id="2b067-143">ALIASES</span></span>

<span data-ttu-id="2b067-144">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="2b067-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2b067-145">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="2b067-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2b067-146">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="2b067-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2b067-147">INPUTOBJECT： <ICloudServiceIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="2b067-147">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2b067-148">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="2b067-148">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="2b067-149">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="2b067-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2b067-150">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="2b067-150">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="2b067-151">`[RoleInstanceName <String>]`：角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b067-151">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="2b067-152">`[RoleName <String>]`：角色名稱。</span><span class="sxs-lookup"><span data-stu-id="2b067-152">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="2b067-153">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="2b067-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="2b067-154">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="2b067-154">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="2b067-155">`[UpdateDomain <Int32?>]`：指定可識別更新網域的整數值。</span><span class="sxs-lookup"><span data-stu-id="2b067-155">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="2b067-156">更新網域會以零型索引識別：第一個更新網域的識別碼為 0，第二個更新網域的識別碼為 1，以此類比。</span><span class="sxs-lookup"><span data-stu-id="2b067-156">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="2b067-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="2b067-157">RELATED LINKS</span></span>

