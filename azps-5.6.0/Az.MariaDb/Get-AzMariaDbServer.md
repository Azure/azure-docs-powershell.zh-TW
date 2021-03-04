---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/get-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbServer.md
ms.openlocfilehash: ac7ea6689b18c14cca2213e3856cb093f5f36287
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906585"
---
# <span data-ttu-id="ba2e1-101">Get-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="ba2e1-101">Get-AzMariaDbServer</span></span>

## <span data-ttu-id="ba2e1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ba2e1-102">SYNOPSIS</span></span>
<span data-ttu-id="ba2e1-103">獲得伺服器相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ba2e1-103">Gets information about a server.</span></span>

## <span data-ttu-id="ba2e1-104">語法</span><span class="sxs-lookup"><span data-stu-id="ba2e1-104">SYNTAX</span></span>

### <span data-ttu-id="ba2e1-105">清單1 (預設) </span><span class="sxs-lookup"><span data-stu-id="ba2e1-105">List1 (Default)</span></span>
```
Get-AzMariaDbServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ba2e1-106">獲取</span><span class="sxs-lookup"><span data-stu-id="ba2e1-106">Get</span></span>
```
Get-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ba2e1-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ba2e1-107">GetViaIdentity</span></span>
```
Get-AzMariaDbServer -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ba2e1-108">清單</span><span class="sxs-lookup"><span data-stu-id="ba2e1-108">List</span></span>
```
Get-AzMariaDbServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="ba2e1-109">描述</span><span class="sxs-lookup"><span data-stu-id="ba2e1-109">DESCRIPTION</span></span>
<span data-ttu-id="ba2e1-110">獲得伺服器相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ba2e1-110">Gets information about a server.</span></span>

## <span data-ttu-id="ba2e1-111">例子</span><span class="sxs-lookup"><span data-stu-id="ba2e1-111">EXAMPLES</span></span>

### <span data-ttu-id="ba2e1-112">範例 1：在訂閱下列出所有 MariaDB</span><span class="sxs-lookup"><span data-stu-id="ba2e1-112">Example 1: List all MariaDB under a subscriptions</span></span>
```powershell
PS C:\> Get-AzMariaDbServer

Name                       Location AdministratorLogin Version StorageProfileStorageMb SkuName    SkuTier        SslEnforcement
----                       -------- ------------------ ------- ----------------------- -------    -------        --------------
mrdb01                     eastus   dolauli            10.2    5120                    B_Gen5_1   Basic          Enabled
wyunchi-10                 eastus   wyunchi            10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
wyunchi                    eastus   wyunchi            10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
wyunchi-eastus             eastus   wyunchi            10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-h3pame        eastus   qiszomtkpf         10.2    5120                    B_Gen5_1   Basic          Enabled
mariadb-test-4rmtig        eastus   xofavpndqj         10.2    5120                    B_Gen5_1   Basic          Enabled
mariadb-test-szp6dt        eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-9pebvn        eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-szp6dt-rep428 eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-asd-01             eastus   adminuser          10.2    5120                    B_Gen5_1   Basic          Enabled
rst-001                    eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rst-002                    eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rstrgp02-rep-003           eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rstrgp02-rep-004           eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
```

<span data-ttu-id="ba2e1-113">此命令會列出訂閱下的所有 MariaDB。</span><span class="sxs-lookup"><span data-stu-id="ba2e1-113">This command lists all MariaDB under a subscriptions.</span></span>

### <span data-ttu-id="ba2e1-114">範例 2：在資源群組下列出所有 MariaDB</span><span class="sxs-lookup"><span data-stu-id="ba2e1-114">Example 2: List all MariaDB under a resource group</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -ResourceGroupName mariadb-test-qu5ov0

