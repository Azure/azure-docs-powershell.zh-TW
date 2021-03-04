---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/get-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudService.md
ms.openlocfilehash: 31683a7f8d0bea3a2e21588b0451275c74d52e97
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917098"
---
# <span data-ttu-id="70305-101">Get-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="70305-101">Get-AzCloudService</span></span>

## <span data-ttu-id="70305-102">簡介</span><span class="sxs-lookup"><span data-stu-id="70305-102">SYNOPSIS</span></span>
<span data-ttu-id="70305-103">顯示雲端服務的資訊。</span><span class="sxs-lookup"><span data-stu-id="70305-103">Display information about a cloud service.</span></span>

## <span data-ttu-id="70305-104">語法</span><span class="sxs-lookup"><span data-stu-id="70305-104">SYNTAX</span></span>

### <span data-ttu-id="70305-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="70305-105">List (Default)</span></span>
```
Get-AzCloudService [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="70305-106">獲取</span><span class="sxs-lookup"><span data-stu-id="70305-106">Get</span></span>
```
Get-AzCloudService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="70305-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="70305-107">GetViaIdentity</span></span>
```
Get-AzCloudService -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="70305-108">清單1</span><span class="sxs-lookup"><span data-stu-id="70305-108">List1</span></span>
```
Get-AzCloudService -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="70305-109">描述</span><span class="sxs-lookup"><span data-stu-id="70305-109">DESCRIPTION</span></span>
<span data-ttu-id="70305-110">顯示雲端服務的資訊。</span><span class="sxs-lookup"><span data-stu-id="70305-110">Display information about a cloud service.</span></span>

## <span data-ttu-id="70305-111">例子</span><span class="sxs-lookup"><span data-stu-id="70305-111">EXAMPLES</span></span>

### <span data-ttu-id="70305-112">範例 1：在資源群組下取得所有雲端服務</span><span class="sxs-lookup"><span data-stu-id="70305-112">Example 1: Get all cloud service under a resource group</span></span>
```powershell
PS C:\> Get-AzCloudService -ResourceGroupName "ContosOrg"

ResourceGroupName Name              Location    ProvisioningState
----------------- ----              --------    -----------------
ContosOrg         ContosoCS         eastus2euap Succeeded
ContosOrg         ContosoCSTest     eastus2euap Failed
```

<span data-ttu-id="70305-113">此命令會獲得資源群組中名為 ContosOrg 的所有雲端服務</span><span class="sxs-lookup"><span data-stu-id="70305-113">This command gets all cloud services in resource group named ContosOrg</span></span>

### <span data-ttu-id="70305-114">範例 2：取得雲端服務</span><span class="sxs-lookup"><span data-stu-id="70305-114">Example 2: Get cloud service</span></span>
```powershell
PS C:\> Get-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"

ResourceGroupName Name              Location    ProvisioningState
----------------- ----              --------    -----------------
ContosOrg         ContosoCS         eastus2euap Succeeded

PS C:\> $cloudService = Get-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"
PS C:\> $cloudService | Format-List
ResourceGroupName : ContosOrg
Configuration     : xxxxxxxx
ConfigurationUrl  :
ExtensionProfile  : xxxxxxxx
Id                : xxxxxxxx
Location          : East US
Name              : ContosoCS
NetworkProfile    : xxxxxxxx
OSProfile         : xxxxxxxx
PackageUrl        : xxxxxxxx
ProvisioningState : Succeeded
RoleProfile       : xxxxxxxx
StartCloudService :
Tag               : {
                      "Owner": "Contos"
                    }
Type              : Microsoft.Compute/cloudServices
UniqueId          : xxxxxxxx
UpgradeMode       : Auto

```

<span data-ttu-id="70305-115">此命令會獲得名為 ContosoCS 的雲端服務，該服務屬於名為 ContosOrg 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="70305-115">This command gets cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="70305-116">參數</span><span class="sxs-lookup"><span data-stu-id="70305-116">PARAMETERS</span></span>

### <span data-ttu-id="70305-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70305-117">-DefaultProfile</span></span>
<span data-ttu-id="70305-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="70305-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70305-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70305-119">-InputObject</span></span>
<span data-ttu-id="70305-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="70305-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="70305-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="70305-121">-Name</span></span>
<span data-ttu-id="70305-122">雲端服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="70305-122">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70305-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70305-123">-ResourceGroupName</span></span>
<span data-ttu-id="70305-124">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="70305-124">Name of the resource group.</span></span>

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

### <span data-ttu-id="70305-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="70305-125">-SubscriptionId</span></span>
<span data-ttu-id="70305-126">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="70305-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="70305-127">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="70305-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="70305-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70305-128">CommonParameters</span></span>
<span data-ttu-id="70305-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="70305-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70305-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="70305-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70305-131">輸入</span><span class="sxs-lookup"><span data-stu-id="70305-131">INPUTS</span></span>

### <span data-ttu-id="70305-132">Microsoft.Azure.PowerShell.Cmdlets.CloudService.models.iCloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="70305-132">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="70305-133">輸出</span><span class="sxs-lookup"><span data-stu-id="70305-133">OUTPUTS</span></span>

### <span data-ttu-id="70305-134">Microsoft.Azure.PowerShell.Cmdlets.CloudService.models.Api20201001Preview.ICloudService</span><span class="sxs-lookup"><span data-stu-id="70305-134">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span></span>

## <span data-ttu-id="70305-135">筆記</span><span class="sxs-lookup"><span data-stu-id="70305-135">NOTES</span></span>

<span data-ttu-id="70305-136">別名</span><span class="sxs-lookup"><span data-stu-id="70305-136">ALIASES</span></span>

<span data-ttu-id="70305-137">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="70305-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="70305-138">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="70305-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="70305-139">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="70305-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="70305-140">INPUTOBJECT： <ICloudServiceIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="70305-140">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="70305-141">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="70305-141">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="70305-142">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="70305-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="70305-143">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="70305-143">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="70305-144">`[RoleInstanceName <String>]`：角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="70305-144">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="70305-145">`[RoleName <String>]`：角色名稱。</span><span class="sxs-lookup"><span data-stu-id="70305-145">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="70305-146">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="70305-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="70305-147">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="70305-147">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="70305-148">`[UpdateDomain <Int32?>]`：指定可識別更新網域的整數值。</span><span class="sxs-lookup"><span data-stu-id="70305-148">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="70305-149">更新網域會以零型索引識別：第一個更新網域的識別碼為 0，第二個更新網域的識別碼為 1，以此類比。</span><span class="sxs-lookup"><span data-stu-id="70305-149">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="70305-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="70305-150">RELATED LINKS</span></span>

