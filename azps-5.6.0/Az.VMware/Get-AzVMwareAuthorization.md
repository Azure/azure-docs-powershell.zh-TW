---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/get-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwareAuthorization.md
ms.openlocfilehash: dad73292e6875e2cf38244ed74e0519490860c4f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912145"
---
# <span data-ttu-id="96813-101">Get-AzVMWareAuthorization</span><span class="sxs-lookup"><span data-stu-id="96813-101">Get-AzVMWareAuthorization</span></span>

## <span data-ttu-id="96813-102">簡介</span><span class="sxs-lookup"><span data-stu-id="96813-102">SYNOPSIS</span></span>
<span data-ttu-id="96813-103">在私人雲端中以名稱取得 ExpressRoute 回路授權</span><span class="sxs-lookup"><span data-stu-id="96813-103">Get an ExpressRoute Circuit Authorization by name in a private cloud</span></span>

## <span data-ttu-id="96813-104">語法</span><span class="sxs-lookup"><span data-stu-id="96813-104">SYNTAX</span></span>

### <span data-ttu-id="96813-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="96813-105">List (Default)</span></span>
```
Get-AzVMWareAuthorization -PrivateCloudName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="96813-106">獲取</span><span class="sxs-lookup"><span data-stu-id="96813-106">Get</span></span>
```
Get-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="96813-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="96813-107">GetViaIdentity</span></span>
```
Get-AzVMWareAuthorization -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="96813-108">描述</span><span class="sxs-lookup"><span data-stu-id="96813-108">DESCRIPTION</span></span>
<span data-ttu-id="96813-109">在私人雲端中以名稱取得 ExpressRoute 回路授權</span><span class="sxs-lookup"><span data-stu-id="96813-109">Get an ExpressRoute Circuit Authorization by name in a private cloud</span></span>

## <span data-ttu-id="96813-110">例子</span><span class="sxs-lookup"><span data-stu-id="96813-110">EXAMPLES</span></span>

### <span data-ttu-id="96813-111">範例 1：取得授權</span><span class="sxs-lookup"><span data-stu-id="96813-111">Example 1: Get authorization</span></span>
```powershell
PS C:\> Get-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="96813-112">此 Cmdlet 在私人 `azps-test-auth` 雲端下獲得授權 `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="96813-112">This cmdlet gets authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

### <span data-ttu-id="96813-113">範例 2：清單授權</span><span class="sxs-lookup"><span data-stu-id="96813-113">Example 2: List authorization</span></span>
```powershell
PS C:\> Get-AzVMWareAuthorization -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="96813-114">此 Cmdlet 會列出 `azps-test-auth` 私人雲端下的授權 `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="96813-114">This cmdlet lists authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

## <span data-ttu-id="96813-115">參數</span><span class="sxs-lookup"><span data-stu-id="96813-115">PARAMETERS</span></span>

### <span data-ttu-id="96813-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96813-116">-DefaultProfile</span></span>
<span data-ttu-id="96813-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="96813-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96813-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="96813-118">-InputObject</span></span>
<span data-ttu-id="96813-119">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="96813-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="96813-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="96813-120">-Name</span></span>
<span data-ttu-id="96813-121">專用雲端中的 ExpressRoute 回路授權名稱</span><span class="sxs-lookup"><span data-stu-id="96813-121">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AuthorizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96813-122">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="96813-122">-PrivateCloudName</span></span>
<span data-ttu-id="96813-123">私人雲端的名稱</span><span class="sxs-lookup"><span data-stu-id="96813-123">Name of the private cloud</span></span>

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

### <span data-ttu-id="96813-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96813-124">-ResourceGroupName</span></span>
<span data-ttu-id="96813-125">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="96813-125">The name of the resource group.</span></span>
<span data-ttu-id="96813-126">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="96813-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="96813-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="96813-127">-SubscriptionId</span></span>
<span data-ttu-id="96813-128">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="96813-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="96813-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96813-129">CommonParameters</span></span>
<span data-ttu-id="96813-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="96813-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96813-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="96813-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96813-132">輸入</span><span class="sxs-lookup"><span data-stu-id="96813-132">INPUTS</span></span>

### <span data-ttu-id="96813-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.models.I VMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="96813-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="96813-134">輸出</span><span class="sxs-lookup"><span data-stu-id="96813-134">OUTPUTS</span></span>

### <span data-ttu-id="96813-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span><span class="sxs-lookup"><span data-stu-id="96813-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span></span>

## <span data-ttu-id="96813-136">筆記</span><span class="sxs-lookup"><span data-stu-id="96813-136">NOTES</span></span>

<span data-ttu-id="96813-137">別名</span><span class="sxs-lookup"><span data-stu-id="96813-137">ALIASES</span></span>

<span data-ttu-id="96813-138">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="96813-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="96813-139">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="96813-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="96813-140">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="96813-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="96813-141">INPUTOBJECT： <IVMWareIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="96813-141">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="96813-142">`[AuthorizationName <String>]`：專用雲端中的 ExpressRoute 回路授權名稱</span><span class="sxs-lookup"><span data-stu-id="96813-142">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="96813-143">`[ClusterName <String>]`：專用雲端中的組名</span><span class="sxs-lookup"><span data-stu-id="96813-143">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="96813-144">`[HcxEnterpriseSiteName <String>]`：私人雲端中的 HCX 企業網站名稱</span><span class="sxs-lookup"><span data-stu-id="96813-144">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="96813-145">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="96813-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="96813-146">`[Location <String>]`：Azure 區域</span><span class="sxs-lookup"><span data-stu-id="96813-146">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="96813-147">`[PrivateCloudName <String>]`：專用雲端的名稱</span><span class="sxs-lookup"><span data-stu-id="96813-147">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="96813-148">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="96813-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="96813-149">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="96813-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="96813-150">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="96813-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="96813-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="96813-151">RELATED LINKS</span></span>

