---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/get-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwarePrivateCloud.md
ms.openlocfilehash: ae53ac56d60d61340e2592233901556a0e1d6b62
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911238"
---
# <span data-ttu-id="40c8a-101">Get-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="40c8a-101">Get-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="40c8a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="40c8a-102">SYNOPSIS</span></span>
<span data-ttu-id="40c8a-103">取得私人雲端</span><span class="sxs-lookup"><span data-stu-id="40c8a-103">Get a private cloud</span></span>

## <span data-ttu-id="40c8a-104">語法</span><span class="sxs-lookup"><span data-stu-id="40c8a-104">SYNTAX</span></span>

### <span data-ttu-id="40c8a-105">清單1 (預設) </span><span class="sxs-lookup"><span data-stu-id="40c8a-105">List1 (Default)</span></span>
```
Get-AzVMWarePrivateCloud [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="40c8a-106">獲取</span><span class="sxs-lookup"><span data-stu-id="40c8a-106">Get</span></span>
```
Get-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="40c8a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="40c8a-107">GetViaIdentity</span></span>
```
Get-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="40c8a-108">清單</span><span class="sxs-lookup"><span data-stu-id="40c8a-108">List</span></span>
```
Get-AzVMWarePrivateCloud -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="40c8a-109">描述</span><span class="sxs-lookup"><span data-stu-id="40c8a-109">DESCRIPTION</span></span>
<span data-ttu-id="40c8a-110">取得私人雲端</span><span class="sxs-lookup"><span data-stu-id="40c8a-110">Get a private cloud</span></span>

## <span data-ttu-id="40c8a-111">例子</span><span class="sxs-lookup"><span data-stu-id="40c8a-111">EXAMPLES</span></span>

### <span data-ttu-id="40c8a-112">範例 1：在訂閱下列出私人雲端</span><span class="sxs-lookup"><span data-stu-id="40c8a-112">Example 1: List private cloud under subscription</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="40c8a-113">在訂閱下列出私人雲端</span><span class="sxs-lookup"><span data-stu-id="40c8a-113">List private cloud under subscription</span></span>

### <span data-ttu-id="40c8a-114">範例 2：在資源群組下列出私人雲端</span><span class="sxs-lookup"><span data-stu-id="40c8a-114">Example 2: List private cloud under resource group</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="40c8a-115">在資源群組下列出私人雲端</span><span class="sxs-lookup"><span data-stu-id="40c8a-115">List private cloud under resource group</span></span>

### <span data-ttu-id="40c8a-116">範例 3：取得私人雲端</span><span class="sxs-lookup"><span data-stu-id="40c8a-116">Example 3: Get private cloud</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="40c8a-117">取得私人雲端</span><span class="sxs-lookup"><span data-stu-id="40c8a-117">Get private cloud</span></span>

## <span data-ttu-id="40c8a-118">參數</span><span class="sxs-lookup"><span data-stu-id="40c8a-118">PARAMETERS</span></span>

### <span data-ttu-id="40c8a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40c8a-119">-DefaultProfile</span></span>
<span data-ttu-id="40c8a-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="40c8a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40c8a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40c8a-121">-InputObject</span></span>
<span data-ttu-id="40c8a-122">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="40c8a-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="40c8a-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="40c8a-123">-Name</span></span>
<span data-ttu-id="40c8a-124">私人雲端的名稱</span><span class="sxs-lookup"><span data-stu-id="40c8a-124">Name of the private cloud</span></span>

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

### <span data-ttu-id="40c8a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40c8a-125">-ResourceGroupName</span></span>
<span data-ttu-id="40c8a-126">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="40c8a-126">The name of the resource group.</span></span>
<span data-ttu-id="40c8a-127">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="40c8a-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="40c8a-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="40c8a-128">-SubscriptionId</span></span>
<span data-ttu-id="40c8a-129">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="40c8a-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="40c8a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40c8a-130">CommonParameters</span></span>
<span data-ttu-id="40c8a-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="40c8a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40c8a-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="40c8a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40c8a-133">輸入</span><span class="sxs-lookup"><span data-stu-id="40c8a-133">INPUTS</span></span>

### <span data-ttu-id="40c8a-134">Microsoft.Azure.PowerShell.Cmdlets.VMWare.models.I VMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="40c8a-134">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="40c8a-135">輸出</span><span class="sxs-lookup"><span data-stu-id="40c8a-135">OUTPUTS</span></span>

### <span data-ttu-id="40c8a-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="40c8a-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="40c8a-137">筆記</span><span class="sxs-lookup"><span data-stu-id="40c8a-137">NOTES</span></span>

<span data-ttu-id="40c8a-138">別名</span><span class="sxs-lookup"><span data-stu-id="40c8a-138">ALIASES</span></span>

<span data-ttu-id="40c8a-139">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="40c8a-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="40c8a-140">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="40c8a-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="40c8a-141">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="40c8a-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="40c8a-142">INPUTOBJECT： <IVMWareIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="40c8a-142">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="40c8a-143">`[AuthorizationName <String>]`：專用雲端中的 ExpressRoute 回路授權名稱</span><span class="sxs-lookup"><span data-stu-id="40c8a-143">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="40c8a-144">`[ClusterName <String>]`：專用雲端中的組名</span><span class="sxs-lookup"><span data-stu-id="40c8a-144">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="40c8a-145">`[HcxEnterpriseSiteName <String>]`：私人雲端中的 HCX 企業網站名稱</span><span class="sxs-lookup"><span data-stu-id="40c8a-145">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="40c8a-146">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="40c8a-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="40c8a-147">`[Location <String>]`：Azure 區域</span><span class="sxs-lookup"><span data-stu-id="40c8a-147">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="40c8a-148">`[PrivateCloudName <String>]`：專用雲端的名稱</span><span class="sxs-lookup"><span data-stu-id="40c8a-148">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="40c8a-149">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="40c8a-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="40c8a-150">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="40c8a-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="40c8a-151">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="40c8a-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="40c8a-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="40c8a-152">RELATED LINKS</span></span>

