---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServer.md
ms.openlocfilehash: 1dbd998cdafc92de6541e25c2cb2bf6477e2d5b2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98275067"
---
# <span data-ttu-id="be520-101">New-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="be520-101">New-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="be520-102">摘要</span><span class="sxs-lookup"><span data-stu-id="be520-102">SYNOPSIS</span></span>
<span data-ttu-id="be520-103">建立新的 MySQL 靈活伺服器</span><span class="sxs-lookup"><span data-stu-id="be520-103">Creates a new MySQL flexible server</span></span>

## <span data-ttu-id="be520-104">句法</span><span class="sxs-lookup"><span data-stu-id="be520-104">SYNTAX</span></span>

```
New-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String>
 -AdministratorLoginPassword <SecureString> -AdministratorUserName <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-Location <String>] [-Sku <String>] [-SkuTier <String>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="be520-105">說明</span><span class="sxs-lookup"><span data-stu-id="be520-105">DESCRIPTION</span></span>
<span data-ttu-id="be520-106">建立新的伺服器。</span><span class="sxs-lookup"><span data-stu-id="be520-106">Creates a new server.</span></span>

## <span data-ttu-id="be520-107">示例</span><span class="sxs-lookup"><span data-stu-id="be520-107">EXAMPLES</span></span>

### <span data-ttu-id="be520-108">範例1：建立新的 MySql 靈活伺服器</span><span class="sxs-lookup"><span data-stu-id="be520-108">Example 1: Create a new MySql flexible server</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest \
-Location eastus -AdministratorUserName mysqltest -AdministratorLoginPassword $password -Sku Standard_B1ms -SkuTier Burstable -Version 12 -StorageInMb 10240

Name            Location AdministratorLogin Version StorageProfileStorageMb SkuName         SkuTier     
----            -------- ------------------ ------- ----------------------- ------------    -------------        
mysql-test      West US 2   mysqltest    5.7      10240                  Standard_B1ms   Burstable
```



### <span data-ttu-id="be520-109">範例2：使用預設設定建立新的 MySql 彈性伺服器</span><span class="sxs-lookup"><span data-stu-id="be520-109">Example 2: Create a new MySql flexible server with default setting</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest \
-AdministratorUserName mysqltest -AdministratorLoginPassword $password

