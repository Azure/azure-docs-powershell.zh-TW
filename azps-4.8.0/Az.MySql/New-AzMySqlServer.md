---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlServer.md
ms.openlocfilehash: 3b9ca8c4aa236b690bbe0dfe09c35f0ebc8a5b22
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969620"
---
# <span data-ttu-id="eeb82-101">New-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="eeb82-101">New-AzMySqlServer</span></span>

## <span data-ttu-id="eeb82-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eeb82-102">SYNOPSIS</span></span>
<span data-ttu-id="eeb82-103">建立新的伺服器。</span><span class="sxs-lookup"><span data-stu-id="eeb82-103">Creates a new server.</span></span>

## <span data-ttu-id="eeb82-104">句法</span><span class="sxs-lookup"><span data-stu-id="eeb82-104">SYNTAX</span></span>

```
New-AzMySqlServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUserName <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="eeb82-105">說明</span><span class="sxs-lookup"><span data-stu-id="eeb82-105">DESCRIPTION</span></span>
<span data-ttu-id="eeb82-106">建立新的伺服器。</span><span class="sxs-lookup"><span data-stu-id="eeb82-106">Creates a new server.</span></span>

## <span data-ttu-id="eeb82-107">示例</span><span class="sxs-lookup"><span data-stu-id="eeb82-107">EXAMPLES</span></span>

### <span data-ttu-id="eeb82-108">範例1：建立新的 MySql 伺服器</span><span class="sxs-lookup"><span data-stu-id="eeb82-108">Example 1: Create a new MySql server</span></span>
```powershell
PS C:\> New-AzMySqlServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -Location eastus -AdministratorUser mysql_test -AdministratorLoginPassword $password -Sku GP_Gen5_4

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="eeb82-109">這些 Cmdlet 會建立新的 MySql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="eeb82-109">These cmdlets create a new MySql server.</span></span>

## <span data-ttu-id="eeb82-110">參數</span><span class="sxs-lookup"><span data-stu-id="eeb82-110">PARAMETERS</span></span>

### <span data-ttu-id="eeb82-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="eeb82-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="eeb82-112">資源所在的位置。</span><span class="sxs-lookup"><span data-stu-id="eeb82-112">The location the resource resides in.</span></span>

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

### <span data-ttu-id="eeb82-113">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="eeb82-113">-AdministratorUserName</span></span>
<span data-ttu-id="eeb82-114">資源所在的位置。</span><span class="sxs-lookup"><span data-stu-id="eeb82-114">The location the resource resides in.</span></span>

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

### <span data-ttu-id="eeb82-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eeb82-115">-AsJob</span></span>
<span data-ttu-id="eeb82-116">執行命令做為作業。</span><span class="sxs-lookup"><span data-stu-id="eeb82-116">Run the command as a job.</span></span>

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

### <span data-ttu-id="eeb82-117">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="eeb82-117">-BackupRetentionDay</span></span>
<span data-ttu-id="eeb82-118">伺服器的備份保留天數。</span><span class="sxs-lookup"><span data-stu-id="eeb82-118">Backup retention days for the server.</span></span>
<span data-ttu-id="eeb82-119">日算在7到35。</span><span class="sxs-lookup"><span data-stu-id="eeb82-119">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="eeb82-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eeb82-120">-DefaultProfile</span></span>
<span data-ttu-id="eeb82-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="eeb82-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eeb82-122">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="eeb82-122">-GeoRedundantBackup</span></span>
<span data-ttu-id="eeb82-123">啟用地域冗余，或不針對伺服器備份。</span><span class="sxs-lookup"><span data-stu-id="eeb82-123">Enable Geo-redundant or not for server backup.</span></span>

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

### <span data-ttu-id="eeb82-124">-位置</span><span class="sxs-lookup"><span data-stu-id="eeb82-124">-Location</span></span>
<span data-ttu-id="eeb82-125">資源所在的位置。</span><span class="sxs-lookup"><span data-stu-id="eeb82-125">The location the resource resides in.</span></span>

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

