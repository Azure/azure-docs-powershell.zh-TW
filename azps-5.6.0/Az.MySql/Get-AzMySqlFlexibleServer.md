---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServer.md
ms.openlocfilehash: cbbe321f23fb95bca8a4a70dd59f30ec098cf2d0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916927"
---
# <span data-ttu-id="e54ec-101">Get-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="e54ec-101">Get-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="e54ec-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e54ec-102">SYNOPSIS</span></span>
<span data-ttu-id="e54ec-103">獲得伺服器相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e54ec-103">Gets information about a server.</span></span>

## <span data-ttu-id="e54ec-104">語法</span><span class="sxs-lookup"><span data-stu-id="e54ec-104">SYNTAX</span></span>

### <span data-ttu-id="e54ec-105">清單1 (預設) </span><span class="sxs-lookup"><span data-stu-id="e54ec-105">List1 (Default)</span></span>
```
Get-AzMySqlFlexibleServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e54ec-106">獲取</span><span class="sxs-lookup"><span data-stu-id="e54ec-106">Get</span></span>
```
Get-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e54ec-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e54ec-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e54ec-108">清單</span><span class="sxs-lookup"><span data-stu-id="e54ec-108">List</span></span>
```
Get-AzMySqlFlexibleServer -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e54ec-109">描述</span><span class="sxs-lookup"><span data-stu-id="e54ec-109">DESCRIPTION</span></span>
<span data-ttu-id="e54ec-110">獲得伺服器相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e54ec-110">Gets information about a server.</span></span>

## <span data-ttu-id="e54ec-111">例子</span><span class="sxs-lookup"><span data-stu-id="e54ec-111">EXAMPLES</span></span>

### <span data-ttu-id="e54ec-112">範例 1：取得具有預設上下文的 MySql 伺服器</span><span class="sxs-lookup"><span data-stu-id="e54ec-112">Example 1: Get MySql server with default context</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test-11  westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="e54ec-113">此 Cmdlet 會獲得具有預設上下文的 MySql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="e54ec-113">This cmdlet gets MySql servers with default context.</span></span>

### <span data-ttu-id="e54ec-114">範例 2：根據資源群組和伺服器名稱取得 MySql 伺服器</span><span class="sxs-lookup"><span data-stu-id="e54ec-114">Example 2: Get MySql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Name mysql-test

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test     westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="e54ec-115">此 Cmdlet 會根據資源群組和伺服器名稱來獲得 MySql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="e54ec-115">This cmdlet gets MySql servers by resource group and server name.</span></span>

### <span data-ttu-id="e54ec-116">範例 3：列出指定資源群組中所有的 MySql 伺服器</span><span class="sxs-lookup"><span data-stu-id="e54ec-116">Example 3: Lists all the MySql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test-11 westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
mysql-test-12 westus2   mysql_test2        5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="e54ec-117">此 Cmdlet 會列出指定資源群組中所有的 MySql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="e54ec-117">This cmdlet lists all the MySql servers in the specified resource group.</span></span>

### <span data-ttu-id="e54ec-118">範例 4：使用身分識別取得 MySql 伺服器</span><span class="sxs-lookup"><span data-stu-id="e54ec-118">Example 4: Get MySql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test"
PS C:\> Get-AzMySqlFlexibleServer -InputObject $ID

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test    westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="e54ec-119">此 Cmdlet 清單會以身分識別獲得 MySql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="e54ec-119">This cmdlet lists gets MySql servers by identity.</span></span>

## <span data-ttu-id="e54ec-120">參數</span><span class="sxs-lookup"><span data-stu-id="e54ec-120">PARAMETERS</span></span>

### <span data-ttu-id="e54ec-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e54ec-121">-DefaultProfile</span></span>
<span data-ttu-id="e54ec-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e54ec-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e54ec-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e54ec-123">-InputObject</span></span>
<span data-ttu-id="e54ec-124">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="e54ec-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e54ec-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="e54ec-125">-Name</span></span>
<span data-ttu-id="e54ec-126">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="e54ec-126">The name of the server.</span></span>

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

### <span data-ttu-id="e54ec-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e54ec-127">-ResourceGroupName</span></span>
<span data-ttu-id="e54ec-128">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e54ec-128">The name of the resource group.</span></span>
<span data-ttu-id="e54ec-129">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="e54ec-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e54ec-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e54ec-130">-SubscriptionId</span></span>
<span data-ttu-id="e54ec-131">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e54ec-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e54ec-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e54ec-132">CommonParameters</span></span>
<span data-ttu-id="e54ec-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e54ec-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e54ec-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e54ec-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e54ec-135">輸入</span><span class="sxs-lookup"><span data-stu-id="e54ec-135">INPUTS</span></span>

### <span data-ttu-id="e54ec-136">Microsoft.Azure.PowerShell.Cmdlets.MySql.models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="e54ec-136">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="e54ec-137">輸出</span><span class="sxs-lookup"><span data-stu-id="e54ec-137">OUTPUTS</span></span>

### <span data-ttu-id="e54ec-138">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="e54ec-138">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="e54ec-139">筆記</span><span class="sxs-lookup"><span data-stu-id="e54ec-139">NOTES</span></span>

<span data-ttu-id="e54ec-140">別名</span><span class="sxs-lookup"><span data-stu-id="e54ec-140">ALIASES</span></span>

<span data-ttu-id="e54ec-141">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="e54ec-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e54ec-142">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="e54ec-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e54ec-143">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="e54ec-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e54ec-144">INPUTOBJECT： <IMySqlIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="e54ec-144">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e54ec-145">`[ConfigurationName <String>]`：伺服器組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e54ec-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="e54ec-146">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="e54ec-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="e54ec-147">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="e54ec-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="e54ec-148">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="e54ec-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e54ec-149">`[KeyName <String>]`：伺服器金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="e54ec-149">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="e54ec-150">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="e54ec-150">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="e54ec-151">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e54ec-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e54ec-152">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="e54ec-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="e54ec-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全性警示策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="e54ec-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="e54ec-154">`[ServerName <String>]`：伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="e54ec-154">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="e54ec-155">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e54ec-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="e54ec-156">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="e54ec-156">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="e54ec-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="e54ec-157">RELATED LINKS</span></span>

