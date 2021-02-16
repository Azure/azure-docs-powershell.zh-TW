---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/remove-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Remove-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Remove-AzCloudService.md
ms.openlocfilehash: 07d7747a16af8d61b8ddbf05030445e599bb7e33
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100139366"
---
# <span data-ttu-id="8171d-101">Remove-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="8171d-101">Remove-AzCloudService</span></span>

## <span data-ttu-id="8171d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8171d-102">SYNOPSIS</span></span>
<span data-ttu-id="8171d-103">刪除雲端服務。</span><span class="sxs-lookup"><span data-stu-id="8171d-103">Deletes a cloud service.</span></span>

## <span data-ttu-id="8171d-104">句法</span><span class="sxs-lookup"><span data-stu-id="8171d-104">SYNTAX</span></span>

### <span data-ttu-id="8171d-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="8171d-105">Delete (Default)</span></span>
```
Remove-AzCloudService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8171d-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8171d-106">DeleteViaIdentity</span></span>
```
Remove-AzCloudService -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8171d-107">說明</span><span class="sxs-lookup"><span data-stu-id="8171d-107">DESCRIPTION</span></span>
<span data-ttu-id="8171d-108">刪除雲端服務。</span><span class="sxs-lookup"><span data-stu-id="8171d-108">Deletes a cloud service.</span></span>

## <span data-ttu-id="8171d-109">示例</span><span class="sxs-lookup"><span data-stu-id="8171d-109">EXAMPLES</span></span>

### <span data-ttu-id="8171d-110">範例1：移除雲端服務</span><span class="sxs-lookup"><span data-stu-id="8171d-110">Example 1: Remove a cloud service</span></span>
```powershell
PS C:\> Remove-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
```

<span data-ttu-id="8171d-111">這個命令會從屬於名為 ContosOrg 的資源群組中，移除名為 ContosoCS 的雲端服務。</span><span class="sxs-lookup"><span data-stu-id="8171d-111">This command removes the cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="8171d-112">參數</span><span class="sxs-lookup"><span data-stu-id="8171d-112">PARAMETERS</span></span>

### <span data-ttu-id="8171d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8171d-113">-AsJob</span></span>
<span data-ttu-id="8171d-114">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="8171d-114">Run the command as a job</span></span>

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

### <span data-ttu-id="8171d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8171d-115">-DefaultProfile</span></span>
<span data-ttu-id="8171d-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8171d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8171d-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8171d-117">-InputObject</span></span>
<span data-ttu-id="8171d-118">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="8171d-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8171d-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="8171d-119">-Name</span></span>
<span data-ttu-id="8171d-120">雲端服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="8171d-120">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8171d-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8171d-121">-NoWait</span></span>
<span data-ttu-id="8171d-122">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="8171d-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8171d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8171d-123">-PassThru</span></span>
<span data-ttu-id="8171d-124">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="8171d-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8171d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8171d-125">-ResourceGroupName</span></span>
<span data-ttu-id="8171d-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8171d-126">Name of the resource group.</span></span>

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

### <span data-ttu-id="8171d-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8171d-127">-SubscriptionId</span></span>
<span data-ttu-id="8171d-128">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="8171d-128">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8171d-129">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="8171d-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8171d-130">-確認</span><span class="sxs-lookup"><span data-stu-id="8171d-130">-Confirm</span></span>
<span data-ttu-id="8171d-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8171d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8171d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8171d-132">-WhatIf</span></span>
<span data-ttu-id="8171d-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8171d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8171d-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8171d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8171d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8171d-135">CommonParameters</span></span>
<span data-ttu-id="8171d-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8171d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8171d-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8171d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8171d-138">輸入</span><span class="sxs-lookup"><span data-stu-id="8171d-138">INPUTS</span></span>

### <span data-ttu-id="8171d-139">ICloudServiceIdentity （CloudService）的</span><span class="sxs-lookup"><span data-stu-id="8171d-139">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="8171d-140">輸出</span><span class="sxs-lookup"><span data-stu-id="8171d-140">OUTPUTS</span></span>

### <span data-ttu-id="8171d-141">System.object</span><span class="sxs-lookup"><span data-stu-id="8171d-141">System.Boolean</span></span>

## <span data-ttu-id="8171d-142">筆記</span><span class="sxs-lookup"><span data-stu-id="8171d-142">NOTES</span></span>

<span data-ttu-id="8171d-143">別名</span><span class="sxs-lookup"><span data-stu-id="8171d-143">ALIASES</span></span>

<span data-ttu-id="8171d-144">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="8171d-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8171d-145">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="8171d-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8171d-146">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="8171d-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8171d-147">INPUTOBJECT <ICloudServiceIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="8171d-147">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8171d-148">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="8171d-148">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="8171d-149">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="8171d-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8171d-150">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="8171d-150">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="8171d-151">`[RoleInstanceName <String>]`：角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="8171d-151">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="8171d-152">`[RoleName <String>]`：角色的名稱。</span><span class="sxs-lookup"><span data-stu-id="8171d-152">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="8171d-153">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="8171d-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8171d-154">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="8171d-154">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="8171d-155">`[UpdateDomain <Int32?>]`：指定識別更新網域的整數值。</span><span class="sxs-lookup"><span data-stu-id="8171d-155">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="8171d-156">更新網域是以零為基礎的索引來標識：第一個更新網域的識別碼為0，第二個是 ID 為1，依此類推。</span><span class="sxs-lookup"><span data-stu-id="8171d-156">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="8171d-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="8171d-157">RELATED LINKS</span></span>

