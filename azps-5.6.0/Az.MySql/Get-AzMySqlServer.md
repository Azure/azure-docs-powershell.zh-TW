---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlServer.md
ms.openlocfilehash: 7a9ef90da8861da8ae530d3a05dae4bbacd62898
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902001"
---
# <span data-ttu-id="f93f9-101">Get-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="f93f9-101">Get-AzMySqlServer</span></span>

## <span data-ttu-id="f93f9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f93f9-102">SYNOPSIS</span></span>
<span data-ttu-id="f93f9-103">獲得伺服器相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f93f9-103">Gets information about a server.</span></span>

## <span data-ttu-id="f93f9-104">語法</span><span class="sxs-lookup"><span data-stu-id="f93f9-104">SYNTAX</span></span>

### <span data-ttu-id="f93f9-105">清單1 (預設) </span><span class="sxs-lookup"><span data-stu-id="f93f9-105">List1 (Default)</span></span>
```
Get-AzMySqlServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f93f9-106">獲取</span><span class="sxs-lookup"><span data-stu-id="f93f9-106">Get</span></span>
```
Get-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f93f9-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f93f9-107">GetViaIdentity</span></span>
```
Get-AzMySqlServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f93f9-108">清單</span><span class="sxs-lookup"><span data-stu-id="f93f9-108">List</span></span>
```
Get-AzMySqlServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="f93f9-109">描述</span><span class="sxs-lookup"><span data-stu-id="f93f9-109">DESCRIPTION</span></span>
<span data-ttu-id="f93f9-110">獲得伺服器相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f93f9-110">Gets information about a server.</span></span>

## <span data-ttu-id="f93f9-111">例子</span><span class="sxs-lookup"><span data-stu-id="f93f9-111">EXAMPLES</span></span>

### <span data-ttu-id="f93f9-112">範例 1：取得具有預設上下文的 MySql 伺服器</span><span class="sxs-lookup"><span data-stu-id="f93f9-112">Example 1: Get MySql server with default context</span></span>
```powershell
PS C:\> Get-AzMySqlServer

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-11 eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="f93f9-113">此 Cmdlet 會獲得具有預設上下文的 MySql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="f93f9-113">This cmdlet gets MySql server with default context.</span></span>

### <span data-ttu-id="f93f9-114">範例 2：根據資源群組和伺服器名稱取得 MySql 伺服器</span><span class="sxs-lookup"><span data-stu-id="f93f9-114">Example 2: Get MySql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -Name mysql-test

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="f93f9-115">此 Cmdlet 會根據資源群組和伺服器名稱來獲得 MySql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="f93f9-115">This cmdlet gets MySql server by resource group and server name.</span></span>

### <span data-ttu-id="f93f9-116">範例 3：列出指定資源群組中所有的 MySql 伺服器</span><span class="sxs-lookup"><span data-stu-id="f93f9-116">Example 3: Lists all the MySql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="f93f9-117">此 Cmdlet 會列出指定資源群組中所有的 MySql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="f93f9-117">This cmdlet lists all the MySql servers in specified resource group.</span></span>

### <span data-ttu-id="f93f9-118">範例 4：使用身分識別取得 MySql 伺服器</span><span class="sxs-lookup"><span data-stu-id="f93f9-118">Example 4: Get MySql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test"
PS C:\> Get-AzMySqlServer -InputObject $ID

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="f93f9-119">此 Cmdlet 清單會以身分識別獲得 MySql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="f93f9-119">This cmdlet lists gets MySql server by identity.</span></span>

## <span data-ttu-id="f93f9-120">參數</span><span class="sxs-lookup"><span data-stu-id="f93f9-120">PARAMETERS</span></span>

### <span data-ttu-id="f93f9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f93f9-121">-DefaultProfile</span></span>
<span data-ttu-id="f93f9-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f93f9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f93f9-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f93f9-123">-InputObject</span></span>
<span data-ttu-id="f93f9-124">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="f93f9-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f93f9-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="f93f9-125">-Name</span></span>
<span data-ttu-id="f93f9-126">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="f93f9-126">The name of the server.</span></span>

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

### <span data-ttu-id="f93f9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f93f9-127">-ResourceGroupName</span></span>
<span data-ttu-id="f93f9-128">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f93f9-128">The name of the resource group.</span></span>
<span data-ttu-id="f93f9-129">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="f93f9-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f93f9-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f93f9-130">-SubscriptionId</span></span>
<span data-ttu-id="f93f9-131">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f93f9-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f93f9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f93f9-132">CommonParameters</span></span>
<span data-ttu-id="f93f9-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f93f9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f93f9-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f93f9-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f93f9-135">輸入</span><span class="sxs-lookup"><span data-stu-id="f93f9-135">INPUTS</span></span>

### <span data-ttu-id="f93f9-136">Microsoft.Azure.PowerShell.Cmdlets.MySql.models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="f93f9-136">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="f93f9-137">輸出</span><span class="sxs-lookup"><span data-stu-id="f93f9-137">OUTPUTS</span></span>

### <span data-ttu-id="f93f9-138">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="f93f9-138">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="f93f9-139">筆記</span><span class="sxs-lookup"><span data-stu-id="f93f9-139">NOTES</span></span>

<span data-ttu-id="f93f9-140">別名</span><span class="sxs-lookup"><span data-stu-id="f93f9-140">ALIASES</span></span>

<span data-ttu-id="f93f9-141">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="f93f9-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f93f9-142">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="f93f9-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f93f9-143">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="f93f9-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f93f9-144">INPUTOBJECT： <IMySqlIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="f93f9-144">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f93f9-145">`[ConfigurationName <String>]`：伺服器組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f93f9-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="f93f9-146">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="f93f9-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="f93f9-147">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="f93f9-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="f93f9-148">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="f93f9-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f93f9-149">`[KeyName <String>]`：伺服器金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="f93f9-149">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="f93f9-150">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="f93f9-150">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="f93f9-151">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f93f9-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f93f9-152">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="f93f9-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="f93f9-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全性警示策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="f93f9-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="f93f9-154">`[ServerName <String>]`：伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="f93f9-154">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="f93f9-155">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f93f9-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="f93f9-156">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="f93f9-156">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="f93f9-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="f93f9-157">RELATED LINKS</span></span>

