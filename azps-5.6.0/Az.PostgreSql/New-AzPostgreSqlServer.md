---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/new-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlServer.md
ms.openlocfilehash: 71aa5886035164dee5b011be8a90b18e33e055e8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910961"
---
# <span data-ttu-id="a212b-101">New-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="a212b-101">New-AzPostgreSqlServer</span></span>

## <span data-ttu-id="a212b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a212b-102">SYNOPSIS</span></span>
<span data-ttu-id="a212b-103">建立新伺服器。</span><span class="sxs-lookup"><span data-stu-id="a212b-103">Creates a new server.</span></span>

## <span data-ttu-id="a212b-104">語法</span><span class="sxs-lookup"><span data-stu-id="a212b-104">SYNTAX</span></span>

```
New-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUserName <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-Version <ServerVersion>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a212b-105">描述</span><span class="sxs-lookup"><span data-stu-id="a212b-105">DESCRIPTION</span></span>
<span data-ttu-id="a212b-106">建立新伺服器。</span><span class="sxs-lookup"><span data-stu-id="a212b-106">Creates a new server.</span></span>

## <span data-ttu-id="a212b-107">例子</span><span class="sxs-lookup"><span data-stu-id="a212b-107">EXAMPLES</span></span>

### <span data-ttu-id="a212b-108">範例 1：建立新 PostgreSql 伺服器</span><span class="sxs-lookup"><span data-stu-id="a212b-108">Example 1: Create a new PostgreSql server</span></span>
```powershell
PS C:\> New-AzPostgreSqlServer -Name PostgreSqlTestServer -ResourceGroupName PostgreSqlTestRG -Location eastus -AdministratorUserName pwsh -AdministratorLoginPassword $password -Sku GP_Gen5_4

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="a212b-109">這些 Cmdlet 會建立一個新的 PostgreSql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="a212b-109">These cmdlets create a new PostgreSql server.</span></span>

## <span data-ttu-id="a212b-110">參數</span><span class="sxs-lookup"><span data-stu-id="a212b-110">PARAMETERS</span></span>

### <span data-ttu-id="a212b-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="a212b-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="a212b-112">系統管理員的密碼。</span><span class="sxs-lookup"><span data-stu-id="a212b-112">The password of the administrator.</span></span>
<span data-ttu-id="a212b-113">最少 8 個字元，最多 128 個字元。</span><span class="sxs-lookup"><span data-stu-id="a212b-113">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="a212b-114">密碼必須包含下列三種類別的字元：英文大寫字母、英文小寫字母、數位和非英數位元。</span><span class="sxs-lookup"><span data-stu-id="a212b-114">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

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

### <span data-ttu-id="a212b-115">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="a212b-115">-AdministratorUserName</span></span>
<span data-ttu-id="a212b-116">伺服器的系統管理員使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="a212b-116">Administrator username for the server.</span></span>
<span data-ttu-id="a212b-117">設定完成後，即無法變更。</span><span class="sxs-lookup"><span data-stu-id="a212b-117">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="a212b-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a212b-118">-AsJob</span></span>
<span data-ttu-id="a212b-119">以工作執行命令。</span><span class="sxs-lookup"><span data-stu-id="a212b-119">Run the command as a job.</span></span>

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

### <span data-ttu-id="a212b-120">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="a212b-120">-BackupRetentionDay</span></span>
<span data-ttu-id="a212b-121">伺服器的備份保留天數。</span><span class="sxs-lookup"><span data-stu-id="a212b-121">Backup retention days for the server.</span></span>
<span data-ttu-id="a212b-122">日計數介於 7 到 35 之間。</span><span class="sxs-lookup"><span data-stu-id="a212b-122">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="a212b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a212b-123">-DefaultProfile</span></span>
<span data-ttu-id="a212b-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a212b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a212b-125">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="a212b-125">-GeoRedundantBackup</span></span>
<span data-ttu-id="a212b-126">針對伺服器備份啟用異地重複或不啟用。</span><span class="sxs-lookup"><span data-stu-id="a212b-126">Enable Geo-redundant or not for server backup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.GeoRedundantBackup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a212b-127">-位置</span><span class="sxs-lookup"><span data-stu-id="a212b-127">-Location</span></span>
<span data-ttu-id="a212b-128">資源所在位置。</span><span class="sxs-lookup"><span data-stu-id="a212b-128">The location the resource resides in.</span></span>

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