Name            Location AdministratorLogin Version StorageProfileStorageMb SkuName         SkuTier     
----            -------- ------------------ ------- ----------------------- ------------    -------------        
mysql-test      West US 2   mysqltest    5.7      131072                  Standard_B1ms   Burstable
```

<span data-ttu-id="be520-110">使用預設值建立 MySql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="be520-110">Create MySql server with default values.</span></span>
<span data-ttu-id="be520-111">[地點] 的預設值是 [西部美國 2]、Sku 為 Standard_B1ms、Sku 層是 Burstable，而 [儲存空間大小] 是10GiB。</span><span class="sxs-lookup"><span data-stu-id="be520-111">The default values of location is West US 2, Sku is Standard_B1ms, Sku tier is Burstable, and storage size is 10GiB.</span></span>

## <span data-ttu-id="be520-112">參數</span><span class="sxs-lookup"><span data-stu-id="be520-112">PARAMETERS</span></span>

### <span data-ttu-id="be520-113">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="be520-113">-AdministratorLoginPassword</span></span>
<span data-ttu-id="be520-114">系統管理員的密碼。</span><span class="sxs-lookup"><span data-stu-id="be520-114">The password of the administrator.</span></span>
<span data-ttu-id="be520-115">最少8個字元和最大的128個字元。</span><span class="sxs-lookup"><span data-stu-id="be520-115">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="be520-116">密碼必須包含下列其中三種類別的字元：英文大寫字母、英文小寫字母、數位和非數位元字元。</span><span class="sxs-lookup"><span data-stu-id="be520-116">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

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

### <span data-ttu-id="be520-117">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="be520-117">-AdministratorUserName</span></span>
<span data-ttu-id="be520-118">伺服器的系統管理員使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="be520-118">Administrator username for the server.</span></span>
<span data-ttu-id="be520-119">一旦設定，就無法變更。</span><span class="sxs-lookup"><span data-stu-id="be520-119">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="be520-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="be520-120">-AsJob</span></span>
<span data-ttu-id="be520-121">執行命令做為作業。</span><span class="sxs-lookup"><span data-stu-id="be520-121">Run the command as a job.</span></span>

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

### <span data-ttu-id="be520-122">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="be520-122">-BackupRetentionDay</span></span>
<span data-ttu-id="be520-123">伺服器的備份保留天數。</span><span class="sxs-lookup"><span data-stu-id="be520-123">Backup retention days for the server.</span></span>
<span data-ttu-id="be520-124">日算在7到35。</span><span class="sxs-lookup"><span data-stu-id="be520-124">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="be520-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be520-125">-DefaultProfile</span></span>
<span data-ttu-id="be520-126">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="be520-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be520-127">-位置</span><span class="sxs-lookup"><span data-stu-id="be520-127">-Location</span></span>
<span data-ttu-id="be520-128">資源所在的位置。</span><span class="sxs-lookup"><span data-stu-id="be520-128">The location the resource resides in.</span></span>

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

### <span data-ttu-id="be520-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="be520-129">-Name</span></span>
<span data-ttu-id="be520-130">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="be520-130">The name of the server.</span></span>

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

### <span data-ttu-id="be520-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="be520-131">-NoWait</span></span>
<span data-ttu-id="be520-132">以非同步方式執行命令。</span><span class="sxs-lookup"><span data-stu-id="be520-132">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="be520-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be520-133">-ResourceGroupName</span></span>
<span data-ttu-id="be520-134">包含資源之資源群組的名稱，您可以從 Azure 資源管理員 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="be520-134">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="be520-135">-Sku</span><span class="sxs-lookup"><span data-stu-id="be520-135">-Sku</span></span>
<span data-ttu-id="be520-136">Sku 的名稱，通常是 [層 + 家庭 + 核心]，例如 Standard_B1ms、Standard_D2ds_v4。</span><span class="sxs-lookup"><span data-stu-id="be520-136">The name of the sku, typically, tier + family + cores, e.g. Standard_B1ms, Standard_D2ds_v4.</span></span>

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

### <span data-ttu-id="be520-137">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="be520-137">-SkuTier</span></span>
<span data-ttu-id="be520-138">計算伺服器的層級。</span><span class="sxs-lookup"><span data-stu-id="be520-138">Compute tier of the server.</span></span>
<span data-ttu-id="be520-139">已接受的值： Burstable、GeneralPurpose、記憶體已優化。</span><span class="sxs-lookup"><span data-stu-id="be520-139">Accepted values: Burstable, GeneralPurpose, Memory Optimized.</span></span>
<span data-ttu-id="be520-140">預設值： Burstable。</span><span class="sxs-lookup"><span data-stu-id="be520-140">Default: Burstable.</span></span>

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

### <span data-ttu-id="be520-141">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="be520-141">-StorageInMb</span></span>
<span data-ttu-id="be520-142">伺服器允許的最大儲存空間。</span><span class="sxs-lookup"><span data-stu-id="be520-142">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="be520-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="be520-143">-SubscriptionId</span></span>
<span data-ttu-id="be520-144">識別 Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="be520-144">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="be520-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="be520-145">-Tag</span></span>
<span data-ttu-id="be520-146">以鍵值對形式的特定應用程式中繼資料。</span><span class="sxs-lookup"><span data-stu-id="be520-146">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="be520-147">-版本</span><span class="sxs-lookup"><span data-stu-id="be520-147">-Version</span></span>
<span data-ttu-id="be520-148">伺服器版本。</span><span class="sxs-lookup"><span data-stu-id="be520-148">Server version.</span></span>

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

### <span data-ttu-id="be520-149">-確認</span><span class="sxs-lookup"><span data-stu-id="be520-149">-Confirm</span></span>
<span data-ttu-id="be520-150">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="be520-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be520-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be520-151">-WhatIf</span></span>
<span data-ttu-id="be520-152">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="be520-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be520-153">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="be520-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be520-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be520-154">CommonParameters</span></span>
<span data-ttu-id="be520-155">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="be520-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be520-156">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="be520-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be520-157">輸入</span><span class="sxs-lookup"><span data-stu-id="be520-157">INPUTS</span></span>

## <span data-ttu-id="be520-158">輸出</span><span class="sxs-lookup"><span data-stu-id="be520-158">OUTPUTS</span></span>

### <span data-ttu-id="be520-159">IServerAutoGenerated 中的 Api20200701Preview （）。</span><span class="sxs-lookup"><span data-stu-id="be520-159">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="be520-160">筆記</span><span class="sxs-lookup"><span data-stu-id="be520-160">NOTES</span></span>

<span data-ttu-id="be520-161">別名</span><span class="sxs-lookup"><span data-stu-id="be520-161">ALIASES</span></span>

## <span data-ttu-id="be520-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="be520-162">RELATED LINKS</span></span>

