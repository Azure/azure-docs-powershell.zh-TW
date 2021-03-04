---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/new-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbServer.md
ms.openlocfilehash: ccd05d8c0a7678b16831659fb0ca119adf94ddae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904382"
---
# <span data-ttu-id="38356-101">New-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="38356-101">New-AzMariaDbServer</span></span>

## <span data-ttu-id="38356-102">簡介</span><span class="sxs-lookup"><span data-stu-id="38356-102">SYNOPSIS</span></span>
<span data-ttu-id="38356-103">建立新 MariaDB。</span><span class="sxs-lookup"><span data-stu-id="38356-103">Creates a new MariaDB.</span></span>

## <span data-ttu-id="38356-104">語法</span><span class="sxs-lookup"><span data-stu-id="38356-104">SYNTAX</span></span>

```
New-AzMariaDbServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUsername <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="38356-105">描述</span><span class="sxs-lookup"><span data-stu-id="38356-105">DESCRIPTION</span></span>
<span data-ttu-id="38356-106">建立新 MariaDB。</span><span class="sxs-lookup"><span data-stu-id="38356-106">Creates a new MariaDB.</span></span>

## <span data-ttu-id="38356-107">例子</span><span class="sxs-lookup"><span data-stu-id="38356-107">EXAMPLES</span></span>

### <span data-ttu-id="38356-108">範例 1：建立新 MariaDB</span><span class="sxs-lookup"><span data-stu-id="38356-108">Example 1: Create a new MariaDB</span></span>
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

<span data-ttu-id="38356-109">此命令會建立一個新的 MariaDB。</span><span class="sxs-lookup"><span data-stu-id="38356-109">This command creates a new MariaDB.</span></span>

## <span data-ttu-id="38356-110">參數</span><span class="sxs-lookup"><span data-stu-id="38356-110">PARAMETERS</span></span>

### <span data-ttu-id="38356-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="38356-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="38356-112">系統管理員的密碼應該是 SecureString。</span><span class="sxs-lookup"><span data-stu-id="38356-112">Password of administrator, should be SecureString.</span></span>

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

### <span data-ttu-id="38356-113">-AdministratorUsername</span><span class="sxs-lookup"><span data-stu-id="38356-113">-AdministratorUsername</span></span>
<span data-ttu-id="38356-114">系統管理員使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="38356-114">Username of administrator.</span></span>

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

### <span data-ttu-id="38356-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="38356-115">-AsJob</span></span>
<span data-ttu-id="38356-116">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="38356-116">Run the command as a job</span></span>

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

### <span data-ttu-id="38356-117">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="38356-117">-BackupRetentionDay</span></span>
<span data-ttu-id="38356-118">伺服器的備份保留天數。</span><span class="sxs-lookup"><span data-stu-id="38356-118">Backup retention days for the server.</span></span>

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

### <span data-ttu-id="38356-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38356-119">-DefaultProfile</span></span>
<span data-ttu-id="38356-120">區域 DefaultParameters 用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="38356-120">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38356-121">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="38356-121">-GeoRedundantBackup</span></span>
<span data-ttu-id="38356-122">針對伺服器備份啟用異地重複或不啟用。</span><span class="sxs-lookup"><span data-stu-id="38356-122">Enable Geo-redundant or not for server backup.</span></span>

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

### <span data-ttu-id="38356-123">-位置</span><span class="sxs-lookup"><span data-stu-id="38356-123">-Location</span></span>
<span data-ttu-id="38356-124">資源所在位置。</span><span class="sxs-lookup"><span data-stu-id="38356-124">The location the resource resides in.</span></span>

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

### <span data-ttu-id="38356-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="38356-125">-Name</span></span>
<span data-ttu-id="38356-126">MariaDB 伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="38356-126">MariaDB server name.</span></span>

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

### <span data-ttu-id="38356-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="38356-127">-NoWait</span></span>
<span data-ttu-id="38356-128">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="38356-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="38356-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38356-129">-ResourceGroupName</span></span>
<span data-ttu-id="38356-130">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="38356-130">The name of the resource group that contains the resource.</span></span>

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

### <span data-ttu-id="38356-131">-SKU</span><span class="sxs-lookup"><span data-stu-id="38356-131">-Sku</span></span>
<span data-ttu-id="38356-132">SKU 的名稱，通常是 tier + family + 核心，例如 B_Gen4_1、GP_Gen5_8。</span><span class="sxs-lookup"><span data-stu-id="38356-132">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="38356-133">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="38356-133">-SslEnforcement</span></span>
<span data-ttu-id="38356-134">在連接至伺服器時啟用 ssl 強制執行或不啟用。</span><span class="sxs-lookup"><span data-stu-id="38356-134">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="38356-135">-StorageAuto上</span><span class="sxs-lookup"><span data-stu-id="38356-135">-StorageAutogrow</span></span>
<span data-ttu-id="38356-136">啟用儲存空間自動放大。</span><span class="sxs-lookup"><span data-stu-id="38356-136">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="38356-137">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="38356-137">-StorageInMb</span></span>
<span data-ttu-id="38356-138">伺服器允許的最大儲存空間。</span><span class="sxs-lookup"><span data-stu-id="38356-138">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="38356-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="38356-139">-SubscriptionId</span></span>
<span data-ttu-id="38356-140">訂閱識別碼是每個服務通話 URI 的一部分</span><span class="sxs-lookup"><span data-stu-id="38356-140">The subscription ID is part of the URI for every service call</span></span>

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

### <span data-ttu-id="38356-141">-標記</span><span class="sxs-lookup"><span data-stu-id="38356-141">-Tag</span></span>
<span data-ttu-id="38356-142">以金鑰值組形式顯示的應用程式特定中繼資料。</span><span class="sxs-lookup"><span data-stu-id="38356-142">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="38356-143">-版本</span><span class="sxs-lookup"><span data-stu-id="38356-143">-Version</span></span>
<span data-ttu-id="38356-144">伺服器版本。</span><span class="sxs-lookup"><span data-stu-id="38356-144">Server version.</span></span>

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

### <span data-ttu-id="38356-145">-確認</span><span class="sxs-lookup"><span data-stu-id="38356-145">-Confirm</span></span>
<span data-ttu-id="38356-146">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="38356-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38356-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38356-147">-WhatIf</span></span>
<span data-ttu-id="38356-148">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="38356-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38356-149">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="38356-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38356-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38356-150">CommonParameters</span></span>
<span data-ttu-id="38356-151">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="38356-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38356-152">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="38356-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38356-153">輸入</span><span class="sxs-lookup"><span data-stu-id="38356-153">INPUTS</span></span>

## <span data-ttu-id="38356-154">輸出</span><span class="sxs-lookup"><span data-stu-id="38356-154">OUTPUTS</span></span>

### <span data-ttu-id="38356-155">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="38356-155">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="38356-156">筆記</span><span class="sxs-lookup"><span data-stu-id="38356-156">NOTES</span></span>

<span data-ttu-id="38356-157">別名</span><span class="sxs-lookup"><span data-stu-id="38356-157">ALIASES</span></span>

## <span data-ttu-id="38356-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="38356-158">RELATED LINKS</span></span>

