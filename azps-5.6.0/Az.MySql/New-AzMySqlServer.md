---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/new-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlServer.md
ms.openlocfilehash: 2ae1e3e92a4118cb6d629f82a837b161ac012724
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904626"
---
# <span data-ttu-id="ae95a-101">New-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="ae95a-101">New-AzMySqlServer</span></span>

## <span data-ttu-id="ae95a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ae95a-102">SYNOPSIS</span></span>
<span data-ttu-id="ae95a-103">建立新伺服器。</span><span class="sxs-lookup"><span data-stu-id="ae95a-103">Creates a new server.</span></span>

## <span data-ttu-id="ae95a-104">語法</span><span class="sxs-lookup"><span data-stu-id="ae95a-104">SYNTAX</span></span>

```
New-AzMySqlServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUserName <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-Version <ServerVersion>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ae95a-105">描述</span><span class="sxs-lookup"><span data-stu-id="ae95a-105">DESCRIPTION</span></span>
<span data-ttu-id="ae95a-106">建立新伺服器。</span><span class="sxs-lookup"><span data-stu-id="ae95a-106">Creates a new server.</span></span>

## <span data-ttu-id="ae95a-107">例子</span><span class="sxs-lookup"><span data-stu-id="ae95a-107">EXAMPLES</span></span>

### <span data-ttu-id="ae95a-108">範例 1：建立新 MySql 伺服器</span><span class="sxs-lookup"><span data-stu-id="ae95a-108">Example 1: Create a new MySql server</span></span>
```powershell
PS C:\> New-AzMySqlServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -Location eastus -AdministratorUser mysql_test -AdministratorLoginPassword $password -Sku GP_Gen5_4

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="ae95a-109">這些 Cmdlet 會建立一個新的 MySql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="ae95a-109">These cmdlets create a new MySql server.</span></span>

## <span data-ttu-id="ae95a-110">參數</span><span class="sxs-lookup"><span data-stu-id="ae95a-110">PARAMETERS</span></span>

### <span data-ttu-id="ae95a-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="ae95a-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="ae95a-112">系統管理員的密碼。</span><span class="sxs-lookup"><span data-stu-id="ae95a-112">The password of the administrator.</span></span>
<span data-ttu-id="ae95a-113">最少 8 個字元，最多 128 個字元。</span><span class="sxs-lookup"><span data-stu-id="ae95a-113">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="ae95a-114">密碼必須包含下列三種類別的字元：英文大寫字母、英文小寫字母、數位和非英數位元。</span><span class="sxs-lookup"><span data-stu-id="ae95a-114">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

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

### <span data-ttu-id="ae95a-115">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="ae95a-115">-AdministratorUserName</span></span>
<span data-ttu-id="ae95a-116">伺服器的系統管理員使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="ae95a-116">Administrator username for the server.</span></span>
<span data-ttu-id="ae95a-117">設定完成後，即無法變更。</span><span class="sxs-lookup"><span data-stu-id="ae95a-117">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="ae95a-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ae95a-118">-AsJob</span></span>
<span data-ttu-id="ae95a-119">以工作執行命令。</span><span class="sxs-lookup"><span data-stu-id="ae95a-119">Run the command as a job.</span></span>

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

### <span data-ttu-id="ae95a-120">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="ae95a-120">-BackupRetentionDay</span></span>
<span data-ttu-id="ae95a-121">伺服器的備份保留天數。</span><span class="sxs-lookup"><span data-stu-id="ae95a-121">Backup retention days for the server.</span></span>
<span data-ttu-id="ae95a-122">日計數介於 7 到 35 之間。</span><span class="sxs-lookup"><span data-stu-id="ae95a-122">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="ae95a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae95a-123">-DefaultProfile</span></span>
<span data-ttu-id="ae95a-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ae95a-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae95a-125">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="ae95a-125">-GeoRedundantBackup</span></span>
<span data-ttu-id="ae95a-126">針對伺服器備份啟用異地重複或不啟用。</span><span class="sxs-lookup"><span data-stu-id="ae95a-126">Enable Geo-redundant or not for server backup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.GeoRedundantBackup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae95a-127">-位置</span><span class="sxs-lookup"><span data-stu-id="ae95a-127">-Location</span></span>
<span data-ttu-id="ae95a-128">資源所在位置。</span><span class="sxs-lookup"><span data-stu-id="ae95a-128">The location the resource resides in.</span></span>

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

