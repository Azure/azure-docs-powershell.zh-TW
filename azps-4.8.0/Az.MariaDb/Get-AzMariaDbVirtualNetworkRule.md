---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 7ae1159c3cd5f5feea3d836a421dd9fe08c78da8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127751"
---
# <span data-ttu-id="3d734-101">Get-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3d734-101">Get-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="3d734-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3d734-102">SYNOPSIS</span></span>
<span data-ttu-id="3d734-103">取得虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="3d734-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="3d734-104">句法</span><span class="sxs-lookup"><span data-stu-id="3d734-104">SYNTAX</span></span>

### <span data-ttu-id="3d734-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="3d734-105">List (Default)</span></span>
```
Get-AzMariaDbVirtualNetworkRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="3d734-106">獲取</span><span class="sxs-lookup"><span data-stu-id="3d734-106">Get</span></span>
```
Get-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="3d734-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3d734-107">GetViaIdentity</span></span>
```
Get-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="3d734-108">說明</span><span class="sxs-lookup"><span data-stu-id="3d734-108">DESCRIPTION</span></span>
<span data-ttu-id="3d734-109">取得虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="3d734-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="3d734-110">示例</span><span class="sxs-lookup"><span data-stu-id="3d734-110">EXAMPLES</span></span>

### <span data-ttu-id="3d734-111">範例1：列出 MariaDB 下的所有虛擬網路規則</span><span class="sxs-lookup"><span data-stu-id="3d734-111">Example 1: List all virtual network rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbVirtualNetworkRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
vnetrule-Adsefc Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="3d734-112">這個命令會列出 MariaDB 下的所有虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="3d734-112">This command lists all virtual network rule under a MariaDB.</span></span>

### <span data-ttu-id="3d734-113">範例2：在 MariaDB 下取得虛擬網路規則</span><span class="sxs-lookup"><span data-stu-id="3d734-113">Example 2: Get virtual network rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbVirtualNetworkRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn -Name vnetrule-QdMJpU

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="3d734-114">這個命令會在 MariaDB 下取得虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="3d734-114">This command gets virtual network rule under a MariaDB.</span></span>

## <span data-ttu-id="3d734-115">參數</span><span class="sxs-lookup"><span data-stu-id="3d734-115">PARAMETERS</span></span>

### <span data-ttu-id="3d734-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d734-116">-DefaultProfile</span></span>
<span data-ttu-id="3d734-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3d734-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d734-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d734-118">-InputObject</span></span>
<span data-ttu-id="3d734-119">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="3d734-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d734-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="3d734-120">-Name</span></span>
<span data-ttu-id="3d734-121">虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d734-121">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d734-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3d734-122">-PassThru</span></span>
<span data-ttu-id="3d734-123">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="3d734-123">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d734-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d734-124">-ResourceGroupName</span></span>
<span data-ttu-id="3d734-125">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d734-125">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="3d734-126">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="3d734-126">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="3d734-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3d734-127">-ServerName</span></span>
<span data-ttu-id="3d734-128">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d734-128">The name of the server.</span></span>

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

### <span data-ttu-id="3d734-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3d734-129">-SubscriptionId</span></span>
<span data-ttu-id="3d734-130">識別 Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="3d734-130">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="3d734-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d734-131">CommonParameters</span></span>
<span data-ttu-id="3d734-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3d734-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d734-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3d734-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d734-134">輸入</span><span class="sxs-lookup"><span data-stu-id="3d734-134">INPUTS</span></span>

### <span data-ttu-id="3d734-135">IMariaDbIdentity （MariaDb）的</span><span class="sxs-lookup"><span data-stu-id="3d734-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="3d734-136">輸出</span><span class="sxs-lookup"><span data-stu-id="3d734-136">OUTPUTS</span></span>

### <span data-ttu-id="3d734-137">IVirtualNetworkRule （MariaDb）。 Api20180601Preview。</span><span class="sxs-lookup"><span data-stu-id="3d734-137">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="3d734-138">筆記</span><span class="sxs-lookup"><span data-stu-id="3d734-138">NOTES</span></span>

<span data-ttu-id="3d734-139">別名</span><span class="sxs-lookup"><span data-stu-id="3d734-139">ALIASES</span></span>

<span data-ttu-id="3d734-140">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="3d734-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3d734-141">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="3d734-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3d734-142">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="3d734-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3d734-143">INPUTOBJECT <IMariaDbIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="3d734-143">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3d734-144">`[ConfigurationName <String>]`：伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d734-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="3d734-145">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d734-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="3d734-146">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d734-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="3d734-147">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="3d734-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3d734-148">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d734-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="3d734-149">`[ResourceGroupName <String>]`：包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d734-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="3d734-150">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="3d734-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="3d734-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全警示原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d734-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="3d734-152">`[ServerName <String>]`：伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d734-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="3d734-153">`[SubscriptionId <String>]`：識別 Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="3d734-153">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="3d734-154">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d734-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="3d734-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="3d734-155">RELATED LINKS</span></span>

