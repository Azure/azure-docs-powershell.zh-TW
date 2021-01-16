---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlServer.md
ms.openlocfilehash: 683ca81587ff7c71f1406eb7a4accef37aac794d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435281"
---
# <span data-ttu-id="6820b-101">New-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="6820b-101">New-AzMySqlServer</span></span>

## <span data-ttu-id="6820b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6820b-102">SYNOPSIS</span></span>
<span data-ttu-id="6820b-103">建立新的伺服器。</span><span class="sxs-lookup"><span data-stu-id="6820b-103">Creates a new server.</span></span>

## <span data-ttu-id="6820b-104">句法</span><span class="sxs-lookup"><span data-stu-id="6820b-104">SYNTAX</span></span>

```
New-AzMySqlServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUserName <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6820b-105">說明</span><span class="sxs-lookup"><span data-stu-id="6820b-105">DESCRIPTION</span></span>
<span data-ttu-id="6820b-106">建立新的伺服器。</span><span class="sxs-lookup"><span data-stu-id="6820b-106">Creates a new server.</span></span>

## <span data-ttu-id="6820b-107">示例</span><span class="sxs-lookup"><span data-stu-id="6820b-107">EXAMPLES</span></span>

### <span data-ttu-id="6820b-108">範例1：建立新的 MySql 伺服器</span><span class="sxs-lookup"><span data-stu-id="6820b-108">Example 1: Create a new MySql server</span></span>
```powershell
PS C:\> New-AzMySqlServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -Location eastus -AdministratorUser mysql_test -AdministratorLoginPassword $password -Sku GP_Gen5_4

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="6820b-109">這些 Cmdlet 會建立新的 MySql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="6820b-109">These cmdlets create a new MySql server.</span></span>

## <span data-ttu-id="6820b-110">參數</span><span class="sxs-lookup"><span data-stu-id="6820b-110">PARAMETERS</span></span>

### <span data-ttu-id="6820b-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="6820b-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="6820b-112">系統管理員的密碼。</span><span class="sxs-lookup"><span data-stu-id="6820b-112">The password of the administrator.</span></span>
<span data-ttu-id="6820b-113">最少8個字元和最大的128個字元。</span><span class="sxs-lookup"><span data-stu-id="6820b-113">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="6820b-114">密碼必須包含下列其中三種類別的字元：英文大寫字母、英文小寫字母、數位和非數位元字元。</span><span class="sxs-lookup"><span data-stu-id="6820b-114">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

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

### <span data-ttu-id="6820b-115">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="6820b-115">-AdministratorUserName</span></span>
<span data-ttu-id="6820b-116">伺服器的系統管理員使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="6820b-116">Administrator username for the server.</span></span>
<span data-ttu-id="6820b-117">一旦設定，就無法變更。</span><span class="sxs-lookup"><span data-stu-id="6820b-117">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="6820b-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6820b-118">-AsJob</span></span>
<span data-ttu-id="6820b-119">執行命令做為作業。</span><span class="sxs-lookup"><span data-stu-id="6820b-119">Run the command as a job.</span></span>

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

### <span data-ttu-id="6820b-120">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="6820b-120">-BackupRetentionDay</span></span>
<span data-ttu-id="6820b-121">伺服器的備份保留天數。</span><span class="sxs-lookup"><span data-stu-id="6820b-121">Backup retention days for the server.</span></span>
<span data-ttu-id="6820b-122">日算在7到35。</span><span class="sxs-lookup"><span data-stu-id="6820b-122">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="6820b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6820b-123">-DefaultProfile</span></span>
<span data-ttu-id="6820b-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6820b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6820b-125">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="6820b-125">-GeoRedundantBackup</span></span>
<span data-ttu-id="6820b-126">啟用地域冗余，或不針對伺服器備份。</span><span class="sxs-lookup"><span data-stu-id="6820b-126">Enable Geo-redundant or not for server backup.</span></span>

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

