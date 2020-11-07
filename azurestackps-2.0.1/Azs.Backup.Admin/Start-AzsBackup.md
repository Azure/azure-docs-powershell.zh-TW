---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/start-azsbackup
schema: 2.0.0
ms.openlocfilehash: 37fc3ddb1c878bc8b6b1e14d920a5747edce0cd3
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/24/2020
ms.locfileid: "93966796"
---
# <span data-ttu-id="8f406-101">Start-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="8f406-101">Start-AzsBackup</span></span>

## <span data-ttu-id="8f406-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8f406-102">SYNOPSIS</span></span>
<span data-ttu-id="8f406-103">備份特定位置。</span><span class="sxs-lookup"><span data-stu-id="8f406-103">Back up a specific location.</span></span>

## <span data-ttu-id="8f406-104">句法</span><span class="sxs-lookup"><span data-stu-id="8f406-104">SYNTAX</span></span>

### <span data-ttu-id="8f406-105">建立 (預設) </span><span class="sxs-lookup"><span data-stu-id="8f406-105">Create (Default)</span></span>
```
Start-AzsBackup [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8f406-106">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8f406-106">CreateViaIdentity</span></span>
```
Start-AzsBackup -InputObject <IBackupAdminIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8f406-107">說明</span><span class="sxs-lookup"><span data-stu-id="8f406-107">DESCRIPTION</span></span>
<span data-ttu-id="8f406-108">備份特定位置。</span><span class="sxs-lookup"><span data-stu-id="8f406-108">Back up a specific location.</span></span>

## <span data-ttu-id="8f406-109">示例</span><span class="sxs-lookup"><span data-stu-id="8f406-109">EXAMPLES</span></span>

### <span data-ttu-id="8f406-110">範例1：開始 azurestack 備份</span><span class="sxs-lookup"><span data-stu-id="8f406-110">Example 1: Start azurestack backup</span></span>
```powershell
PS C:\>Start-AzsBackup

```

<span data-ttu-id="8f406-111">啟動 Azure 堆疊備份。</span><span class="sxs-lookup"><span data-stu-id="8f406-111">Start an Azure Stack backup.</span></span>

## <span data-ttu-id="8f406-112">參數</span><span class="sxs-lookup"><span data-stu-id="8f406-112">PARAMETERS</span></span>

### <span data-ttu-id="8f406-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8f406-113">-AsJob</span></span>
<span data-ttu-id="8f406-114">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="8f406-114">Run the command as a job</span></span>

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

### <span data-ttu-id="8f406-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f406-115">-DefaultProfile</span></span>
<span data-ttu-id="8f406-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8f406-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f406-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f406-117">-InputObject</span></span>
<span data-ttu-id="8f406-118">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="8f406-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity
Parameter Sets: CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="8f406-119">-位置</span><span class="sxs-lookup"><span data-stu-id="8f406-119">-Location</span></span>
<span data-ttu-id="8f406-120">備份位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="8f406-120">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: Create
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8f406-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8f406-121">-NoWait</span></span>
<span data-ttu-id="8f406-122">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="8f406-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8f406-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f406-123">-ResourceGroupName</span></span>
<span data-ttu-id="8f406-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8f406-124">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Create
Aliases:

Required: False
Position: Named
Default value: "system.$((Get-AzLocation)[0].Location)"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8f406-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8f406-125">-SubscriptionId</span></span>
<span data-ttu-id="8f406-126">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="8f406-126">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8f406-127">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="8f406-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Create
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8f406-128">-確認</span><span class="sxs-lookup"><span data-stu-id="8f406-128">-Confirm</span></span>
<span data-ttu-id="8f406-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8f406-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f406-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f406-130">-WhatIf</span></span>
<span data-ttu-id="8f406-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8f406-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f406-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8f406-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f406-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f406-133">CommonParameters</span></span>
<span data-ttu-id="8f406-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8f406-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f406-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8f406-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f406-136">輸入</span><span class="sxs-lookup"><span data-stu-id="8f406-136">INPUTS</span></span>

### <span data-ttu-id="8f406-137">IBackupAdminIdentity （BackupAdmin）的</span><span class="sxs-lookup"><span data-stu-id="8f406-137">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity</span></span>

## <span data-ttu-id="8f406-138">輸出</span><span class="sxs-lookup"><span data-stu-id="8f406-138">OUTPUTS</span></span>

### <span data-ttu-id="8f406-139">IBackup （BackupAdmin）。 Api20180901。</span><span class="sxs-lookup"><span data-stu-id="8f406-139">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackup</span></span>



## <span data-ttu-id="8f406-140">筆記</span><span class="sxs-lookup"><span data-stu-id="8f406-140">NOTES</span></span>

<span data-ttu-id="8f406-141">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="8f406-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8f406-142">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="8f406-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="8f406-143">INPUTOBJECT <IBackupAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="8f406-143">INPUTOBJECT <IBackupAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8f406-144">`[Backup <String>]`：備份的名稱。</span><span class="sxs-lookup"><span data-stu-id="8f406-144">`[Backup <String>]`: Name of the backup.</span></span>
  - <span data-ttu-id="8f406-145">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="8f406-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8f406-146">`[Location <String>]`：備份位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="8f406-146">`[Location <String>]`: Name of the backup location.</span></span>
  - <span data-ttu-id="8f406-147">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8f406-147">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="8f406-148">`[SubscriptionId <String>]`：唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="8f406-148">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8f406-149">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="8f406-149">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="8f406-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="8f406-150">RELATED LINKS</span></span>

