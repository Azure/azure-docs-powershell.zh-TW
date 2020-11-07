---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/get-azsbackupconfiguration
schema: 2.0.0
ms.openlocfilehash: 3a9fedc637f8400b952d823a98dfe0abaa1d40d3
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/24/2020
ms.locfileid: "93966800"
---
# <span data-ttu-id="e5e9d-101">Get-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5e9d-101">Get-AzsBackupConfiguration</span></span>

## <span data-ttu-id="e5e9d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e5e9d-102">SYNOPSIS</span></span>
<span data-ttu-id="e5e9d-103">根據名稱傳回特定的備份位置。</span><span class="sxs-lookup"><span data-stu-id="e5e9d-103">Returns a specific backup location based on name.</span></span>

## <span data-ttu-id="e5e9d-104">句法</span><span class="sxs-lookup"><span data-stu-id="e5e9d-104">SYNTAX</span></span>

### <span data-ttu-id="e5e9d-105">取得 (預設) </span><span class="sxs-lookup"><span data-stu-id="e5e9d-105">Get (Default)</span></span>
```
Get-AzsBackupConfiguration [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e5e9d-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e5e9d-106">GetViaIdentity</span></span>
```
Get-AzsBackupConfiguration -InputObject <IBackupAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="e5e9d-107">清單</span><span class="sxs-lookup"><span data-stu-id="e5e9d-107">List</span></span>
```
Get-AzsBackupConfiguration [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Skip <String>]
 [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e5e9d-108">說明</span><span class="sxs-lookup"><span data-stu-id="e5e9d-108">DESCRIPTION</span></span>
<span data-ttu-id="e5e9d-109">根據名稱傳回特定的備份位置。</span><span class="sxs-lookup"><span data-stu-id="e5e9d-109">Returns a specific backup location based on name.</span></span>

## <span data-ttu-id="e5e9d-110">示例</span><span class="sxs-lookup"><span data-stu-id="e5e9d-110">EXAMPLES</span></span>

### <span data-ttu-id="e5e9d-111">範例1： Get-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5e9d-111">Example 1: Get-AzsBackupConfiguration</span></span>
```powershell
PS C:\> Get-AzsBackupConfiguration

```

<span data-ttu-id="e5e9d-112">取得 Azure 堆疊備份設定。</span><span class="sxs-lookup"><span data-stu-id="e5e9d-112">Get Azure Stack backup configuration.</span></span>

## <span data-ttu-id="e5e9d-113">參數</span><span class="sxs-lookup"><span data-stu-id="e5e9d-113">PARAMETERS</span></span>

### <span data-ttu-id="e5e9d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5e9d-114">-DefaultProfile</span></span>
<span data-ttu-id="e5e9d-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e5e9d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5e9d-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5e9d-116">-InputObject</span></span>
<span data-ttu-id="e5e9d-117">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="e5e9d-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e5e9d-118">-位置</span><span class="sxs-lookup"><span data-stu-id="e5e9d-118">-Location</span></span>
<span data-ttu-id="e5e9d-119">備份位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5e9d-119">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e5e9d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5e9d-120">-ResourceGroupName</span></span>
<span data-ttu-id="e5e9d-121">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5e9d-121">Name of the resource group.</span></span>

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

### <span data-ttu-id="e5e9d-122">-略過</span><span class="sxs-lookup"><span data-stu-id="e5e9d-122">-Skip</span></span>
<span data-ttu-id="e5e9d-123">OData 略過參數。</span><span class="sxs-lookup"><span data-stu-id="e5e9d-123">OData skip parameter.</span></span>

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

### <span data-ttu-id="e5e9d-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e5e9d-124">-SubscriptionId</span></span>
<span data-ttu-id="e5e9d-125">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="e5e9d-125">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e5e9d-126">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="e5e9d-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e5e9d-127">-上方</span><span class="sxs-lookup"><span data-stu-id="e5e9d-127">-Top</span></span>
<span data-ttu-id="e5e9d-128">OData top 參數。</span><span class="sxs-lookup"><span data-stu-id="e5e9d-128">OData top parameter.</span></span>

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

### <span data-ttu-id="e5e9d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5e9d-129">CommonParameters</span></span>
<span data-ttu-id="e5e9d-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e5e9d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5e9d-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e5e9d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5e9d-132">輸入</span><span class="sxs-lookup"><span data-stu-id="e5e9d-132">INPUTS</span></span>

### <span data-ttu-id="e5e9d-133">IBackupAdminIdentity （BackupAdmin）的</span><span class="sxs-lookup"><span data-stu-id="e5e9d-133">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity</span></span>

## <span data-ttu-id="e5e9d-134">輸出</span><span class="sxs-lookup"><span data-stu-id="e5e9d-134">OUTPUTS</span></span>

### <span data-ttu-id="e5e9d-135">IBackupLocation （BackupAdmin）。 Api20180901。</span><span class="sxs-lookup"><span data-stu-id="e5e9d-135">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackupLocation</span></span>

## <span data-ttu-id="e5e9d-136">筆記</span><span class="sxs-lookup"><span data-stu-id="e5e9d-136">NOTES</span></span>

<span data-ttu-id="e5e9d-137">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="e5e9d-137">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e5e9d-138">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="e5e9d-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="e5e9d-139">INPUTOBJECT <IBackupAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="e5e9d-139">INPUTOBJECT <IBackupAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e5e9d-140">`[Backup <String>]`：備份的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5e9d-140">`[Backup <String>]`: Name of the backup.</span></span>
  - <span data-ttu-id="e5e9d-141">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="e5e9d-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e5e9d-142">`[Location <String>]`：備份位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5e9d-142">`[Location <String>]`: Name of the backup location.</span></span>
  - <span data-ttu-id="e5e9d-143">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5e9d-143">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="e5e9d-144">`[SubscriptionId <String>]`：唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="e5e9d-144">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e5e9d-145">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="e5e9d-145">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="e5e9d-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="e5e9d-146">RELATED LINKS</span></span>

