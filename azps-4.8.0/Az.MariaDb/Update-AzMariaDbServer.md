---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbServer.md
ms.openlocfilehash: 0a6286c7574a2bf7226f8d4b80a5cac62c535a47
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970996"
---
# <span data-ttu-id="67705-101">Update-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="67705-101">Update-AzMariaDbServer</span></span>

## <span data-ttu-id="67705-102">摘要</span><span class="sxs-lookup"><span data-stu-id="67705-102">SYNOPSIS</span></span>
<span data-ttu-id="67705-103">更新現有的伺服器。</span><span class="sxs-lookup"><span data-stu-id="67705-103">Updates an existing server.</span></span>
<span data-ttu-id="67705-104">要求主體可以包含一個到在一般伺服器定義中存在的許多屬性。</span><span class="sxs-lookup"><span data-stu-id="67705-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="67705-105">如果您想要補救伺服器參數（例如 wait_timeout 或 net_retry_count），請改用 Update-AzMariaDbConfiguration。</span><span class="sxs-lookup"><span data-stu-id="67705-105">Use Update-AzMariaDbConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="67705-106">句法</span><span class="sxs-lookup"><span data-stu-id="67705-106">SYNTAX</span></span>

### <span data-ttu-id="67705-107">ServerName (預設) </span><span class="sxs-lookup"><span data-stu-id="67705-107">ServerName (Default)</span></span>
```
Update-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>]
 [-GeoRedundantBackup <GeoRedundantBackup>] [-ReplicationRole <String>] [-Sku <String>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="67705-108">ServerObject</span><span class="sxs-lookup"><span data-stu-id="67705-108">ServerObject</span></span>
```
Update-AzMariaDbServer -InputObject <IMariaDbIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>] [-ReplicationRole <String>]
 [-Sku <String>] [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>]
 [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="67705-109">說明</span><span class="sxs-lookup"><span data-stu-id="67705-109">DESCRIPTION</span></span>
<span data-ttu-id="67705-110">更新現有的伺服器。</span><span class="sxs-lookup"><span data-stu-id="67705-110">Updates an existing server.</span></span>
<span data-ttu-id="67705-111">要求主體可以包含一個到在一般伺服器定義中存在的許多屬性。</span><span class="sxs-lookup"><span data-stu-id="67705-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="67705-112">如果您想要補救伺服器參數（例如 wait_timeout 或 net_retry_count），請改用 Update-AzMariaDbConfiguration。</span><span class="sxs-lookup"><span data-stu-id="67705-112">Use Update-AzMariaDbConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="67705-113">示例</span><span class="sxs-lookup"><span data-stu-id="67705-113">EXAMPLES</span></span>

### <span data-ttu-id="67705-114">範例1：更新 MariaDB</span><span class="sxs-lookup"><span data-stu-id="67705-114">Example 1: Update MariaDB</span></span>
```powershell
PS C:\> Update-AzMariaDbServer -Name mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 -StorageInMb 8192

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-4rmtig eastus   xofavpndqj         10.2    8192                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="67705-115">這個命令會更新 MariaDB。</span><span class="sxs-lookup"><span data-stu-id="67705-115">This command updates a MariaDB.</span></span>

### <span data-ttu-id="67705-116">範例2：更新 MariaDB</span><span class="sxs-lookup"><span data-stu-id="67705-116">Example 2: Update MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 | Update-AzMariaDbServer -StorageInMb (8192+1024)

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-4rmtig eastus   xofavpndqj         10.2    9216                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="67705-117">這個命令會更新 MariaDB。</span><span class="sxs-lookup"><span data-stu-id="67705-117">This command updates a MariaDB.</span></span>

## <span data-ttu-id="67705-118">參數</span><span class="sxs-lookup"><span data-stu-id="67705-118">PARAMETERS</span></span>

### <span data-ttu-id="67705-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="67705-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="67705-120">系統管理員登入的密碼。</span><span class="sxs-lookup"><span data-stu-id="67705-120">The password of the administrator login.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67705-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="67705-121">-AsJob</span></span>
<span data-ttu-id="67705-122">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="67705-122">Run the command as a job</span></span>

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

### <span data-ttu-id="67705-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="67705-123">-BackupRetentionDay</span></span>
<span data-ttu-id="67705-124">伺服器的備份保留天數。</span><span class="sxs-lookup"><span data-stu-id="67705-124">Backup retention days for the server.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67705-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67705-125">-DefaultProfile</span></span>
<span data-ttu-id="67705-126">地區 DefaultParameters 用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="67705-126">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67705-127">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="67705-127">-GeoRedundantBackup</span></span>
<span data-ttu-id="67705-128">啟用地域冗余，或不針對伺服器備份。</span><span class="sxs-lookup"><span data-stu-id="67705-128">Enable Geo-redundant or not for server backup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.GeoRedundantBackup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67705-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67705-129">-InputObject</span></span>
<span data-ttu-id="67705-130">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="67705-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: ServerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67705-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="67705-131">-Name</span></span>
<span data-ttu-id="67705-132">MariaDB 伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="67705-132">MariaDB server name</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67705-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="67705-133">-NoWait</span></span>
<span data-ttu-id="67705-134">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="67705-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="67705-135">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="67705-135">-ReplicationRole</span></span>
<span data-ttu-id="67705-136">伺服器的複製角色。</span><span class="sxs-lookup"><span data-stu-id="67705-136">The replication role of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67705-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67705-137">-ResourceGroupName</span></span>
<span data-ttu-id="67705-138">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="67705-138">The name of the resource group that contains the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67705-139">-Sku</span><span class="sxs-lookup"><span data-stu-id="67705-139">-Sku</span></span>
<span data-ttu-id="67705-140">Sku 的名稱，通常是 [層 + 家庭 + 核心]，例如 B_Gen4_1、GP_Gen5_8。</span><span class="sxs-lookup"><span data-stu-id="67705-140">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67705-141">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="67705-141">-SslEnforcement</span></span>
<span data-ttu-id="67705-142">在連線至伺服器時啟用 ssl 強制執行。</span><span class="sxs-lookup"><span data-stu-id="67705-142">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67705-143">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="67705-143">-StorageAutogrow</span></span>
<span data-ttu-id="67705-144">啟用儲存空間自動增長。</span><span class="sxs-lookup"><span data-stu-id="67705-144">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67705-145">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="67705-145">-StorageInMb</span></span>
<span data-ttu-id="67705-146">伺服器允許的最大儲存空間。</span><span class="sxs-lookup"><span data-stu-id="67705-146">Max storage allowed for a server.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67705-147">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="67705-147">-SubscriptionId</span></span>
<span data-ttu-id="67705-148">訂閱識別碼是每個服務通話的 URI 的一部分</span><span class="sxs-lookup"><span data-stu-id="67705-148">The subscription ID is part of the URI for every service call</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67705-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="67705-149">-Tag</span></span>
<span data-ttu-id="67705-150">以鍵值對形式的特定應用程式中繼資料。</span><span class="sxs-lookup"><span data-stu-id="67705-150">Application-specific metadata in the form of key-value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67705-151">-確認</span><span class="sxs-lookup"><span data-stu-id="67705-151">-Confirm</span></span>
<span data-ttu-id="67705-152">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="67705-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67705-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67705-153">-WhatIf</span></span>
<span data-ttu-id="67705-154">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="67705-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67705-155">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="67705-155">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67705-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67705-156">CommonParameters</span></span>
<span data-ttu-id="67705-157">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="67705-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67705-158">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="67705-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67705-159">輸入</span><span class="sxs-lookup"><span data-stu-id="67705-159">INPUTS</span></span>

### <span data-ttu-id="67705-160">IMariaDbIdentity （MariaDb）的</span><span class="sxs-lookup"><span data-stu-id="67705-160">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="67705-161">輸出</span><span class="sxs-lookup"><span data-stu-id="67705-161">OUTPUTS</span></span>

### <span data-ttu-id="67705-162">IServer （MariaDb）。 Api20180601Preview。</span><span class="sxs-lookup"><span data-stu-id="67705-162">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="67705-163">筆記</span><span class="sxs-lookup"><span data-stu-id="67705-163">NOTES</span></span>

<span data-ttu-id="67705-164">別名</span><span class="sxs-lookup"><span data-stu-id="67705-164">ALIASES</span></span>

<span data-ttu-id="67705-165">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="67705-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="67705-166">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="67705-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="67705-167">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="67705-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="67705-168">INPUTOBJECT <IMariaDbIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="67705-168">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="67705-169">`[ConfigurationName <String>]`：伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="67705-169">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="67705-170">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="67705-170">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="67705-171">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="67705-171">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="67705-172">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="67705-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="67705-173">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="67705-173">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="67705-174">`[ResourceGroupName <String>]`：包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="67705-174">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="67705-175">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="67705-175">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="67705-176">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全警示原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="67705-176">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="67705-177">`[ServerName <String>]`：伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="67705-177">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="67705-178">`[SubscriptionId <String>]`：識別 Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="67705-178">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="67705-179">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="67705-179">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="67705-180">相關連結</span><span class="sxs-lookup"><span data-stu-id="67705-180">RELATED LINKS</span></span>

