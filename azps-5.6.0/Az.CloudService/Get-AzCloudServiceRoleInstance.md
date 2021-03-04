---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/get-azcloudserviceroleinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstance.md
ms.openlocfilehash: 516bc63d7866ffd8a3c16fd224a49697c0cc972f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914905"
---
# <span data-ttu-id="f2791-101">Get-AzCloudServiceRoleInstance</span><span class="sxs-lookup"><span data-stu-id="f2791-101">Get-AzCloudServiceRoleInstance</span></span>

## <span data-ttu-id="f2791-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f2791-102">SYNOPSIS</span></span>
<span data-ttu-id="f2791-103">從雲端服務獲得角色實例。</span><span class="sxs-lookup"><span data-stu-id="f2791-103">Gets a role instance from a cloud service.</span></span>

## <span data-ttu-id="f2791-104">語法</span><span class="sxs-lookup"><span data-stu-id="f2791-104">SYNTAX</span></span>

### <span data-ttu-id="f2791-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="f2791-105">List (Default)</span></span>
```
Get-AzCloudServiceRoleInstance -CloudServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-Expand <InstanceViewTypes>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f2791-106">獲取</span><span class="sxs-lookup"><span data-stu-id="f2791-106">Get</span></span>
```
Get-AzCloudServiceRoleInstance -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String[]>] [-Expand <InstanceViewTypes>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f2791-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f2791-107">GetViaIdentity</span></span>
```
Get-AzCloudServiceRoleInstance -InputObject <ICloudServiceIdentity> [-Expand <InstanceViewTypes>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f2791-108">描述</span><span class="sxs-lookup"><span data-stu-id="f2791-108">DESCRIPTION</span></span>
<span data-ttu-id="f2791-109">從雲端服務獲得角色實例。</span><span class="sxs-lookup"><span data-stu-id="f2791-109">Gets a role instance from a cloud service.</span></span>

## <span data-ttu-id="f2791-110">例子</span><span class="sxs-lookup"><span data-stu-id="f2791-110">EXAMPLES</span></span>

### <span data-ttu-id="f2791-111">範例 1：取得所有角色實例</span><span class="sxs-lookup"><span data-stu-id="f2791-111">Example 1: Get all role instances</span></span>
```powershell
PS C:\> Get-AzCloudServiceRoleInstance -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"

Name                    Location    SkuName        SkuTier
----                    --------    -------        -------
ContosoFrontEnd_IN_0    eastus2euap Standard_D1_v2 Standard
ContosoFrontEnd_IN_1    eastus2euap Standard_D1_v2 Standard
ContosoBackEnd_IN_1     eastus2euap Standard_D1_v2 Standard
ContosoBackEnd_IN_1     eastus2euap Standard_D1_v2 Standard

```

<span data-ttu-id="f2791-112">此命令會獲得名為 ContosoCS 的雲端服務所有角色實例的屬性，這些角色實例屬於名為 ContosOrg 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="f2791-112">This command gets the properties of all role instances of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="f2791-113">範例 2：取得單一角色實例的屬性</span><span class="sxs-lookup"><span data-stu-id="f2791-113">Example 2: Get properties for single role instance</span></span>
```powershell
PS C:\> Get-AzCloudServiceRoleInstance -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"

Name                    Location    SkuName        SkuTier
----                    --------    -------        -------
ContosoFrontEnd_IN_0    eastus2euap Standard_D1_v2 Standard

```

<span data-ttu-id="f2791-114">此命令會獲得名稱為 contosoCS 之ContosoFrontEnd_IN_0名為 ContosOrg 之雲端服務之角色實例的屬性。</span><span class="sxs-lookup"><span data-stu-id="f2791-114">This command gets the properties of the role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="f2791-115">參數</span><span class="sxs-lookup"><span data-stu-id="f2791-115">PARAMETERS</span></span>

### <span data-ttu-id="f2791-116">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="f2791-116">-CloudServiceName</span></span>
<span data-ttu-id="f2791-117">.</span><span class="sxs-lookup"><span data-stu-id="f2791-117">.</span></span>

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

### <span data-ttu-id="f2791-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2791-118">-DefaultProfile</span></span>
<span data-ttu-id="f2791-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f2791-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2791-120">-展開</span><span class="sxs-lookup"><span data-stu-id="f2791-120">-Expand</span></span>
<span data-ttu-id="f2791-121">要適用于運算的展開運算式。</span><span class="sxs-lookup"><span data-stu-id="f2791-121">The expand expression to apply to the operation.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Support.InstanceViewTypes
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2791-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2791-122">-InputObject</span></span>
<span data-ttu-id="f2791-123">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="f2791-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2791-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2791-124">-ResourceGroupName</span></span>
<span data-ttu-id="f2791-125">.</span><span class="sxs-lookup"><span data-stu-id="f2791-125">.</span></span>

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

### <span data-ttu-id="f2791-126">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="f2791-126">-RoleInstanceName</span></span>
<span data-ttu-id="f2791-127">角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="f2791-127">Name of the role instance.</span></span>

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

### <span data-ttu-id="f2791-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f2791-128">-SubscriptionId</span></span>
<span data-ttu-id="f2791-129">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="f2791-129">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f2791-130">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="f2791-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f2791-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2791-131">CommonParameters</span></span>
<span data-ttu-id="f2791-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f2791-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2791-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2791-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2791-134">輸入</span><span class="sxs-lookup"><span data-stu-id="f2791-134">INPUTS</span></span>

### <span data-ttu-id="f2791-135">Microsoft.Azure.PowerShell.Cmdlets.CloudService.models.iCloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="f2791-135">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="f2791-136">輸出</span><span class="sxs-lookup"><span data-stu-id="f2791-136">OUTPUTS</span></span>

### <span data-ttu-id="f2791-137">Microsoft.Azure.PowerShell.Cmdlets.CloudService.models.Api20201001Preview.IRoleInstance</span><span class="sxs-lookup"><span data-stu-id="f2791-137">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.IRoleInstance</span></span>

## <span data-ttu-id="f2791-138">筆記</span><span class="sxs-lookup"><span data-stu-id="f2791-138">NOTES</span></span>

<span data-ttu-id="f2791-139">別名</span><span class="sxs-lookup"><span data-stu-id="f2791-139">ALIASES</span></span>

<span data-ttu-id="f2791-140">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="f2791-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f2791-141">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="f2791-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f2791-142">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="f2791-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f2791-143">INPUTOBJECT： <ICloudServiceIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="f2791-143">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f2791-144">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="f2791-144">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="f2791-145">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="f2791-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f2791-146">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="f2791-146">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="f2791-147">`[RoleInstanceName <String>]`：角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="f2791-147">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="f2791-148">`[RoleName <String>]`：角色名稱。</span><span class="sxs-lookup"><span data-stu-id="f2791-148">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="f2791-149">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="f2791-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f2791-150">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="f2791-150">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="f2791-151">`[UpdateDomain <Int32?>]`：指定可識別更新網域的整數值。</span><span class="sxs-lookup"><span data-stu-id="f2791-151">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="f2791-152">更新網域會以零型索引識別：第一個更新網域的識別碼為 0，第二個更新網域的識別碼為 1，以此類比。</span><span class="sxs-lookup"><span data-stu-id="f2791-152">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="f2791-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="f2791-153">RELATED LINKS</span></span>

