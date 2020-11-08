---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlServer.md
ms.openlocfilehash: 71fb10b0aeed85a716a834b42b1bdae3e5f7b270
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970226"
---
# <span data-ttu-id="2c8e0-101">Get-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="2c8e0-101">Get-AzPostgreSqlServer</span></span>

## <span data-ttu-id="2c8e0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2c8e0-102">SYNOPSIS</span></span>
<span data-ttu-id="2c8e0-103">取得伺服器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2c8e0-103">Gets information about a server.</span></span>

## <span data-ttu-id="2c8e0-104">句法</span><span class="sxs-lookup"><span data-stu-id="2c8e0-104">SYNTAX</span></span>

### <span data-ttu-id="2c8e0-105">List1 (預設) </span><span class="sxs-lookup"><span data-stu-id="2c8e0-105">List1 (Default)</span></span>
```
Get-AzPostgreSqlServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2c8e0-106">獲取</span><span class="sxs-lookup"><span data-stu-id="2c8e0-106">Get</span></span>
```
Get-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2c8e0-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2c8e0-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2c8e0-108">清單</span><span class="sxs-lookup"><span data-stu-id="2c8e0-108">List</span></span>
```
Get-AzPostgreSqlServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="2c8e0-109">說明</span><span class="sxs-lookup"><span data-stu-id="2c8e0-109">DESCRIPTION</span></span>
<span data-ttu-id="2c8e0-110">取得伺服器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2c8e0-110">Gets information about a server.</span></span>

## <span data-ttu-id="2c8e0-111">示例</span><span class="sxs-lookup"><span data-stu-id="2c8e0-111">EXAMPLES</span></span>

### <span data-ttu-id="2c8e0-112">範例1：使用預設內容取得 PostgreSql 伺服器</span><span class="sxs-lookup"><span data-stu-id="2c8e0-112">Example 1: Get PostgreSql server with default context</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver        eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="2c8e0-113">這個 Cmdlet 會取得預設內容的 PostgreSql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="2c8e0-113">This cmdlet gets PostgreSql server with default context.</span></span>

### <span data-ttu-id="2c8e0-114">範例2：依資源群組和伺服器名稱取得 PostgreSql 伺服器</span><span class="sxs-lookup"><span data-stu-id="2c8e0-114">Example 2: Get PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -Name PostgreSqlTestServer

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="2c8e0-115">這個 Cmdlet 會透過資源群組和伺服器名稱來取得 PostgreSql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="2c8e0-115">This cmdlet gets PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="2c8e0-116">範例3：列出指定資源群組中的所有 PostgreSql 伺服器</span><span class="sxs-lookup"><span data-stu-id="2c8e0-116">Example 3: Lists all the PostgreSql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver        eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="2c8e0-117">這個 Cmdlet 會列出指定資源群組中的所有 PostgreSql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="2c8e0-117">This cmdlet lists all the PostgreSql servers in specified resource group.</span></span>

### <span data-ttu-id="2c8e0-118">範例4：依身分識別取得 PostgreSql 伺服器</span><span class="sxs-lookup"><span data-stu-id="2c8e0-118">Example 4: Get PostgreSql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/postgresqltestserver"
PS C:\> Get-AzPostgreSqlServer -InputObject $ID

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="2c8e0-119">這個 Cmdlet 清單會透過身分識別來取得 PostgreSql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="2c8e0-119">This cmdlet lists gets PostgreSql server by identity.</span></span>

## <span data-ttu-id="2c8e0-120">參數</span><span class="sxs-lookup"><span data-stu-id="2c8e0-120">PARAMETERS</span></span>

### <span data-ttu-id="2c8e0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c8e0-121">-DefaultProfile</span></span>
<span data-ttu-id="2c8e0-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2c8e0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c8e0-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c8e0-123">-InputObject</span></span>
<span data-ttu-id="2c8e0-124">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="2c8e0-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2c8e0-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="2c8e0-125">-Name</span></span>
<span data-ttu-id="2c8e0-126">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="2c8e0-126">The name of the server.</span></span>

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

### <span data-ttu-id="2c8e0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c8e0-127">-ResourceGroupName</span></span>
<span data-ttu-id="2c8e0-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2c8e0-128">The name of the resource group.</span></span>
<span data-ttu-id="2c8e0-129">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="2c8e0-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="2c8e0-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2c8e0-130">-SubscriptionId</span></span>
<span data-ttu-id="2c8e0-131">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="2c8e0-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="2c8e0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c8e0-132">CommonParameters</span></span>
<span data-ttu-id="2c8e0-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2c8e0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c8e0-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2c8e0-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c8e0-135">輸入</span><span class="sxs-lookup"><span data-stu-id="2c8e0-135">INPUTS</span></span>

### <span data-ttu-id="2c8e0-136">IPostgreSqlIdentity （PostgreSql）的</span><span class="sxs-lookup"><span data-stu-id="2c8e0-136">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="2c8e0-137">輸出</span><span class="sxs-lookup"><span data-stu-id="2c8e0-137">OUTPUTS</span></span>

### <span data-ttu-id="2c8e0-138">IServer （PostgreSql）。 Api20171201。</span><span class="sxs-lookup"><span data-stu-id="2c8e0-138">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="2c8e0-139">筆記</span><span class="sxs-lookup"><span data-stu-id="2c8e0-139">NOTES</span></span>

<span data-ttu-id="2c8e0-140">別名</span><span class="sxs-lookup"><span data-stu-id="2c8e0-140">ALIASES</span></span>

<span data-ttu-id="2c8e0-141">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="2c8e0-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2c8e0-142">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="2c8e0-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2c8e0-143">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="2c8e0-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2c8e0-144">INPUTOBJECT <IPostgreSqlIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="2c8e0-144">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2c8e0-145">`[ConfigurationName <String>]`：伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="2c8e0-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="2c8e0-146">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="2c8e0-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="2c8e0-147">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="2c8e0-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="2c8e0-148">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="2c8e0-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2c8e0-149">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="2c8e0-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="2c8e0-150">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2c8e0-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="2c8e0-151">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="2c8e0-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="2c8e0-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全警示原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="2c8e0-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="2c8e0-153">`[ServerName <String>]`：伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="2c8e0-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="2c8e0-154">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="2c8e0-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="2c8e0-155">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="2c8e0-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="2c8e0-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="2c8e0-156">RELATED LINKS</span></span>

