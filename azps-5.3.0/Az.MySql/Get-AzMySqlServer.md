---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlServer.md
ms.openlocfilehash: 4308f2ec3da458f03e53d17a873d92ea5d775ff4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449025"
---
# <span data-ttu-id="71bcb-101">Get-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="71bcb-101">Get-AzMySqlServer</span></span>

## <span data-ttu-id="71bcb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="71bcb-102">SYNOPSIS</span></span>
<span data-ttu-id="71bcb-103">取得伺服器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="71bcb-103">Gets information about a server.</span></span>

## <span data-ttu-id="71bcb-104">句法</span><span class="sxs-lookup"><span data-stu-id="71bcb-104">SYNTAX</span></span>

### <span data-ttu-id="71bcb-105">List1 (預設) </span><span class="sxs-lookup"><span data-stu-id="71bcb-105">List1 (Default)</span></span>
```
Get-AzMySqlServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="71bcb-106">獲取</span><span class="sxs-lookup"><span data-stu-id="71bcb-106">Get</span></span>
```
Get-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="71bcb-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="71bcb-107">GetViaIdentity</span></span>
```
Get-AzMySqlServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="71bcb-108">清單</span><span class="sxs-lookup"><span data-stu-id="71bcb-108">List</span></span>
```
Get-AzMySqlServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="71bcb-109">說明</span><span class="sxs-lookup"><span data-stu-id="71bcb-109">DESCRIPTION</span></span>
<span data-ttu-id="71bcb-110">取得伺服器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="71bcb-110">Gets information about a server.</span></span>

## <span data-ttu-id="71bcb-111">示例</span><span class="sxs-lookup"><span data-stu-id="71bcb-111">EXAMPLES</span></span>

### <span data-ttu-id="71bcb-112">範例1：使用預設內容取得 MySql 伺服器</span><span class="sxs-lookup"><span data-stu-id="71bcb-112">Example 1: Get MySql server with default context</span></span>
```powershell
PS C:\> Get-AzMySqlServer

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-11 eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="71bcb-113">這個 Cmdlet 會取得使用預設內容的 MySql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="71bcb-113">This cmdlet gets MySql server with default context.</span></span>

### <span data-ttu-id="71bcb-114">範例2：透過資源群組和伺服器名稱取得 MySql 伺服器</span><span class="sxs-lookup"><span data-stu-id="71bcb-114">Example 2: Get MySql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -Name mysql-test

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="71bcb-115">這個 Cmdlet 透過資源群組和伺服器名稱來取得 MySql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="71bcb-115">This cmdlet gets MySql server by resource group and server name.</span></span>

### <span data-ttu-id="71bcb-116">範例3：列出指定資源群組中的所有 MySql 伺服器</span><span class="sxs-lookup"><span data-stu-id="71bcb-116">Example 3: Lists all the MySql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="71bcb-117">這個 Cmdlet 會列出指定資源群組中的所有 MySql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="71bcb-117">This cmdlet lists all the MySql servers in specified resource group.</span></span>

### <span data-ttu-id="71bcb-118">範例4：透過身分識別取得 MySql 伺服器</span><span class="sxs-lookup"><span data-stu-id="71bcb-118">Example 4: Get MySql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test"
PS C:\> Get-AzMySqlServer -InputObject $ID

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="71bcb-119">這個 Cmdlet 清單會透過身分識別取得 MySql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="71bcb-119">This cmdlet lists gets MySql server by identity.</span></span>

## <span data-ttu-id="71bcb-120">參數</span><span class="sxs-lookup"><span data-stu-id="71bcb-120">PARAMETERS</span></span>

### <span data-ttu-id="71bcb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71bcb-121">-DefaultProfile</span></span>
<span data-ttu-id="71bcb-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="71bcb-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71bcb-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71bcb-123">-InputObject</span></span>
<span data-ttu-id="71bcb-124">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="71bcb-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="71bcb-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="71bcb-125">-Name</span></span>
<span data-ttu-id="71bcb-126">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="71bcb-126">The name of the server.</span></span>

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

### <span data-ttu-id="71bcb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71bcb-127">-ResourceGroupName</span></span>
<span data-ttu-id="71bcb-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="71bcb-128">The name of the resource group.</span></span>
<span data-ttu-id="71bcb-129">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="71bcb-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="71bcb-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="71bcb-130">-SubscriptionId</span></span>
<span data-ttu-id="71bcb-131">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="71bcb-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="71bcb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71bcb-132">CommonParameters</span></span>
<span data-ttu-id="71bcb-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="71bcb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71bcb-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="71bcb-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71bcb-135">輸入</span><span class="sxs-lookup"><span data-stu-id="71bcb-135">INPUTS</span></span>

### <span data-ttu-id="71bcb-136">IMySqlIdentity 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="71bcb-136">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="71bcb-137">輸出</span><span class="sxs-lookup"><span data-stu-id="71bcb-137">OUTPUTS</span></span>

### <span data-ttu-id="71bcb-138">IServer 中的 Api20171201 （）。</span><span class="sxs-lookup"><span data-stu-id="71bcb-138">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="71bcb-139">筆記</span><span class="sxs-lookup"><span data-stu-id="71bcb-139">NOTES</span></span>

<span data-ttu-id="71bcb-140">別名</span><span class="sxs-lookup"><span data-stu-id="71bcb-140">ALIASES</span></span>

<span data-ttu-id="71bcb-141">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="71bcb-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="71bcb-142">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="71bcb-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="71bcb-143">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="71bcb-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="71bcb-144">INPUTOBJECT <IMySqlIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="71bcb-144">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="71bcb-145">`[ConfigurationName <String>]`：伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="71bcb-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="71bcb-146">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="71bcb-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="71bcb-147">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="71bcb-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="71bcb-148">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="71bcb-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="71bcb-149">`[KeyName <String>]`：伺服器金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="71bcb-149">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="71bcb-150">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="71bcb-150">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="71bcb-151">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="71bcb-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="71bcb-152">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="71bcb-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="71bcb-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全警示原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="71bcb-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="71bcb-154">`[ServerName <String>]`：伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="71bcb-154">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="71bcb-155">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="71bcb-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="71bcb-156">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="71bcb-156">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="71bcb-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="71bcb-157">RELATED LINKS</span></span>

