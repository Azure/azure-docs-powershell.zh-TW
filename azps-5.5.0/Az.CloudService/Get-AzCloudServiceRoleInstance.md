---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/get-azcloudserviceroleinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstance.md
ms.openlocfilehash: 55416adbd2ffbcb816e5652ad33e1777594fdcb6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100129915"
---
# <span data-ttu-id="07d5c-101">Get-AzCloudServiceRoleInstance</span><span class="sxs-lookup"><span data-stu-id="07d5c-101">Get-AzCloudServiceRoleInstance</span></span>

## <span data-ttu-id="07d5c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="07d5c-102">SYNOPSIS</span></span>
<span data-ttu-id="07d5c-103">從雲端服務取得角色實例。</span><span class="sxs-lookup"><span data-stu-id="07d5c-103">Gets a role instance from a cloud service.</span></span>

## <span data-ttu-id="07d5c-104">句法</span><span class="sxs-lookup"><span data-stu-id="07d5c-104">SYNTAX</span></span>

### <span data-ttu-id="07d5c-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="07d5c-105">List (Default)</span></span>
```
Get-AzCloudServiceRoleInstance -CloudServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-Expand <InstanceViewTypes>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="07d5c-106">獲取</span><span class="sxs-lookup"><span data-stu-id="07d5c-106">Get</span></span>
```
Get-AzCloudServiceRoleInstance -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String[]>] [-Expand <InstanceViewTypes>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="07d5c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="07d5c-107">GetViaIdentity</span></span>
```
Get-AzCloudServiceRoleInstance -InputObject <ICloudServiceIdentity> [-Expand <InstanceViewTypes>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="07d5c-108">說明</span><span class="sxs-lookup"><span data-stu-id="07d5c-108">DESCRIPTION</span></span>
<span data-ttu-id="07d5c-109">從雲端服務取得角色實例。</span><span class="sxs-lookup"><span data-stu-id="07d5c-109">Gets a role instance from a cloud service.</span></span>

## <span data-ttu-id="07d5c-110">示例</span><span class="sxs-lookup"><span data-stu-id="07d5c-110">EXAMPLES</span></span>

### <span data-ttu-id="07d5c-111">範例1：取得所有角色實例</span><span class="sxs-lookup"><span data-stu-id="07d5c-111">Example 1: Get all role instances</span></span>
```powershell
PS C:\> Get-AzCloudServiceRoleInstance -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"

Name                    Location    SkuName        SkuTier
----                    --------    -------        -------
ContosoFrontEnd_IN_0    eastus2euap Standard_D1_v2 Standard
ContosoFrontEnd_IN_1    eastus2euap Standard_D1_v2 Standard
ContosoBackEnd_IN_1     eastus2euap Standard_D1_v2 Standard
ContosoBackEnd_IN_1     eastus2euap Standard_D1_v2 Standard

```

<span data-ttu-id="07d5c-112">這個命令會取得屬於名為 ContosOrg 之資源群組之名為 ContosoCS 之雲端服務所有角色實例的屬性。</span><span class="sxs-lookup"><span data-stu-id="07d5c-112">This command gets the properties of all role instances of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="07d5c-113">範例2：取得單一角色實例的屬性</span><span class="sxs-lookup"><span data-stu-id="07d5c-113">Example 2: Get properties for single role instance</span></span>
```powershell
PS C:\> Get-AzCloudServiceRoleInstance -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"

Name                    Location    SkuName        SkuTier
----                    --------    -------        -------
ContosoFrontEnd_IN_0    eastus2euap Standard_D1_v2 Standard

```

<span data-ttu-id="07d5c-114">這個命令會從屬於名為 ContosOrg 之資源群組的名為 ContosoCS 的雲端服務 ContosoFrontEnd_IN_0，取得該角色實例的屬性。</span><span class="sxs-lookup"><span data-stu-id="07d5c-114">This command gets the properties of the role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="07d5c-115">參數</span><span class="sxs-lookup"><span data-stu-id="07d5c-115">PARAMETERS</span></span>

### <span data-ttu-id="07d5c-116">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="07d5c-116">-CloudServiceName</span></span>
<span data-ttu-id="07d5c-117">.</span><span class="sxs-lookup"><span data-stu-id="07d5c-117">.</span></span>

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

### <span data-ttu-id="07d5c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07d5c-118">-DefaultProfile</span></span>
<span data-ttu-id="07d5c-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="07d5c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07d5c-120">-展開</span><span class="sxs-lookup"><span data-stu-id="07d5c-120">-Expand</span></span>
<span data-ttu-id="07d5c-121">要套用至運算的 expand 運算式。</span><span class="sxs-lookup"><span data-stu-id="07d5c-121">The expand expression to apply to the operation.</span></span>

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

### <span data-ttu-id="07d5c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07d5c-122">-InputObject</span></span>
<span data-ttu-id="07d5c-123">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="07d5c-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="07d5c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07d5c-124">-ResourceGroupName</span></span>
<span data-ttu-id="07d5c-125">.</span><span class="sxs-lookup"><span data-stu-id="07d5c-125">.</span></span>

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

### <span data-ttu-id="07d5c-126">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="07d5c-126">-RoleInstanceName</span></span>
<span data-ttu-id="07d5c-127">角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="07d5c-127">Name of the role instance.</span></span>

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

### <span data-ttu-id="07d5c-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="07d5c-128">-SubscriptionId</span></span>
<span data-ttu-id="07d5c-129">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="07d5c-129">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="07d5c-130">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="07d5c-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="07d5c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07d5c-131">CommonParameters</span></span>
<span data-ttu-id="07d5c-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="07d5c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07d5c-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="07d5c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07d5c-134">輸入</span><span class="sxs-lookup"><span data-stu-id="07d5c-134">INPUTS</span></span>

### <span data-ttu-id="07d5c-135">ICloudServiceIdentity （CloudService）的</span><span class="sxs-lookup"><span data-stu-id="07d5c-135">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="07d5c-136">輸出</span><span class="sxs-lookup"><span data-stu-id="07d5c-136">OUTPUTS</span></span>

### <span data-ttu-id="07d5c-137">IRoleInstance （CloudService）。 Api20201001Preview。</span><span class="sxs-lookup"><span data-stu-id="07d5c-137">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.IRoleInstance</span></span>

## <span data-ttu-id="07d5c-138">筆記</span><span class="sxs-lookup"><span data-stu-id="07d5c-138">NOTES</span></span>

<span data-ttu-id="07d5c-139">別名</span><span class="sxs-lookup"><span data-stu-id="07d5c-139">ALIASES</span></span>

<span data-ttu-id="07d5c-140">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="07d5c-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="07d5c-141">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="07d5c-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="07d5c-142">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="07d5c-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="07d5c-143">INPUTOBJECT <ICloudServiceIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="07d5c-143">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="07d5c-144">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="07d5c-144">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="07d5c-145">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="07d5c-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="07d5c-146">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="07d5c-146">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="07d5c-147">`[RoleInstanceName <String>]`：角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="07d5c-147">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="07d5c-148">`[RoleName <String>]`：角色的名稱。</span><span class="sxs-lookup"><span data-stu-id="07d5c-148">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="07d5c-149">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="07d5c-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="07d5c-150">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="07d5c-150">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="07d5c-151">`[UpdateDomain <Int32?>]`：指定識別更新網域的整數值。</span><span class="sxs-lookup"><span data-stu-id="07d5c-151">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="07d5c-152">更新網域是以零為基礎的索引來標識：第一個更新網域的識別碼為0，第二個是 ID 為1，依此類推。</span><span class="sxs-lookup"><span data-stu-id="07d5c-152">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="07d5c-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="07d5c-153">RELATED LINKS</span></span>