### <span data-ttu-id="ae95a-129">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="ae95a-129">-MinimalTlsVersion</span></span>
<span data-ttu-id="ae95a-130">在啟用 SSL 時，設定伺服器連至伺服器的最小 TLS 版本。</span><span class="sxs-lookup"><span data-stu-id="ae95a-130">Set the minimal TLS version for connections to server when SSL is enabled.</span></span>
<span data-ttu-id="ae95a-131">預設值為 TLSEnforcementDisabled.accepted 值：TLS1_0、TLS1_1、TLS1_2、TLSEnforcementDisabled。</span><span class="sxs-lookup"><span data-stu-id="ae95a-131">Default is TLSEnforcementDisabled.accepted values: TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.MinimalTlsVersionEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae95a-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="ae95a-132">-Name</span></span>
<span data-ttu-id="ae95a-133">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="ae95a-133">The name of the server.</span></span>

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

### <span data-ttu-id="ae95a-134">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ae95a-134">-NoWait</span></span>
<span data-ttu-id="ae95a-135">非同步執行命令。</span><span class="sxs-lookup"><span data-stu-id="ae95a-135">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="ae95a-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae95a-136">-ResourceGroupName</span></span>
<span data-ttu-id="ae95a-137">包含資源的資源組名，您可從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="ae95a-137">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="ae95a-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="ae95a-138">-Sku</span></span>
<span data-ttu-id="ae95a-139">SKU 的名稱，通常是 tier + family + 核心，例如 B_Gen4_1、GP_Gen5_8。</span><span class="sxs-lookup"><span data-stu-id="ae95a-139">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="ae95a-140">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="ae95a-140">-SslEnforcement</span></span>
<span data-ttu-id="ae95a-141">在連接至伺服器時啟用 ssl 強制執行或不啟用。</span><span class="sxs-lookup"><span data-stu-id="ae95a-141">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae95a-142">-StorageAuto上</span><span class="sxs-lookup"><span data-stu-id="ae95a-142">-StorageAutogrow</span></span>
<span data-ttu-id="ae95a-143">啟用儲存空間自動放大。</span><span class="sxs-lookup"><span data-stu-id="ae95a-143">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae95a-144">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="ae95a-144">-StorageInMb</span></span>
<span data-ttu-id="ae95a-145">伺服器允許的最大儲存空間。</span><span class="sxs-lookup"><span data-stu-id="ae95a-145">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="ae95a-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ae95a-146">-SubscriptionId</span></span>
<span data-ttu-id="ae95a-147">可識別 Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="ae95a-147">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="ae95a-148">-標記</span><span class="sxs-lookup"><span data-stu-id="ae95a-148">-Tag</span></span>
<span data-ttu-id="ae95a-149">以金鑰值組形式顯示的應用程式特定中繼資料。</span><span class="sxs-lookup"><span data-stu-id="ae95a-149">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="ae95a-150">-版本</span><span class="sxs-lookup"><span data-stu-id="ae95a-150">-Version</span></span>
<span data-ttu-id="ae95a-151">伺服器版本。</span><span class="sxs-lookup"><span data-stu-id="ae95a-151">Server version.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.ServerVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae95a-152">-確認</span><span class="sxs-lookup"><span data-stu-id="ae95a-152">-Confirm</span></span>
<span data-ttu-id="ae95a-153">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ae95a-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae95a-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae95a-154">-WhatIf</span></span>
<span data-ttu-id="ae95a-155">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ae95a-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae95a-156">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ae95a-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae95a-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae95a-157">CommonParameters</span></span>
<span data-ttu-id="ae95a-158">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ae95a-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae95a-159">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ae95a-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae95a-160">輸入</span><span class="sxs-lookup"><span data-stu-id="ae95a-160">INPUTS</span></span>

## <span data-ttu-id="ae95a-161">輸出</span><span class="sxs-lookup"><span data-stu-id="ae95a-161">OUTPUTS</span></span>

### <span data-ttu-id="ae95a-162">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="ae95a-162">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="ae95a-163">筆記</span><span class="sxs-lookup"><span data-stu-id="ae95a-163">NOTES</span></span>

<span data-ttu-id="ae95a-164">別名</span><span class="sxs-lookup"><span data-stu-id="ae95a-164">ALIASES</span></span>

## <span data-ttu-id="ae95a-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="ae95a-165">RELATED LINKS</span></span>

