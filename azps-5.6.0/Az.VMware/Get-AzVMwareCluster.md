---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/get-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwareCluster.md
ms.openlocfilehash: 842d0c26d4034a8c07415dfe8524b32623c07e89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910822"
---
# <span data-ttu-id="313da-101">Get-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="313da-101">Get-AzVMWareCluster</span></span>

## <span data-ttu-id="313da-102">簡介</span><span class="sxs-lookup"><span data-stu-id="313da-102">SYNOPSIS</span></span>
<span data-ttu-id="313da-103">在私人雲端中以名稱取得組群</span><span class="sxs-lookup"><span data-stu-id="313da-103">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="313da-104">語法</span><span class="sxs-lookup"><span data-stu-id="313da-104">SYNTAX</span></span>

### <span data-ttu-id="313da-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="313da-105">List (Default)</span></span>
```
Get-AzVMWareCluster -PrivateCloudName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="313da-106">獲取</span><span class="sxs-lookup"><span data-stu-id="313da-106">Get</span></span>
```
Get-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="313da-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="313da-107">GetViaIdentity</span></span>
```
Get-AzVMWareCluster -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="313da-108">描述</span><span class="sxs-lookup"><span data-stu-id="313da-108">DESCRIPTION</span></span>
<span data-ttu-id="313da-109">在私人雲端中以名稱取得組群</span><span class="sxs-lookup"><span data-stu-id="313da-109">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="313da-110">例子</span><span class="sxs-lookup"><span data-stu-id="313da-110">EXAMPLES</span></span>

### <span data-ttu-id="313da-111">範例 1：取得集區</span><span class="sxs-lookup"><span data-stu-id="313da-111">Example 1: Get cluster</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="313da-112">取得集區</span><span class="sxs-lookup"><span data-stu-id="313da-112">Get cluster</span></span>

### <span data-ttu-id="313da-113">範例 2：清單組</span><span class="sxs-lookup"><span data-stu-id="313da-113">Example 2: List clusters</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="313da-114">清單組</span><span class="sxs-lookup"><span data-stu-id="313da-114">List clusters</span></span>

## <span data-ttu-id="313da-115">參數</span><span class="sxs-lookup"><span data-stu-id="313da-115">PARAMETERS</span></span>

### <span data-ttu-id="313da-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="313da-116">-DefaultProfile</span></span>
<span data-ttu-id="313da-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="313da-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="313da-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="313da-118">-InputObject</span></span>
<span data-ttu-id="313da-119">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="313da-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="313da-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="313da-120">-Name</span></span>
<span data-ttu-id="313da-121">專用雲端中的組名</span><span class="sxs-lookup"><span data-stu-id="313da-121">Name of the cluster in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="313da-122">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="313da-122">-PrivateCloudName</span></span>
<span data-ttu-id="313da-123">私人雲端的名稱</span><span class="sxs-lookup"><span data-stu-id="313da-123">Name of the private cloud</span></span>

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

### <span data-ttu-id="313da-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="313da-124">-ResourceGroupName</span></span>
<span data-ttu-id="313da-125">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="313da-125">The name of the resource group.</span></span>
<span data-ttu-id="313da-126">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="313da-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="313da-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="313da-127">-SubscriptionId</span></span>
<span data-ttu-id="313da-128">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="313da-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="313da-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="313da-129">CommonParameters</span></span>
<span data-ttu-id="313da-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="313da-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="313da-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="313da-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="313da-132">輸入</span><span class="sxs-lookup"><span data-stu-id="313da-132">INPUTS</span></span>

### <span data-ttu-id="313da-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.models.I VMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="313da-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="313da-134">輸出</span><span class="sxs-lookup"><span data-stu-id="313da-134">OUTPUTS</span></span>

### <span data-ttu-id="313da-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span><span class="sxs-lookup"><span data-stu-id="313da-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="313da-136">筆記</span><span class="sxs-lookup"><span data-stu-id="313da-136">NOTES</span></span>

<span data-ttu-id="313da-137">別名</span><span class="sxs-lookup"><span data-stu-id="313da-137">ALIASES</span></span>

<span data-ttu-id="313da-138">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="313da-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="313da-139">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="313da-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="313da-140">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="313da-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="313da-141">INPUTOBJECT： <IVMWareIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="313da-141">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="313da-142">`[AuthorizationName <String>]`：專用雲端中的 ExpressRoute 回路授權名稱</span><span class="sxs-lookup"><span data-stu-id="313da-142">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="313da-143">`[ClusterName <String>]`：專用雲端中的組名</span><span class="sxs-lookup"><span data-stu-id="313da-143">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="313da-144">`[HcxEnterpriseSiteName <String>]`：私人雲端中的 HCX 企業網站名稱</span><span class="sxs-lookup"><span data-stu-id="313da-144">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="313da-145">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="313da-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="313da-146">`[Location <String>]`：Azure 區域</span><span class="sxs-lookup"><span data-stu-id="313da-146">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="313da-147">`[PrivateCloudName <String>]`：專用雲端的名稱</span><span class="sxs-lookup"><span data-stu-id="313da-147">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="313da-148">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="313da-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="313da-149">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="313da-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="313da-150">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="313da-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="313da-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="313da-151">RELATED LINKS</span></span>

