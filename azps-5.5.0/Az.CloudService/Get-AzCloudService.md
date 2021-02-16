---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/get-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudService.md
ms.openlocfilehash: faab9e645f05b8b661b03911bcba517e770f4d78
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100141394"
---
# <span data-ttu-id="a93c7-101">Get-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="a93c7-101">Get-AzCloudService</span></span>

## <span data-ttu-id="a93c7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a93c7-102">SYNOPSIS</span></span>
<span data-ttu-id="a93c7-103">顯示雲端服務的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a93c7-103">Display information about a cloud service.</span></span>

## <span data-ttu-id="a93c7-104">句法</span><span class="sxs-lookup"><span data-stu-id="a93c7-104">SYNTAX</span></span>

### <span data-ttu-id="a93c7-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="a93c7-105">List (Default)</span></span>
```
Get-AzCloudService [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a93c7-106">獲取</span><span class="sxs-lookup"><span data-stu-id="a93c7-106">Get</span></span>
```
Get-AzCloudService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a93c7-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a93c7-107">GetViaIdentity</span></span>
```
Get-AzCloudService -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a93c7-108">List1</span><span class="sxs-lookup"><span data-stu-id="a93c7-108">List1</span></span>
```
Get-AzCloudService -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="a93c7-109">說明</span><span class="sxs-lookup"><span data-stu-id="a93c7-109">DESCRIPTION</span></span>
<span data-ttu-id="a93c7-110">顯示雲端服務的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a93c7-110">Display information about a cloud service.</span></span>

## <span data-ttu-id="a93c7-111">示例</span><span class="sxs-lookup"><span data-stu-id="a93c7-111">EXAMPLES</span></span>

### <span data-ttu-id="a93c7-112">範例1：取得資源群組底下的所有雲端服務</span><span class="sxs-lookup"><span data-stu-id="a93c7-112">Example 1: Get all cloud service under a resource group</span></span>
```powershell
PS C:\> Get-AzCloudService -ResourceGroupName "ContosOrg"

ResourceGroupName Name              Location    ProvisioningState
----------------- ----              --------    -----------------
ContosOrg         ContosoCS         eastus2euap Succeeded
ContosOrg         ContosoCSTest     eastus2euap Failed
```

<span data-ttu-id="a93c7-113">這個命令會取得名為 ContosOrg 的資源群組中的所有雲端服務</span><span class="sxs-lookup"><span data-stu-id="a93c7-113">This command gets all cloud services in resource group named ContosOrg</span></span>

### <span data-ttu-id="a93c7-114">範例2：取得雲端服務</span><span class="sxs-lookup"><span data-stu-id="a93c7-114">Example 2: Get cloud service</span></span>
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

<span data-ttu-id="a93c7-115">這個命令會取得名為 ContosoCS 的雲端服務，該名稱屬於名為 ContosOrg 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="a93c7-115">This command gets cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="a93c7-116">參數</span><span class="sxs-lookup"><span data-stu-id="a93c7-116">PARAMETERS</span></span>

### <span data-ttu-id="a93c7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a93c7-117">-DefaultProfile</span></span>
<span data-ttu-id="a93c7-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a93c7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a93c7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a93c7-119">-InputObject</span></span>
<span data-ttu-id="a93c7-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="a93c7-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a93c7-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="a93c7-121">-Name</span></span>
<span data-ttu-id="a93c7-122">雲端服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="a93c7-122">Name of the cloud service.</span></span>

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

### <span data-ttu-id="a93c7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a93c7-123">-ResourceGroupName</span></span>
<span data-ttu-id="a93c7-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a93c7-124">Name of the resource group.</span></span>

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

### <span data-ttu-id="a93c7-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a93c7-125">-SubscriptionId</span></span>
<span data-ttu-id="a93c7-126">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="a93c7-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a93c7-127">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="a93c7-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a93c7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a93c7-128">CommonParameters</span></span>
<span data-ttu-id="a93c7-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a93c7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a93c7-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a93c7-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a93c7-131">輸入</span><span class="sxs-lookup"><span data-stu-id="a93c7-131">INPUTS</span></span>

### <span data-ttu-id="a93c7-132">ICloudServiceIdentity （CloudService）的</span><span class="sxs-lookup"><span data-stu-id="a93c7-132">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="a93c7-133">輸出</span><span class="sxs-lookup"><span data-stu-id="a93c7-133">OUTPUTS</span></span>

### <span data-ttu-id="a93c7-134">ICloudService （CloudService）。 Api20201001Preview。</span><span class="sxs-lookup"><span data-stu-id="a93c7-134">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span></span>

## <span data-ttu-id="a93c7-135">筆記</span><span class="sxs-lookup"><span data-stu-id="a93c7-135">NOTES</span></span>

<span data-ttu-id="a93c7-136">別名</span><span class="sxs-lookup"><span data-stu-id="a93c7-136">ALIASES</span></span>

<span data-ttu-id="a93c7-137">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="a93c7-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a93c7-138">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="a93c7-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a93c7-139">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="a93c7-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a93c7-140">INPUTOBJECT <ICloudServiceIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="a93c7-140">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a93c7-141">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="a93c7-141">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="a93c7-142">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="a93c7-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a93c7-143">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="a93c7-143">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="a93c7-144">`[RoleInstanceName <String>]`：角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="a93c7-144">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="a93c7-145">`[RoleName <String>]`：角色的名稱。</span><span class="sxs-lookup"><span data-stu-id="a93c7-145">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="a93c7-146">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="a93c7-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a93c7-147">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="a93c7-147">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="a93c7-148">`[UpdateDomain <Int32?>]`：指定識別更新網域的整數值。</span><span class="sxs-lookup"><span data-stu-id="a93c7-148">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="a93c7-149">更新網域是以零為基礎的索引來標識：第一個更新網域的識別碼為0，第二個是 ID 為1，依此類推。</span><span class="sxs-lookup"><span data-stu-id="a93c7-149">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="a93c7-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="a93c7-150">RELATED LINKS</span></span>