### <span data-ttu-id="eeb82-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="eeb82-126">-Name</span></span>
<span data-ttu-id="eeb82-127">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="eeb82-127">The name of the server.</span></span>

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

### <span data-ttu-id="eeb82-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="eeb82-128">-NoWait</span></span>
<span data-ttu-id="eeb82-129">以非同步方式執行命令。</span><span class="sxs-lookup"><span data-stu-id="eeb82-129">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="eeb82-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eeb82-130">-ResourceGroupName</span></span>
<span data-ttu-id="eeb82-131">包含資源之資源群組的名稱，您可以從 Azure 資源管理員 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="eeb82-131">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="eeb82-132">-Sku</span><span class="sxs-lookup"><span data-stu-id="eeb82-132">-Sku</span></span>
<span data-ttu-id="eeb82-133">Sku 的名稱，通常是 [層 + 家庭 + 核心]，例如 B_Gen4_1、GP_Gen5_8。</span><span class="sxs-lookup"><span data-stu-id="eeb82-133">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="eeb82-134">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="eeb82-134">-SslEnforcement</span></span>
<span data-ttu-id="eeb82-135">在連線至伺服器時啟用 ssl 強制執行。</span><span class="sxs-lookup"><span data-stu-id="eeb82-135">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="eeb82-136">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="eeb82-136">-StorageAutogrow</span></span>
<span data-ttu-id="eeb82-137">啟用儲存空間自動增長。</span><span class="sxs-lookup"><span data-stu-id="eeb82-137">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="eeb82-138">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="eeb82-138">-StorageInMb</span></span>
<span data-ttu-id="eeb82-139">伺服器允許的最大儲存空間。</span><span class="sxs-lookup"><span data-stu-id="eeb82-139">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="eeb82-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="eeb82-140">-SubscriptionId</span></span>
<span data-ttu-id="eeb82-141">識別 Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="eeb82-141">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="eeb82-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="eeb82-142">-Tag</span></span>
<span data-ttu-id="eeb82-143">以鍵值對形式的特定應用程式中繼資料。</span><span class="sxs-lookup"><span data-stu-id="eeb82-143">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="eeb82-144">-版本</span><span class="sxs-lookup"><span data-stu-id="eeb82-144">-Version</span></span>
<span data-ttu-id="eeb82-145">伺服器版本。</span><span class="sxs-lookup"><span data-stu-id="eeb82-145">Server version.</span></span>

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

### <span data-ttu-id="eeb82-146">-確認</span><span class="sxs-lookup"><span data-stu-id="eeb82-146">-Confirm</span></span>
<span data-ttu-id="eeb82-147">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="eeb82-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eeb82-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eeb82-148">-WhatIf</span></span>
<span data-ttu-id="eeb82-149">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="eeb82-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eeb82-150">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eeb82-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eeb82-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eeb82-151">CommonParameters</span></span>
<span data-ttu-id="eeb82-152">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eeb82-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eeb82-153">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="eeb82-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eeb82-154">輸入</span><span class="sxs-lookup"><span data-stu-id="eeb82-154">INPUTS</span></span>

## <span data-ttu-id="eeb82-155">輸出</span><span class="sxs-lookup"><span data-stu-id="eeb82-155">OUTPUTS</span></span>

### <span data-ttu-id="eeb82-156">IServer 中的 Api20171201 （）。</span><span class="sxs-lookup"><span data-stu-id="eeb82-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="eeb82-157">筆記</span><span class="sxs-lookup"><span data-stu-id="eeb82-157">NOTES</span></span>

<span data-ttu-id="eeb82-158">別名</span><span class="sxs-lookup"><span data-stu-id="eeb82-158">ALIASES</span></span>

## <span data-ttu-id="eeb82-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="eeb82-159">RELATED LINKS</span></span>

