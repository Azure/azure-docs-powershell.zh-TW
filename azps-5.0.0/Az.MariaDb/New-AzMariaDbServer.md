---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbServer.md
ms.openlocfilehash: e6416fd67091fc86a5fe9844d3b1d366aaa6cb58
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140093"
---
# <span data-ttu-id="8071e-101">New-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="8071e-101">New-AzMariaDbServer</span></span>

## <span data-ttu-id="8071e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8071e-102">SYNOPSIS</span></span>
<span data-ttu-id="8071e-103">建立新的 MariaDB。</span><span class="sxs-lookup"><span data-stu-id="8071e-103">Creates a new MariaDB.</span></span>

## <span data-ttu-id="8071e-104">句法</span><span class="sxs-lookup"><span data-stu-id="8071e-104">SYNTAX</span></span>

```
New-AzMariaDbServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUsername <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8071e-105">說明</span><span class="sxs-lookup"><span data-stu-id="8071e-105">DESCRIPTION</span></span>
<span data-ttu-id="8071e-106">建立新的 MariaDB。</span><span class="sxs-lookup"><span data-stu-id="8071e-106">Creates a new MariaDB.</span></span>

## <span data-ttu-id="8071e-107">示例</span><span class="sxs-lookup"><span data-stu-id="8071e-107">EXAMPLES</span></span>

### <span data-ttu-id="8071e-108">範例1：建立新的 MariaDB</span><span class="sxs-lookup"><span data-stu-id="8071e-108">Example 1: Create a new MariaDB</span></span>
```powershell
PS C:\> New-AzMariaDbServer -Name mariadb-aassd-01 -ResourceGroupName lucas-manual-test -Sku 'B_Gen5_1' -Location eastus
cmdlet New-AzMariaDbServer at command pipeline position 1
Supply values for the following parameters:
AdministratorUsername: adminuser
AdministratorLoginPassword: ************

Name             Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----             -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-aassd-01 eastus   adminuser          10.2    5120                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="8071e-109">這個命令會建立新的 MariaDB。</span><span class="sxs-lookup"><span data-stu-id="8071e-109">This command creates a new MariaDB.</span></span>

## <span data-ttu-id="8071e-110">參數</span><span class="sxs-lookup"><span data-stu-id="8071e-110">PARAMETERS</span></span>

### <span data-ttu-id="8071e-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="8071e-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="8071e-112">系統管理員的密碼應該是 SecureString。</span><span class="sxs-lookup"><span data-stu-id="8071e-112">Password of administrator, should be SecureString.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8071e-113">-AdministratorUsername</span><span class="sxs-lookup"><span data-stu-id="8071e-113">-AdministratorUsername</span></span>
<span data-ttu-id="8071e-114">系統管理員的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="8071e-114">Username of administrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8071e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8071e-115">-AsJob</span></span>
<span data-ttu-id="8071e-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="8071e-116">Run the command as a job</span></span>

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

### <span data-ttu-id="8071e-117">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="8071e-117">-BackupRetentionDay</span></span>
<span data-ttu-id="8071e-118">伺服器的備份保留天數。</span><span class="sxs-lookup"><span data-stu-id="8071e-118">Backup retention days for the server.</span></span>

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

### <span data-ttu-id="8071e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8071e-119">-DefaultProfile</span></span>
<span data-ttu-id="8071e-120">地區 DefaultParameters 用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8071e-120">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8071e-121">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="8071e-121">-GeoRedundantBackup</span></span>
<span data-ttu-id="8071e-122">啟用地域冗余，或不針對伺服器備份。</span><span class="sxs-lookup"><span data-stu-id="8071e-122">Enable Geo-redundant or not for server backup.</span></span>

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

### <span data-ttu-id="8071e-123">-位置</span><span class="sxs-lookup"><span data-stu-id="8071e-123">-Location</span></span>
<span data-ttu-id="8071e-124">資源所在的位置。</span><span class="sxs-lookup"><span data-stu-id="8071e-124">The location the resource resides in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8071e-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="8071e-125">-Name</span></span>
<span data-ttu-id="8071e-126">MariaDB [伺服器名稱]。</span><span class="sxs-lookup"><span data-stu-id="8071e-126">MariaDB server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8071e-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8071e-127">-NoWait</span></span>
<span data-ttu-id="8071e-128">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="8071e-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8071e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8071e-129">-ResourceGroupName</span></span>
<span data-ttu-id="8071e-130">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8071e-130">The name of the resource group that contains the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8071e-131">-Sku</span><span class="sxs-lookup"><span data-stu-id="8071e-131">-Sku</span></span>
<span data-ttu-id="8071e-132">Sku 的名稱，通常是 [層 + 家庭 + 核心]，例如 B_Gen4_1、GP_Gen5_8。</span><span class="sxs-lookup"><span data-stu-id="8071e-132">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8071e-133">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="8071e-133">-SslEnforcement</span></span>
<span data-ttu-id="8071e-134">在連線至伺服器時啟用 ssl 強制執行。</span><span class="sxs-lookup"><span data-stu-id="8071e-134">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="8071e-135">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="8071e-135">-StorageAutogrow</span></span>
<span data-ttu-id="8071e-136">啟用儲存空間自動增長。</span><span class="sxs-lookup"><span data-stu-id="8071e-136">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="8071e-137">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="8071e-137">-StorageInMb</span></span>
<span data-ttu-id="8071e-138">伺服器允許的最大儲存空間。</span><span class="sxs-lookup"><span data-stu-id="8071e-138">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="8071e-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8071e-139">-SubscriptionId</span></span>
<span data-ttu-id="8071e-140">訂閱識別碼是每個服務通話的 URI 的一部分</span><span class="sxs-lookup"><span data-stu-id="8071e-140">The subscription ID is part of the URI for every service call</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8071e-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="8071e-141">-Tag</span></span>
<span data-ttu-id="8071e-142">以鍵值對形式的特定應用程式中繼資料。</span><span class="sxs-lookup"><span data-stu-id="8071e-142">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="8071e-143">-版本</span><span class="sxs-lookup"><span data-stu-id="8071e-143">-Version</span></span>
<span data-ttu-id="8071e-144">伺服器版本。</span><span class="sxs-lookup"><span data-stu-id="8071e-144">Server version.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.ServerVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8071e-145">-確認</span><span class="sxs-lookup"><span data-stu-id="8071e-145">-Confirm</span></span>
<span data-ttu-id="8071e-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8071e-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8071e-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8071e-147">-WhatIf</span></span>
<span data-ttu-id="8071e-148">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8071e-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8071e-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8071e-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8071e-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8071e-150">CommonParameters</span></span>
<span data-ttu-id="8071e-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8071e-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8071e-152">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8071e-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8071e-153">輸入</span><span class="sxs-lookup"><span data-stu-id="8071e-153">INPUTS</span></span>

## <span data-ttu-id="8071e-154">輸出</span><span class="sxs-lookup"><span data-stu-id="8071e-154">OUTPUTS</span></span>

### <span data-ttu-id="8071e-155">IServer （MariaDb）。 Api20180601Preview。</span><span class="sxs-lookup"><span data-stu-id="8071e-155">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="8071e-156">筆記</span><span class="sxs-lookup"><span data-stu-id="8071e-156">NOTES</span></span>

<span data-ttu-id="8071e-157">別名</span><span class="sxs-lookup"><span data-stu-id="8071e-157">ALIASES</span></span>

## <span data-ttu-id="8071e-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="8071e-158">RELATED LINKS</span></span>