### <span data-ttu-id="a212b-129">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="a212b-129">-MinimalTlsVersion</span></span>
<span data-ttu-id="a212b-130">在啟用 SSL 時，設定伺服器連至伺服器的最小 TLS 版本。</span><span class="sxs-lookup"><span data-stu-id="a212b-130">Set the minimal TLS version for connections to server when SSL is enabled.</span></span>
<span data-ttu-id="a212b-131">預設值為 TLSEnforcementDisabled.accepted 值：TLS1_0、TLS1_1、TLS1_2、TLSEnforcementDisabled。</span><span class="sxs-lookup"><span data-stu-id="a212b-131">Default is TLSEnforcementDisabled.accepted values: TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.MinimalTlsVersionEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a212b-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="a212b-132">-Name</span></span>
<span data-ttu-id="a212b-133">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="a212b-133">The name of the server.</span></span>

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

### <span data-ttu-id="a212b-134">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a212b-134">-NoWait</span></span>
<span data-ttu-id="a212b-135">非同步執行命令。</span><span class="sxs-lookup"><span data-stu-id="a212b-135">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="a212b-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a212b-136">-ResourceGroupName</span></span>
<span data-ttu-id="a212b-137">包含資源的資源組名，您可從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="a212b-137">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="a212b-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="a212b-138">-Sku</span></span>
<span data-ttu-id="a212b-139">SKU 的名稱，通常是 tier + family + 核心，例如 B_Gen4_1、GP_Gen5_8。</span><span class="sxs-lookup"><span data-stu-id="a212b-139">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="a212b-140">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="a212b-140">-SslEnforcement</span></span>
<span data-ttu-id="a212b-141">在連接至伺服器時啟用 ssl 強制執行或不啟用。</span><span class="sxs-lookup"><span data-stu-id="a212b-141">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a212b-142">-StorageAuto上</span><span class="sxs-lookup"><span data-stu-id="a212b-142">-StorageAutogrow</span></span>
<span data-ttu-id="a212b-143">啟用儲存空間自動放大。</span><span class="sxs-lookup"><span data-stu-id="a212b-143">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a212b-144">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="a212b-144">-StorageInMb</span></span>
<span data-ttu-id="a212b-145">伺服器允許的最大儲存空間。</span><span class="sxs-lookup"><span data-stu-id="a212b-145">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="a212b-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a212b-146">-SubscriptionId</span></span>
<span data-ttu-id="a212b-147">可識別 Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="a212b-147">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="a212b-148">-標記</span><span class="sxs-lookup"><span data-stu-id="a212b-148">-Tag</span></span>
<span data-ttu-id="a212b-149">以金鑰值組形式顯示的應用程式特定中繼資料。</span><span class="sxs-lookup"><span data-stu-id="a212b-149">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="a212b-150">-版本</span><span class="sxs-lookup"><span data-stu-id="a212b-150">-Version</span></span>
<span data-ttu-id="a212b-151">伺服器版本。</span><span class="sxs-lookup"><span data-stu-id="a212b-151">Server version.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.ServerVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a212b-152">-確認</span><span class="sxs-lookup"><span data-stu-id="a212b-152">-Confirm</span></span>
<span data-ttu-id="a212b-153">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a212b-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a212b-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a212b-154">-WhatIf</span></span>
<span data-ttu-id="a212b-155">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a212b-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a212b-156">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a212b-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a212b-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a212b-157">CommonParameters</span></span>
<span data-ttu-id="a212b-158">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a212b-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a212b-159">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a212b-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a212b-160">輸入</span><span class="sxs-lookup"><span data-stu-id="a212b-160">INPUTS</span></span>

## <span data-ttu-id="a212b-161">輸出</span><span class="sxs-lookup"><span data-stu-id="a212b-161">OUTPUTS</span></span>

### <span data-ttu-id="a212b-162">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="a212b-162">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="a212b-163">筆記</span><span class="sxs-lookup"><span data-stu-id="a212b-163">NOTES</span></span>

<span data-ttu-id="a212b-164">別名</span><span class="sxs-lookup"><span data-stu-id="a212b-164">ALIASES</span></span>

## <span data-ttu-id="a212b-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="a212b-165">RELATED LINKS</span></span>

