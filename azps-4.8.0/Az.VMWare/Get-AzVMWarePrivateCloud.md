---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloud.md
ms.openlocfilehash: 31400d3b9b6e57190a852ae579fffcaa9fc60401
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129381"
---
# <span data-ttu-id="ef826-101">Get-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="ef826-101">Get-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="ef826-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ef826-102">SYNOPSIS</span></span>
<span data-ttu-id="ef826-103">取得私有雲端</span><span class="sxs-lookup"><span data-stu-id="ef826-103">Get a private cloud</span></span>

## <span data-ttu-id="ef826-104">句法</span><span class="sxs-lookup"><span data-stu-id="ef826-104">SYNTAX</span></span>

### <span data-ttu-id="ef826-105">List1 (預設) </span><span class="sxs-lookup"><span data-stu-id="ef826-105">List1 (Default)</span></span>
```
Get-AzVMWarePrivateCloud [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ef826-106">獲取</span><span class="sxs-lookup"><span data-stu-id="ef826-106">Get</span></span>
```
Get-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ef826-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ef826-107">GetViaIdentity</span></span>
```
Get-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ef826-108">清單</span><span class="sxs-lookup"><span data-stu-id="ef826-108">List</span></span>
```
Get-AzVMWarePrivateCloud -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="ef826-109">說明</span><span class="sxs-lookup"><span data-stu-id="ef826-109">DESCRIPTION</span></span>
<span data-ttu-id="ef826-110">取得私有雲端</span><span class="sxs-lookup"><span data-stu-id="ef826-110">Get a private cloud</span></span>

## <span data-ttu-id="ef826-111">示例</span><span class="sxs-lookup"><span data-stu-id="ef826-111">EXAMPLES</span></span>

### <span data-ttu-id="ef826-112">範例1：在 [訂閱] 底下列出私人雲端</span><span class="sxs-lookup"><span data-stu-id="ef826-112">Example 1: List private cloud under subscription</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="ef826-113">[訂閱] 下的清單私人雲端</span><span class="sxs-lookup"><span data-stu-id="ef826-113">List private cloud under subscription</span></span>

### <span data-ttu-id="ef826-114">範例2：在 [資源群組] 下列出私人雲端</span><span class="sxs-lookup"><span data-stu-id="ef826-114">Example 2: List private cloud under resource group</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="ef826-115">[資源群組] 下的 [清單私人雲端]</span><span class="sxs-lookup"><span data-stu-id="ef826-115">List private cloud under resource group</span></span>

### <span data-ttu-id="ef826-116">範例3：取得私有雲端</span><span class="sxs-lookup"><span data-stu-id="ef826-116">Example 3: Get private cloud</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="ef826-117">取得私有雲端</span><span class="sxs-lookup"><span data-stu-id="ef826-117">Get private cloud</span></span>

## <span data-ttu-id="ef826-118">參數</span><span class="sxs-lookup"><span data-stu-id="ef826-118">PARAMETERS</span></span>

### <span data-ttu-id="ef826-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef826-119">-DefaultProfile</span></span>
<span data-ttu-id="ef826-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ef826-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef826-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef826-121">-InputObject</span></span>
<span data-ttu-id="ef826-122">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="ef826-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ef826-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="ef826-123">-Name</span></span>
<span data-ttu-id="ef826-124">私有雲端的名稱</span><span class="sxs-lookup"><span data-stu-id="ef826-124">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef826-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef826-125">-ResourceGroupName</span></span>
<span data-ttu-id="ef826-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ef826-126">The name of the resource group.</span></span>
<span data-ttu-id="ef826-127">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="ef826-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ef826-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ef826-128">-SubscriptionId</span></span>
<span data-ttu-id="ef826-129">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="ef826-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ef826-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef826-130">CommonParameters</span></span>
<span data-ttu-id="ef826-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ef826-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef826-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ef826-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef826-133">輸入</span><span class="sxs-lookup"><span data-stu-id="ef826-133">INPUTS</span></span>

### <span data-ttu-id="ef826-134">IVMWareIdentity 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ef826-134">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="ef826-135">輸出</span><span class="sxs-lookup"><span data-stu-id="ef826-135">OUTPUTS</span></span>

### <span data-ttu-id="ef826-136">IPrivateCloud 中的 Api20200320 （）。</span><span class="sxs-lookup"><span data-stu-id="ef826-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="ef826-137">筆記</span><span class="sxs-lookup"><span data-stu-id="ef826-137">NOTES</span></span>

<span data-ttu-id="ef826-138">別名</span><span class="sxs-lookup"><span data-stu-id="ef826-138">ALIASES</span></span>

<span data-ttu-id="ef826-139">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="ef826-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ef826-140">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="ef826-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ef826-141">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="ef826-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ef826-142">INPUTOBJECT <IVMWareIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="ef826-142">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ef826-143">`[AuthorizationName <String>]`：私人雲端中 ExpressRoute 線路授權的名稱</span><span class="sxs-lookup"><span data-stu-id="ef826-143">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="ef826-144">`[ClusterName <String>]`：私人雲端中的群集名稱</span><span class="sxs-lookup"><span data-stu-id="ef826-144">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="ef826-145">`[HcxEnterpriseSiteName <String>]`：私人雲端中的 HCX 企業網站名稱</span><span class="sxs-lookup"><span data-stu-id="ef826-145">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="ef826-146">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="ef826-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ef826-147">`[Location <String>]`： Azure region</span><span class="sxs-lookup"><span data-stu-id="ef826-147">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="ef826-148">`[PrivateCloudName <String>]`：私人雲端的名稱</span><span class="sxs-lookup"><span data-stu-id="ef826-148">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="ef826-149">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ef826-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ef826-150">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="ef826-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="ef826-151">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ef826-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="ef826-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="ef826-152">RELATED LINKS</span></span>

