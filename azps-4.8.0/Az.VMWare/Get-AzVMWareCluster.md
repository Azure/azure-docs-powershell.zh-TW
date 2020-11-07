---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWareCluster.md
ms.openlocfilehash: bf763e152c482c4a3fda4951715b01008a730533
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93968887"
---
# <span data-ttu-id="34b86-101">Get-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="34b86-101">Get-AzVMWareCluster</span></span>

## <span data-ttu-id="34b86-102">摘要</span><span class="sxs-lookup"><span data-stu-id="34b86-102">SYNOPSIS</span></span>
<span data-ttu-id="34b86-103">在私有雲端以名稱取得群集</span><span class="sxs-lookup"><span data-stu-id="34b86-103">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="34b86-104">句法</span><span class="sxs-lookup"><span data-stu-id="34b86-104">SYNTAX</span></span>

### <span data-ttu-id="34b86-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="34b86-105">List (Default)</span></span>
```
Get-AzVMWareCluster -PrivateCloudName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="34b86-106">獲取</span><span class="sxs-lookup"><span data-stu-id="34b86-106">Get</span></span>
```
Get-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="34b86-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="34b86-107">GetViaIdentity</span></span>
```
Get-AzVMWareCluster -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="34b86-108">說明</span><span class="sxs-lookup"><span data-stu-id="34b86-108">DESCRIPTION</span></span>
<span data-ttu-id="34b86-109">在私有雲端以名稱取得群集</span><span class="sxs-lookup"><span data-stu-id="34b86-109">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="34b86-110">示例</span><span class="sxs-lookup"><span data-stu-id="34b86-110">EXAMPLES</span></span>

### <span data-ttu-id="34b86-111">範例1：取得群集</span><span class="sxs-lookup"><span data-stu-id="34b86-111">Example 1: Get cluster</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="34b86-112">取得群集</span><span class="sxs-lookup"><span data-stu-id="34b86-112">Get cluster</span></span>

### <span data-ttu-id="34b86-113">範例2：清單群集</span><span class="sxs-lookup"><span data-stu-id="34b86-113">Example 2: List clusters</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="34b86-114">清單群集</span><span class="sxs-lookup"><span data-stu-id="34b86-114">List clusters</span></span>

## <span data-ttu-id="34b86-115">參數</span><span class="sxs-lookup"><span data-stu-id="34b86-115">PARAMETERS</span></span>

### <span data-ttu-id="34b86-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34b86-116">-DefaultProfile</span></span>
<span data-ttu-id="34b86-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="34b86-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34b86-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34b86-118">-InputObject</span></span>
<span data-ttu-id="34b86-119">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="34b86-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="34b86-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="34b86-120">-Name</span></span>
<span data-ttu-id="34b86-121">私人雲端中的群集名稱</span><span class="sxs-lookup"><span data-stu-id="34b86-121">Name of the cluster in the private cloud</span></span>

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

### <span data-ttu-id="34b86-122">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="34b86-122">-PrivateCloudName</span></span>
<span data-ttu-id="34b86-123">私有雲端的名稱</span><span class="sxs-lookup"><span data-stu-id="34b86-123">Name of the private cloud</span></span>

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

### <span data-ttu-id="34b86-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34b86-124">-ResourceGroupName</span></span>
<span data-ttu-id="34b86-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="34b86-125">The name of the resource group.</span></span>
<span data-ttu-id="34b86-126">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="34b86-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="34b86-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="34b86-127">-SubscriptionId</span></span>
<span data-ttu-id="34b86-128">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="34b86-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="34b86-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34b86-129">CommonParameters</span></span>
<span data-ttu-id="34b86-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="34b86-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34b86-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="34b86-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34b86-132">輸入</span><span class="sxs-lookup"><span data-stu-id="34b86-132">INPUTS</span></span>

### <span data-ttu-id="34b86-133">IVMWareIdentity 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="34b86-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="34b86-134">輸出</span><span class="sxs-lookup"><span data-stu-id="34b86-134">OUTPUTS</span></span>

### <span data-ttu-id="34b86-135">ICluster 中的 Api20200320 （）。</span><span class="sxs-lookup"><span data-stu-id="34b86-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="34b86-136">筆記</span><span class="sxs-lookup"><span data-stu-id="34b86-136">NOTES</span></span>

<span data-ttu-id="34b86-137">別名</span><span class="sxs-lookup"><span data-stu-id="34b86-137">ALIASES</span></span>

<span data-ttu-id="34b86-138">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="34b86-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="34b86-139">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="34b86-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="34b86-140">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="34b86-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="34b86-141">INPUTOBJECT <IVMWareIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="34b86-141">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="34b86-142">`[AuthorizationName <String>]`：私人雲端中 ExpressRoute 線路授權的名稱</span><span class="sxs-lookup"><span data-stu-id="34b86-142">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="34b86-143">`[ClusterName <String>]`：私人雲端中的群集名稱</span><span class="sxs-lookup"><span data-stu-id="34b86-143">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="34b86-144">`[HcxEnterpriseSiteName <String>]`：私人雲端中的 HCX 企業網站名稱</span><span class="sxs-lookup"><span data-stu-id="34b86-144">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="34b86-145">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="34b86-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="34b86-146">`[Location <String>]`： Azure region</span><span class="sxs-lookup"><span data-stu-id="34b86-146">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="34b86-147">`[PrivateCloudName <String>]`：私人雲端的名稱</span><span class="sxs-lookup"><span data-stu-id="34b86-147">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="34b86-148">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="34b86-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="34b86-149">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="34b86-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="34b86-150">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="34b86-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="34b86-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="34b86-151">RELATED LINKS</span></span>