### <span data-ttu-id="6820b-127">-位置</span><span class="sxs-lookup"><span data-stu-id="6820b-127">-Location</span></span>
<span data-ttu-id="6820b-128">資源所在的位置。</span><span class="sxs-lookup"><span data-stu-id="6820b-128">The location the resource resides in.</span></span>

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

### <span data-ttu-id="6820b-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="6820b-129">-Name</span></span>
<span data-ttu-id="6820b-130">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="6820b-130">The name of the server.</span></span>

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

### <span data-ttu-id="6820b-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6820b-131">-NoWait</span></span>
<span data-ttu-id="6820b-132">以非同步方式執行命令。</span><span class="sxs-lookup"><span data-stu-id="6820b-132">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="6820b-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6820b-133">-ResourceGroupName</span></span>
<span data-ttu-id="6820b-134">包含資源之資源群組的名稱，您可以從 Azure 資源管理員 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="6820b-134">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="6820b-135">-Sku</span><span class="sxs-lookup"><span data-stu-id="6820b-135">-Sku</span></span>
<span data-ttu-id="6820b-136">Sku 的名稱，通常是 [層 + 家庭 + 核心]，例如 B_Gen4_1、GP_Gen5_8。</span><span class="sxs-lookup"><span data-stu-id="6820b-136">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="6820b-137">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="6820b-137">-SslEnforcement</span></span>
<span data-ttu-id="6820b-138">在連線至伺服器時啟用 ssl 強制執行。</span><span class="sxs-lookup"><span data-stu-id="6820b-138">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="6820b-139">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="6820b-139">-StorageAutogrow</span></span>
<span data-ttu-id="6820b-140">啟用儲存空間自動增長。</span><span class="sxs-lookup"><span data-stu-id="6820b-140">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="6820b-141">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="6820b-141">-StorageInMb</span></span>
<span data-ttu-id="6820b-142">伺服器允許的最大儲存空間。</span><span class="sxs-lookup"><span data-stu-id="6820b-142">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="6820b-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6820b-143">-SubscriptionId</span></span>
<span data-ttu-id="6820b-144">識別 Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="6820b-144">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="6820b-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="6820b-145">-Tag</span></span>
<span data-ttu-id="6820b-146">以鍵值對形式的特定應用程式中繼資料。</span><span class="sxs-lookup"><span data-stu-id="6820b-146">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="6820b-147">-版本</span><span class="sxs-lookup"><span data-stu-id="6820b-147">-Version</span></span>
<span data-ttu-id="6820b-148">伺服器版本。</span><span class="sxs-lookup"><span data-stu-id="6820b-148">Server version.</span></span>

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

### <span data-ttu-id="6820b-149">-確認</span><span class="sxs-lookup"><span data-stu-id="6820b-149">-Confirm</span></span>
<span data-ttu-id="6820b-150">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6820b-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6820b-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6820b-151">-WhatIf</span></span>
<span data-ttu-id="6820b-152">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6820b-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6820b-153">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6820b-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6820b-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6820b-154">CommonParameters</span></span>
<span data-ttu-id="6820b-155">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6820b-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6820b-156">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6820b-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6820b-157">輸入</span><span class="sxs-lookup"><span data-stu-id="6820b-157">INPUTS</span></span>

## <span data-ttu-id="6820b-158">輸出</span><span class="sxs-lookup"><span data-stu-id="6820b-158">OUTPUTS</span></span>

### <span data-ttu-id="6820b-159">IServer 中的 Api20171201 （）。</span><span class="sxs-lookup"><span data-stu-id="6820b-159">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="6820b-160">筆記</span><span class="sxs-lookup"><span data-stu-id="6820b-160">NOTES</span></span>

<span data-ttu-id="6820b-161">別名</span><span class="sxs-lookup"><span data-stu-id="6820b-161">ALIASES</span></span>

## <span data-ttu-id="6820b-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="6820b-162">RELATED LINKS</span></span>

