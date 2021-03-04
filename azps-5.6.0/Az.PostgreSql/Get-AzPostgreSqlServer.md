---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/get-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlServer.md
ms.openlocfilehash: 718443cc31972f1d1d53a5b5802dc50c1ac31df0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909502"
---
# <span data-ttu-id="42679-101">Get-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="42679-101">Get-AzPostgreSqlServer</span></span>

## <span data-ttu-id="42679-102">簡介</span><span class="sxs-lookup"><span data-stu-id="42679-102">SYNOPSIS</span></span>
<span data-ttu-id="42679-103">獲得伺服器相關資訊。</span><span class="sxs-lookup"><span data-stu-id="42679-103">Gets information about a server.</span></span>

## <span data-ttu-id="42679-104">語法</span><span class="sxs-lookup"><span data-stu-id="42679-104">SYNTAX</span></span>

### <span data-ttu-id="42679-105">清單1 (預設) </span><span class="sxs-lookup"><span data-stu-id="42679-105">List1 (Default)</span></span>
```
Get-AzPostgreSqlServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="42679-106">獲取</span><span class="sxs-lookup"><span data-stu-id="42679-106">Get</span></span>
```
Get-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="42679-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="42679-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="42679-108">清單</span><span class="sxs-lookup"><span data-stu-id="42679-108">List</span></span>
```
Get-AzPostgreSqlServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="42679-109">描述</span><span class="sxs-lookup"><span data-stu-id="42679-109">DESCRIPTION</span></span>
<span data-ttu-id="42679-110">獲得伺服器相關資訊。</span><span class="sxs-lookup"><span data-stu-id="42679-110">Gets information about a server.</span></span>

## <span data-ttu-id="42679-111">例子</span><span class="sxs-lookup"><span data-stu-id="42679-111">EXAMPLES</span></span>

### <span data-ttu-id="42679-112">範例 1：取得具有預設上下文的 PostgreSql 伺服器</span><span class="sxs-lookup"><span data-stu-id="42679-112">Example 1: Get PostgreSql server with default context</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver        eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="42679-113">此 Cmdlet 會獲得具有預設上下文的 PostgreSql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="42679-113">This cmdlet gets PostgreSql server with default context.</span></span>

### <span data-ttu-id="42679-114">範例 2：根據資源群組和伺服器名稱取得 PostgreSql 伺服器</span><span class="sxs-lookup"><span data-stu-id="42679-114">Example 2: Get PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -Name PostgreSqlTestServer

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="42679-115">此 Cmdlet 會按資源組和伺服器名稱獲得 PostgreSql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="42679-115">This cmdlet gets PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="42679-116">範例 3：列出指定資源群組中所有的 PostgreSql 伺服器</span><span class="sxs-lookup"><span data-stu-id="42679-116">Example 3: Lists all the PostgreSql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver        eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="42679-117">此 Cmdlet 會列出指定資源群組中所有的 PostgreSql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="42679-117">This cmdlet lists all the PostgreSql servers in specified resource group.</span></span>

### <span data-ttu-id="42679-118">範例 4：使用身分識別取得 PostgreSql 伺服器</span><span class="sxs-lookup"><span data-stu-id="42679-118">Example 4: Get PostgreSql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/postgresqltestserver"
PS C:\> Get-AzPostgreSqlServer -InputObject $ID

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="42679-119">此 Cmdlet 清單會以身分識別獲得 PostgreSql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="42679-119">This cmdlet lists gets PostgreSql server by identity.</span></span>

## <span data-ttu-id="42679-120">參數</span><span class="sxs-lookup"><span data-stu-id="42679-120">PARAMETERS</span></span>

### <span data-ttu-id="42679-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42679-121">-DefaultProfile</span></span>
<span data-ttu-id="42679-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="42679-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42679-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42679-123">-InputObject</span></span>
<span data-ttu-id="42679-124">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="42679-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42679-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="42679-125">-Name</span></span>
<span data-ttu-id="42679-126">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="42679-126">The name of the server.</span></span>

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

### <span data-ttu-id="42679-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42679-127">-ResourceGroupName</span></span>
<span data-ttu-id="42679-128">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="42679-128">The name of the resource group.</span></span>
<span data-ttu-id="42679-129">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="42679-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="42679-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="42679-130">-SubscriptionId</span></span>
<span data-ttu-id="42679-131">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="42679-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="42679-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42679-132">CommonParameters</span></span>
<span data-ttu-id="42679-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="42679-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42679-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="42679-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42679-135">輸入</span><span class="sxs-lookup"><span data-stu-id="42679-135">INPUTS</span></span>

### <span data-ttu-id="42679-136">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="42679-136">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="42679-137">輸出</span><span class="sxs-lookup"><span data-stu-id="42679-137">OUTPUTS</span></span>

### <span data-ttu-id="42679-138">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="42679-138">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="42679-139">筆記</span><span class="sxs-lookup"><span data-stu-id="42679-139">NOTES</span></span>

<span data-ttu-id="42679-140">別名</span><span class="sxs-lookup"><span data-stu-id="42679-140">ALIASES</span></span>

<span data-ttu-id="42679-141">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="42679-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="42679-142">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="42679-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="42679-143">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="42679-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="42679-144">INPUTOBJECT： <IPostgreSqlIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="42679-144">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="42679-145">`[ConfigurationName <String>]`：伺服器組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="42679-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="42679-146">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="42679-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="42679-147">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="42679-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="42679-148">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="42679-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="42679-149">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="42679-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="42679-150">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="42679-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="42679-151">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="42679-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="42679-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全性警示策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="42679-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="42679-153">`[ServerName <String>]`：伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="42679-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="42679-154">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="42679-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="42679-155">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="42679-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="42679-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="42679-156">RELATED LINKS</span></span>

