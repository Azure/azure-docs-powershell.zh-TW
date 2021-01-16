---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWareAuthorization.md
ms.openlocfilehash: fc89f62711744ad1e6bd7182eeb61fffd0478eaf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279360"
---
# <span data-ttu-id="1e1cf-101">Get-AzVMWareAuthorization</span><span class="sxs-lookup"><span data-stu-id="1e1cf-101">Get-AzVMWareAuthorization</span></span>

## <span data-ttu-id="1e1cf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1e1cf-102">SYNOPSIS</span></span>
<span data-ttu-id="1e1cf-103">在私有雲端取得 ExpressRoute 線路授權（依名稱）</span><span class="sxs-lookup"><span data-stu-id="1e1cf-103">Get an ExpressRoute Circuit Authorization by name in a private cloud</span></span>

## <span data-ttu-id="1e1cf-104">句法</span><span class="sxs-lookup"><span data-stu-id="1e1cf-104">SYNTAX</span></span>

### <span data-ttu-id="1e1cf-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="1e1cf-105">List (Default)</span></span>
```
Get-AzVMWareAuthorization -PrivateCloudName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1e1cf-106">獲取</span><span class="sxs-lookup"><span data-stu-id="1e1cf-106">Get</span></span>
```
Get-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1e1cf-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1e1cf-107">GetViaIdentity</span></span>
```
Get-AzVMWareAuthorization -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="1e1cf-108">說明</span><span class="sxs-lookup"><span data-stu-id="1e1cf-108">DESCRIPTION</span></span>
<span data-ttu-id="1e1cf-109">在私有雲端取得 ExpressRoute 線路授權（依名稱）</span><span class="sxs-lookup"><span data-stu-id="1e1cf-109">Get an ExpressRoute Circuit Authorization by name in a private cloud</span></span>

## <span data-ttu-id="1e1cf-110">示例</span><span class="sxs-lookup"><span data-stu-id="1e1cf-110">EXAMPLES</span></span>

### <span data-ttu-id="1e1cf-111">範例1：取得授權</span><span class="sxs-lookup"><span data-stu-id="1e1cf-111">Example 1: Get authorization</span></span>
```powershell
PS C:\> Get-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="1e1cf-112">這個 Cmdlet 會 `azps-test-auth` 在私有雲端下取得授權 `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="1e1cf-112">This cmdlet gets authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

### <span data-ttu-id="1e1cf-113">範例2：清單授權</span><span class="sxs-lookup"><span data-stu-id="1e1cf-113">Example 2: List authorization</span></span>
```powershell
PS C:\> Get-AzVMWareAuthorization -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="1e1cf-114">這個 Cmdlet 會列出 [ `azps-test-auth` 私人雲端] 下的授權 `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="1e1cf-114">This cmdlet lists authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

## <span data-ttu-id="1e1cf-115">參數</span><span class="sxs-lookup"><span data-stu-id="1e1cf-115">PARAMETERS</span></span>

### <span data-ttu-id="1e1cf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e1cf-116">-DefaultProfile</span></span>
<span data-ttu-id="1e1cf-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1e1cf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e1cf-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e1cf-118">-InputObject</span></span>
<span data-ttu-id="1e1cf-119">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="1e1cf-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1e1cf-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="1e1cf-120">-Name</span></span>
<span data-ttu-id="1e1cf-121">私有雲端中 ExpressRoute 線路授權的名稱</span><span class="sxs-lookup"><span data-stu-id="1e1cf-121">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

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

### <span data-ttu-id="1e1cf-122">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="1e1cf-122">-PrivateCloudName</span></span>
<span data-ttu-id="1e1cf-123">私有雲端的名稱</span><span class="sxs-lookup"><span data-stu-id="1e1cf-123">Name of the private cloud</span></span>

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

### <span data-ttu-id="1e1cf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e1cf-124">-ResourceGroupName</span></span>
<span data-ttu-id="1e1cf-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1e1cf-125">The name of the resource group.</span></span>
<span data-ttu-id="1e1cf-126">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="1e1cf-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="1e1cf-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1e1cf-127">-SubscriptionId</span></span>
<span data-ttu-id="1e1cf-128">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="1e1cf-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="1e1cf-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e1cf-129">CommonParameters</span></span>
<span data-ttu-id="1e1cf-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1e1cf-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e1cf-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1e1cf-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e1cf-132">輸入</span><span class="sxs-lookup"><span data-stu-id="1e1cf-132">INPUTS</span></span>

### <span data-ttu-id="1e1cf-133">IVMWareIdentity 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1e1cf-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="1e1cf-134">輸出</span><span class="sxs-lookup"><span data-stu-id="1e1cf-134">OUTPUTS</span></span>

### <span data-ttu-id="1e1cf-135">IExpressRouteAuthorization 中的 Api20200320 （）。</span><span class="sxs-lookup"><span data-stu-id="1e1cf-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span></span>

## <span data-ttu-id="1e1cf-136">筆記</span><span class="sxs-lookup"><span data-stu-id="1e1cf-136">NOTES</span></span>

<span data-ttu-id="1e1cf-137">別名</span><span class="sxs-lookup"><span data-stu-id="1e1cf-137">ALIASES</span></span>

<span data-ttu-id="1e1cf-138">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="1e1cf-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1e1cf-139">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="1e1cf-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1e1cf-140">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="1e1cf-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1e1cf-141">INPUTOBJECT <IVMWareIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="1e1cf-141">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1e1cf-142">`[AuthorizationName <String>]`：私人雲端中 ExpressRoute 線路授權的名稱</span><span class="sxs-lookup"><span data-stu-id="1e1cf-142">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="1e1cf-143">`[ClusterName <String>]`：私人雲端中的群集名稱</span><span class="sxs-lookup"><span data-stu-id="1e1cf-143">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="1e1cf-144">`[HcxEnterpriseSiteName <String>]`：私人雲端中的 HCX 企業網站名稱</span><span class="sxs-lookup"><span data-stu-id="1e1cf-144">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="1e1cf-145">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="1e1cf-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1e1cf-146">`[Location <String>]`： Azure region</span><span class="sxs-lookup"><span data-stu-id="1e1cf-146">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="1e1cf-147">`[PrivateCloudName <String>]`：私人雲端的名稱</span><span class="sxs-lookup"><span data-stu-id="1e1cf-147">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="1e1cf-148">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1e1cf-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="1e1cf-149">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="1e1cf-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="1e1cf-150">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1e1cf-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="1e1cf-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="1e1cf-151">RELATED LINKS</span></span>

