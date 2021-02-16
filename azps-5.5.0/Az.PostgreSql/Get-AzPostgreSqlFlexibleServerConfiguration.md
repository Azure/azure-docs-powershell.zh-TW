---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerConfiguration.md
ms.openlocfilehash: 0f65a007a37df559802a134ec5d6d8fc6fb33d01
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100128595"
---
# <span data-ttu-id="2f526-101">Get-AzPostgreSqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="2f526-101">Get-AzPostgreSqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="2f526-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2f526-102">SYNOPSIS</span></span>
<span data-ttu-id="2f526-103">取得伺服器設定的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2f526-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="2f526-104">句法</span><span class="sxs-lookup"><span data-stu-id="2f526-104">SYNTAX</span></span>

### <span data-ttu-id="2f526-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="2f526-105">List (Default)</span></span>
```
Get-AzPostgreSqlFlexibleServerConfiguration -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2f526-106">獲取</span><span class="sxs-lookup"><span data-stu-id="2f526-106">Get</span></span>
```
Get-AzPostgreSqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2f526-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2f526-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlFlexibleServerConfiguration -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="2f526-108">說明</span><span class="sxs-lookup"><span data-stu-id="2f526-108">DESCRIPTION</span></span>
<span data-ttu-id="2f526-109">取得伺服器設定的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2f526-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="2f526-110">示例</span><span class="sxs-lookup"><span data-stu-id="2f526-110">EXAMPLES</span></span>

### <span data-ttu-id="2f526-111">範例1：依名稱取得指定的 PostgreSql 設定</span><span class="sxs-lookup"><span data-stu-id="2f526-111">Example 1: Get specified PostgreSql configuration by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerConfiguration -Name work_mem -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
work_mem        4096  4096         system-default 4096-2097151   Integer
```

<span data-ttu-id="2f526-112">這個 Cmdlet 透過名稱取得指定的 PostgreSql 配置。</span><span class="sxs-lookup"><span data-stu-id="2f526-112">This cmdlet gets specified PostgreSql configuration by name.</span></span>

### <span data-ttu-id="2f526-113">範例2：列出指定 PostgreSql 伺服器中的所有配置</span><span class="sxs-lookup"><span data-stu-id="2f526-113">Example 2: List all configurations in specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerConfiguration -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
application_name  ""    ""           system-default [A-Za-z0-9._-]*      String
...
pgbouncer.enabled   false  false         system-default true, false   Boolean
```

<span data-ttu-id="2f526-114">這個 Cmdlet 會列出指定 PostgreSql 伺服器中的所有設定。</span><span class="sxs-lookup"><span data-stu-id="2f526-114">This cmdlet lists all configurations in specified PostgreSql server.</span></span>

## <span data-ttu-id="2f526-115">參數</span><span class="sxs-lookup"><span data-stu-id="2f526-115">PARAMETERS</span></span>

### <span data-ttu-id="2f526-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f526-116">-DefaultProfile</span></span>
<span data-ttu-id="2f526-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2f526-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f526-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f526-118">-InputObject</span></span>
<span data-ttu-id="2f526-119">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="2f526-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2f526-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="2f526-120">-Name</span></span>
<span data-ttu-id="2f526-121">伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f526-121">The name of the server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f526-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f526-122">-ResourceGroupName</span></span>
<span data-ttu-id="2f526-123">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f526-123">The name of the resource group.</span></span>
<span data-ttu-id="2f526-124">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="2f526-124">The name is case insensitive.</span></span>

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

### <span data-ttu-id="2f526-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2f526-125">-ServerName</span></span>
<span data-ttu-id="2f526-126">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f526-126">The name of the server.</span></span>

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

### <span data-ttu-id="2f526-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2f526-127">-SubscriptionId</span></span>
<span data-ttu-id="2f526-128">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="2f526-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="2f526-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f526-129">CommonParameters</span></span>
<span data-ttu-id="2f526-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2f526-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f526-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2f526-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f526-132">輸入</span><span class="sxs-lookup"><span data-stu-id="2f526-132">INPUTS</span></span>

### <span data-ttu-id="2f526-133">IPostgreSqlIdentity （PostgreSql）的</span><span class="sxs-lookup"><span data-stu-id="2f526-133">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="2f526-134">輸出</span><span class="sxs-lookup"><span data-stu-id="2f526-134">OUTPUTS</span></span>

### <span data-ttu-id="2f526-135">IConfigurationAutoGenerated （PostgreSql）。 Api20200214Preview。</span><span class="sxs-lookup"><span data-stu-id="2f526-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="2f526-136">筆記</span><span class="sxs-lookup"><span data-stu-id="2f526-136">NOTES</span></span>

<span data-ttu-id="2f526-137">別名</span><span class="sxs-lookup"><span data-stu-id="2f526-137">ALIASES</span></span>

<span data-ttu-id="2f526-138">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="2f526-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2f526-139">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="2f526-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2f526-140">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="2f526-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2f526-141">INPUTOBJECT <IPostgreSqlIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="2f526-141">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2f526-142">`[ConfigurationName <String>]`：伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f526-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="2f526-143">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f526-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="2f526-144">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f526-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="2f526-145">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="2f526-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2f526-146">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f526-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="2f526-147">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f526-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="2f526-148">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="2f526-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="2f526-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全警示原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f526-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="2f526-150">`[ServerName <String>]`：伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f526-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="2f526-151">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="2f526-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="2f526-152">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f526-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="2f526-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="2f526-153">RELATED LINKS</span></span>