Name                       Location AdministratorLogin Version StorageProfileStorageMb SkuName    SkuTier        SslEnforcement
----                       -------- ------------------ ------- ----------------------- -------    -------        --------------
mariadb-test-h3pame        eastus   qiszomtkpf         10.2    5120                    B_Gen5_1   Basic          Enabled
mariadb-test-4rmtig        eastus   xofavpndqj         10.2    5120                    B_Gen5_1   Basic          Enabled
mariadb-test-szp6dt        eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-9pebvn        eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-szp6dt-rep428 eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-asd-01             eastus   adminuser          10.2    5120                    B_Gen5_1   Basic          Enabled
rst-001                    eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rst-002                    eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rstrgp02-rep-003           eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rstrgp02-rep-004           eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
```

<span data-ttu-id="ba2e1-115">此命令會列出資源群組下的所有 MariaDB。</span><span class="sxs-lookup"><span data-stu-id="ba2e1-115">This command lists all MariaDB under a resource group.</span></span>

### <span data-ttu-id="ba2e1-116">範例 3：取得 MariaDB</span><span class="sxs-lookup"><span data-stu-id="ba2e1-116">Example 3: Get a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -ResourceGroupName mariadb-test-qu5ov0 -Name mariadb-test-h3pame

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-h3pame eastus   qiszomtkpf         10.2    5120                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="ba2e1-117">此命令會獲得 MariaDB。</span><span class="sxs-lookup"><span data-stu-id="ba2e1-117">This command gets a MariaDB.</span></span>

## <span data-ttu-id="ba2e1-118">參數</span><span class="sxs-lookup"><span data-stu-id="ba2e1-118">PARAMETERS</span></span>

### <span data-ttu-id="ba2e1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba2e1-119">-DefaultProfile</span></span>
<span data-ttu-id="ba2e1-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ba2e1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba2e1-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba2e1-121">-InputObject</span></span>
<span data-ttu-id="ba2e1-122">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="ba2e1-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ba2e1-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="ba2e1-123">-Name</span></span>
<span data-ttu-id="ba2e1-124">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="ba2e1-124">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba2e1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba2e1-125">-ResourceGroupName</span></span>
<span data-ttu-id="ba2e1-126">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="ba2e1-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="ba2e1-127">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="ba2e1-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="ba2e1-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ba2e1-128">-SubscriptionId</span></span>
<span data-ttu-id="ba2e1-129">可識別 Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="ba2e1-129">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="ba2e1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba2e1-130">CommonParameters</span></span>
<span data-ttu-id="ba2e1-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ba2e1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba2e1-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ba2e1-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba2e1-133">輸入</span><span class="sxs-lookup"><span data-stu-id="ba2e1-133">INPUTS</span></span>

### <span data-ttu-id="ba2e1-134">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.models.IAzaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="ba2e1-134">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="ba2e1-135">輸出</span><span class="sxs-lookup"><span data-stu-id="ba2e1-135">OUTPUTS</span></span>

### <span data-ttu-id="ba2e1-136">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="ba2e1-136">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="ba2e1-137">筆記</span><span class="sxs-lookup"><span data-stu-id="ba2e1-137">NOTES</span></span>

<span data-ttu-id="ba2e1-138">別名</span><span class="sxs-lookup"><span data-stu-id="ba2e1-138">ALIASES</span></span>

<span data-ttu-id="ba2e1-139">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="ba2e1-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ba2e1-140">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="ba2e1-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ba2e1-141">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="ba2e1-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ba2e1-142">INPUTOBJECT： <IMariaDbIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="ba2e1-142">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ba2e1-143">`[ConfigurationName <String>]`：伺服器組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ba2e1-143">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="ba2e1-144">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="ba2e1-144">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="ba2e1-145">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="ba2e1-145">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="ba2e1-146">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="ba2e1-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ba2e1-147">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="ba2e1-147">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="ba2e1-148">`[ResourceGroupName <String>]`：包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="ba2e1-148">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="ba2e1-149">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="ba2e1-149">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="ba2e1-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全性警示策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="ba2e1-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="ba2e1-151">`[ServerName <String>]`：伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="ba2e1-151">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="ba2e1-152">`[SubscriptionId <String>]`：識別 Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="ba2e1-152">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="ba2e1-153">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="ba2e1-153">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="ba2e1-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="ba2e1-154">RELATED LINKS</span></span>

