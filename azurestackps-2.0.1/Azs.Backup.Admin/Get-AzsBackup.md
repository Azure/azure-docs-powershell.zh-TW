---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/get-azsbackup
schema: 2.0.0
ms.openlocfilehash: 2c2d517da3be62ff407ca17577edefcf7322ad55
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/24/2020
ms.locfileid: "93966801"
---
# <span data-ttu-id="390b4-101">Get-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="390b4-101">Get-AzsBackup</span></span>

## <span data-ttu-id="390b4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="390b4-102">SYNOPSIS</span></span>
<span data-ttu-id="390b4-103">從以名稱為基礎的位置傳回備份。</span><span class="sxs-lookup"><span data-stu-id="390b4-103">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="390b4-104">句法</span><span class="sxs-lookup"><span data-stu-id="390b4-104">SYNTAX</span></span>

### <span data-ttu-id="390b4-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="390b4-105">List (Default)</span></span>
```
Get-AzsBackup [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Skip <String>]
 [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="390b4-106">獲取</span><span class="sxs-lookup"><span data-stu-id="390b4-106">Get</span></span>
```
Get-AzsBackup -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="390b4-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="390b4-107">GetViaIdentity</span></span>
```
Get-AzsBackup -InputObject <IBackupAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="390b4-108">說明</span><span class="sxs-lookup"><span data-stu-id="390b4-108">DESCRIPTION</span></span>
<span data-ttu-id="390b4-109">從以名稱為基礎的位置傳回備份。</span><span class="sxs-lookup"><span data-stu-id="390b4-109">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="390b4-110">示例</span><span class="sxs-lookup"><span data-stu-id="390b4-110">EXAMPLES</span></span>

### <span data-ttu-id="390b4-111">範例1：清單備份</span><span class="sxs-lookup"><span data-stu-id="390b4-111">Example 1: List Backups</span></span>
```powershell
PS C:\> Get-AzsBackup

```

<span data-ttu-id="390b4-112">取得所有 Azure 堆疊備份的資訊 sbout。</span><span class="sxs-lookup"><span data-stu-id="390b4-112">Get information sbout all Azure Stack backups.</span></span>

### <span data-ttu-id="390b4-113">範例2：取得特定的備份</span><span class="sxs-lookup"><span data-stu-id="390b4-113">Example 2: Get specific backup</span></span>
```powershell
PS C:\> Get-AzsBackup -Name 'backupName'

```

<span data-ttu-id="390b4-114">取得指定 Azure 堆疊備份的資訊。</span><span class="sxs-lookup"><span data-stu-id="390b4-114">Get information for the the specified Azure Stack backup.</span></span>

## <span data-ttu-id="390b4-115">參數</span><span class="sxs-lookup"><span data-stu-id="390b4-115">PARAMETERS</span></span>

### <span data-ttu-id="390b4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="390b4-116">-DefaultProfile</span></span>
<span data-ttu-id="390b4-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="390b4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="390b4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="390b4-118">-InputObject</span></span>
<span data-ttu-id="390b4-119">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="390b4-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="390b4-120">-位置</span><span class="sxs-lookup"><span data-stu-id="390b4-120">-Location</span></span>
<span data-ttu-id="390b4-121">備份位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="390b4-121">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="390b4-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="390b4-122">-Name</span></span>
<span data-ttu-id="390b4-123">備份的名稱。</span><span class="sxs-lookup"><span data-stu-id="390b4-123">Name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="390b4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="390b4-124">-ResourceGroupName</span></span>
<span data-ttu-id="390b4-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="390b4-125">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: "system.$((Get-AzLocation)[0].Location)"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="390b4-126">-略過</span><span class="sxs-lookup"><span data-stu-id="390b4-126">-Skip</span></span>
<span data-ttu-id="390b4-127">OData 略過參數。</span><span class="sxs-lookup"><span data-stu-id="390b4-127">OData skip parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="390b4-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="390b4-128">-SubscriptionId</span></span>
<span data-ttu-id="390b4-129">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="390b4-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="390b4-130">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="390b4-130">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="390b4-131">-上方</span><span class="sxs-lookup"><span data-stu-id="390b4-131">-Top</span></span>
<span data-ttu-id="390b4-132">OData top 參數。</span><span class="sxs-lookup"><span data-stu-id="390b4-132">OData top parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="390b4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="390b4-133">CommonParameters</span></span>
<span data-ttu-id="390b4-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="390b4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="390b4-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="390b4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="390b4-136">輸入</span><span class="sxs-lookup"><span data-stu-id="390b4-136">INPUTS</span></span>

### <span data-ttu-id="390b4-137">IBackupAdminIdentity （BackupAdmin）的</span><span class="sxs-lookup"><span data-stu-id="390b4-137">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity</span></span>

## <span data-ttu-id="390b4-138">輸出</span><span class="sxs-lookup"><span data-stu-id="390b4-138">OUTPUTS</span></span>

### <span data-ttu-id="390b4-139">IBackup （BackupAdmin）。 Api20180901。</span><span class="sxs-lookup"><span data-stu-id="390b4-139">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackup</span></span>



## <span data-ttu-id="390b4-140">筆記</span><span class="sxs-lookup"><span data-stu-id="390b4-140">NOTES</span></span>

<span data-ttu-id="390b4-141">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="390b4-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="390b4-142">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="390b4-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="390b4-143">INPUTOBJECT <IBackupAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="390b4-143">INPUTOBJECT <IBackupAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="390b4-144">`[Backup <String>]`：備份的名稱。</span><span class="sxs-lookup"><span data-stu-id="390b4-144">`[Backup <String>]`: Name of the backup.</span></span>
  - <span data-ttu-id="390b4-145">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="390b4-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="390b4-146">`[Location <String>]`：備份位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="390b4-146">`[Location <String>]`: Name of the backup location.</span></span>
  - <span data-ttu-id="390b4-147">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="390b4-147">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="390b4-148">`[SubscriptionId <String>]`：唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="390b4-148">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="390b4-149">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="390b4-149">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="390b4-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="390b4-150">RELATED LINKS</span></span>

