---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/get-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: dda229292436d07cf5383343cb85472b92881cdf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906582"
---
# <span data-ttu-id="df13e-101">Get-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="df13e-101">Get-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="df13e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="df13e-102">SYNOPSIS</span></span>
<span data-ttu-id="df13e-103">獲得虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="df13e-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="df13e-104">語法</span><span class="sxs-lookup"><span data-stu-id="df13e-104">SYNTAX</span></span>

### <span data-ttu-id="df13e-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="df13e-105">List (Default)</span></span>
```
Get-AzMariaDbVirtualNetworkRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="df13e-106">獲取</span><span class="sxs-lookup"><span data-stu-id="df13e-106">Get</span></span>
```
Get-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="df13e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="df13e-107">GetViaIdentity</span></span>
```
Get-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="df13e-108">描述</span><span class="sxs-lookup"><span data-stu-id="df13e-108">DESCRIPTION</span></span>
<span data-ttu-id="df13e-109">獲得虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="df13e-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="df13e-110">例子</span><span class="sxs-lookup"><span data-stu-id="df13e-110">EXAMPLES</span></span>

### <span data-ttu-id="df13e-111">範例 1：在 MariaDB 下列出所有虛擬網路規則</span><span class="sxs-lookup"><span data-stu-id="df13e-111">Example 1: List all virtual network rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbVirtualNetworkRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
vnetrule-Adsefc Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="df13e-112">此命令會列出 MariaDB 下的所有虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="df13e-112">This command lists all virtual network rule under a MariaDB.</span></span>

### <span data-ttu-id="df13e-113">範例 2：在 MariaDB 下取得虛擬網路規則</span><span class="sxs-lookup"><span data-stu-id="df13e-113">Example 2: Get virtual network rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbVirtualNetworkRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn -Name vnetrule-QdMJpU

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="df13e-114">此命令在 MariaDB 下會獲得虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="df13e-114">This command gets virtual network rule under a MariaDB.</span></span>

## <span data-ttu-id="df13e-115">參數</span><span class="sxs-lookup"><span data-stu-id="df13e-115">PARAMETERS</span></span>

### <span data-ttu-id="df13e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df13e-116">-DefaultProfile</span></span>
<span data-ttu-id="df13e-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="df13e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df13e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df13e-118">-InputObject</span></span>
<span data-ttu-id="df13e-119">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="df13e-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="df13e-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="df13e-120">-Name</span></span>
<span data-ttu-id="df13e-121">虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="df13e-121">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="df13e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="df13e-122">-PassThru</span></span>
<span data-ttu-id="df13e-123">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="df13e-123">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="df13e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df13e-124">-ResourceGroupName</span></span>
<span data-ttu-id="df13e-125">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="df13e-125">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="df13e-126">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="df13e-126">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="df13e-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="df13e-127">-ServerName</span></span>
<span data-ttu-id="df13e-128">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="df13e-128">The name of the server.</span></span>

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

### <span data-ttu-id="df13e-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="df13e-129">-SubscriptionId</span></span>
<span data-ttu-id="df13e-130">可識別 Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="df13e-130">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="df13e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df13e-131">CommonParameters</span></span>
<span data-ttu-id="df13e-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="df13e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df13e-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="df13e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df13e-134">輸入</span><span class="sxs-lookup"><span data-stu-id="df13e-134">INPUTS</span></span>

### <span data-ttu-id="df13e-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.models.IAzaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="df13e-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="df13e-136">輸出</span><span class="sxs-lookup"><span data-stu-id="df13e-136">OUTPUTS</span></span>

### <span data-ttu-id="df13e-137">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.models.Api20180601Preview.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="df13e-137">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="df13e-138">筆記</span><span class="sxs-lookup"><span data-stu-id="df13e-138">NOTES</span></span>

<span data-ttu-id="df13e-139">別名</span><span class="sxs-lookup"><span data-stu-id="df13e-139">ALIASES</span></span>

<span data-ttu-id="df13e-140">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="df13e-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="df13e-141">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="df13e-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="df13e-142">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="df13e-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="df13e-143">INPUTOBJECT： <IMariaDbIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="df13e-143">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="df13e-144">`[ConfigurationName <String>]`：伺服器組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="df13e-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="df13e-145">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="df13e-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="df13e-146">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="df13e-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="df13e-147">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="df13e-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="df13e-148">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="df13e-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="df13e-149">`[ResourceGroupName <String>]`：包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="df13e-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="df13e-150">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="df13e-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="df13e-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全性警示策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="df13e-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="df13e-152">`[ServerName <String>]`：伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="df13e-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="df13e-153">`[SubscriptionId <String>]`：識別 Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="df13e-153">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="df13e-154">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="df13e-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="df13e-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="df13e-155">RELATED LINKS</span></span>

