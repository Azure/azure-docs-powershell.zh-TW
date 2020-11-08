---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbServer.md
ms.openlocfilehash: 43af6a438a36df5360fd062aaf22e85e95fa62a1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94135897"
---
# <span data-ttu-id="a0ec9-101">Get-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="a0ec9-101">Get-AzMariaDbServer</span></span>

## <span data-ttu-id="a0ec9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a0ec9-102">SYNOPSIS</span></span>
<span data-ttu-id="a0ec9-103">取得伺服器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a0ec9-103">Gets information about a server.</span></span>

## <span data-ttu-id="a0ec9-104">句法</span><span class="sxs-lookup"><span data-stu-id="a0ec9-104">SYNTAX</span></span>

### <span data-ttu-id="a0ec9-105">List1 (預設) </span><span class="sxs-lookup"><span data-stu-id="a0ec9-105">List1 (Default)</span></span>
```
Get-AzMariaDbServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a0ec9-106">獲取</span><span class="sxs-lookup"><span data-stu-id="a0ec9-106">Get</span></span>
```
Get-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a0ec9-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a0ec9-107">GetViaIdentity</span></span>
```
Get-AzMariaDbServer -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a0ec9-108">清單</span><span class="sxs-lookup"><span data-stu-id="a0ec9-108">List</span></span>
```
Get-AzMariaDbServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="a0ec9-109">說明</span><span class="sxs-lookup"><span data-stu-id="a0ec9-109">DESCRIPTION</span></span>
<span data-ttu-id="a0ec9-110">取得伺服器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a0ec9-110">Gets information about a server.</span></span>

## <span data-ttu-id="a0ec9-111">示例</span><span class="sxs-lookup"><span data-stu-id="a0ec9-111">EXAMPLES</span></span>

### <span data-ttu-id="a0ec9-112">範例1：列出訂閱下的所有 MariaDB</span><span class="sxs-lookup"><span data-stu-id="a0ec9-112">Example 1: List all MariaDB under a subscriptions</span></span>
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

<span data-ttu-id="a0ec9-113">這個命令會列出訂閱下的所有 MariaDB。</span><span class="sxs-lookup"><span data-stu-id="a0ec9-113">This command lists all MariaDB under a subscriptions.</span></span>

### <span data-ttu-id="a0ec9-114">範例2：列出資源群組下的所有 MariaDB</span><span class="sxs-lookup"><span data-stu-id="a0ec9-114">Example 2: List all MariaDB under a resource group</span></span>
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

<span data-ttu-id="a0ec9-115">這個命令會列出 [資源] 群組底下的所有 MariaDB。</span><span class="sxs-lookup"><span data-stu-id="a0ec9-115">This command lists all MariaDB under a resource group.</span></span>

### <span data-ttu-id="a0ec9-116">範例3：取得 MariaDB</span><span class="sxs-lookup"><span data-stu-id="a0ec9-116">Example 3: Get a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -ResourceGroupName mariadb-test-qu5ov0 -Name mariadb-test-h3pame

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-h3pame eastus   qiszomtkpf         10.2    5120                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="a0ec9-117">這個命令會取得 MariaDB。</span><span class="sxs-lookup"><span data-stu-id="a0ec9-117">This command gets a MariaDB.</span></span>

## <span data-ttu-id="a0ec9-118">參數</span><span class="sxs-lookup"><span data-stu-id="a0ec9-118">PARAMETERS</span></span>

### <span data-ttu-id="a0ec9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0ec9-119">-DefaultProfile</span></span>
<span data-ttu-id="a0ec9-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a0ec9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0ec9-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a0ec9-121">-InputObject</span></span>
<span data-ttu-id="a0ec9-122">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="a0ec9-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a0ec9-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="a0ec9-123">-Name</span></span>
<span data-ttu-id="a0ec9-124">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="a0ec9-124">The name of the server.</span></span>

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

### <span data-ttu-id="a0ec9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0ec9-125">-ResourceGroupName</span></span>
<span data-ttu-id="a0ec9-126">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a0ec9-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="a0ec9-127">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="a0ec9-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="a0ec9-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a0ec9-128">-SubscriptionId</span></span>
<span data-ttu-id="a0ec9-129">識別 Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="a0ec9-129">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="a0ec9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0ec9-130">CommonParameters</span></span>
<span data-ttu-id="a0ec9-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a0ec9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0ec9-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a0ec9-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0ec9-133">輸入</span><span class="sxs-lookup"><span data-stu-id="a0ec9-133">INPUTS</span></span>

### <span data-ttu-id="a0ec9-134">IMariaDbIdentity （MariaDb）的</span><span class="sxs-lookup"><span data-stu-id="a0ec9-134">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="a0ec9-135">輸出</span><span class="sxs-lookup"><span data-stu-id="a0ec9-135">OUTPUTS</span></span>

### <span data-ttu-id="a0ec9-136">IServer （MariaDb）。 Api20180601Preview。</span><span class="sxs-lookup"><span data-stu-id="a0ec9-136">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="a0ec9-137">筆記</span><span class="sxs-lookup"><span data-stu-id="a0ec9-137">NOTES</span></span>

<span data-ttu-id="a0ec9-138">別名</span><span class="sxs-lookup"><span data-stu-id="a0ec9-138">ALIASES</span></span>

<span data-ttu-id="a0ec9-139">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="a0ec9-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a0ec9-140">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="a0ec9-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a0ec9-141">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="a0ec9-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a0ec9-142">INPUTOBJECT <IMariaDbIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="a0ec9-142">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a0ec9-143">`[ConfigurationName <String>]`：伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="a0ec9-143">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="a0ec9-144">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="a0ec9-144">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="a0ec9-145">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="a0ec9-145">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="a0ec9-146">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="a0ec9-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a0ec9-147">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="a0ec9-147">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="a0ec9-148">`[ResourceGroupName <String>]`：包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a0ec9-148">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="a0ec9-149">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="a0ec9-149">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="a0ec9-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全警示原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="a0ec9-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="a0ec9-151">`[ServerName <String>]`：伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="a0ec9-151">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="a0ec9-152">`[SubscriptionId <String>]`：識別 Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="a0ec9-152">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="a0ec9-153">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="a0ec9-153">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="a0ec9-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="a0ec9-154">RELATED LINKS</span></span>

