---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstorageaccount
schema: 2.0.0
ms.openlocfilehash: 0ddf99277834e69a55b009abcb4b683eebb7a4ec
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968100"
---
# <span data-ttu-id="d9206-101">Get-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d9206-101">Get-AzsStorageAccount</span></span>

## <span data-ttu-id="d9206-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d9206-102">SYNOPSIS</span></span>
<span data-ttu-id="d9206-103">傳回要求的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="d9206-103">Returns the requested storage account.</span></span>

## <span data-ttu-id="d9206-104">句法</span><span class="sxs-lookup"><span data-stu-id="d9206-104">SYNTAX</span></span>

### <span data-ttu-id="d9206-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="d9206-105">List (Default)</span></span>
```
Get-AzsStorageAccount [-Location <String>] [-SubscriptionId <String[]>] [-Filter <String>] [-Summary]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d9206-106">獲取</span><span class="sxs-lookup"><span data-stu-id="d9206-106">Get</span></span>
```
Get-AzsStorageAccount -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d9206-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d9206-107">GetViaIdentity</span></span>
```
Get-AzsStorageAccount -InputObject <IStorageAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d9206-108">說明</span><span class="sxs-lookup"><span data-stu-id="d9206-108">DESCRIPTION</span></span>
<span data-ttu-id="d9206-109">傳回要求的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="d9206-109">Returns the requested storage account.</span></span>

## <span data-ttu-id="d9206-110">示例</span><span class="sxs-lookup"><span data-stu-id="d9206-110">EXAMPLES</span></span>

### <span data-ttu-id="d9206-111">範例1：</span><span class="sxs-lookup"><span data-stu-id="d9206-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsStorageAccount -Summary
```

<span data-ttu-id="d9206-112">取得儲存帳戶清單 (摘要) 。</span><span class="sxs-lookup"><span data-stu-id="d9206-112">Get a list of storage accounts (summary).</span></span>

### <span data-ttu-id="d9206-113">範例2：</span><span class="sxs-lookup"><span data-stu-id="d9206-113">Example 2:</span></span>
```powershell
PS C:\> $storageAccount = Get-AzsStorageAccount
PS C:\> $storageAccount | Select Location,Name,AccountStatus,HealthState,Kind | ft
```

<span data-ttu-id="d9206-114">取得含詳細資料的儲存空間帳戶清單，並列印狀態。</span><span class="sxs-lookup"><span data-stu-id="d9206-114">Get a list of storage account with details and print the status.</span></span>

### <span data-ttu-id="d9206-115">範例3：</span><span class="sxs-lookup"><span data-stu-id="d9206-115">Example 3:</span></span>
```powershell
PS C:\> Get-AzsStorageAccount -Name 32cbc1173bde4e5fad04e11cc4cb2e00 | fl *
```

<span data-ttu-id="d9206-116">取得指定儲存空間帳戶的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d9206-116">Get details of the specified storage account.</span></span>

## <span data-ttu-id="d9206-117">參數</span><span class="sxs-lookup"><span data-stu-id="d9206-117">PARAMETERS</span></span>

### <span data-ttu-id="d9206-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9206-118">-DefaultProfile</span></span>
<span data-ttu-id="d9206-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d9206-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9206-120">-篩選</span><span class="sxs-lookup"><span data-stu-id="d9206-120">-Filter</span></span>
<span data-ttu-id="d9206-121">篩選字串</span><span class="sxs-lookup"><span data-stu-id="d9206-121">Filter string</span></span>

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

### <span data-ttu-id="d9206-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9206-122">-InputObject</span></span>
<span data-ttu-id="d9206-123">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="d9206-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="d9206-124">-位置</span><span class="sxs-lookup"><span data-stu-id="d9206-124">-Location</span></span>
<span data-ttu-id="d9206-125">資源位置。</span><span class="sxs-lookup"><span data-stu-id="d9206-125">Resource location.</span></span>

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

### <span data-ttu-id="d9206-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="d9206-126">-Name</span></span>
<span data-ttu-id="d9206-127">租使用者看不到的內部儲存空間帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="d9206-127">Internal storage account ID, which is not visible to tenant.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AccountId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d9206-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d9206-128">-SubscriptionId</span></span>
<span data-ttu-id="d9206-129">訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="d9206-129">Subscription Id.</span></span>

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

### <span data-ttu-id="d9206-130">-摘要</span><span class="sxs-lookup"><span data-stu-id="d9206-130">-Summary</span></span>
<span data-ttu-id="d9206-131">切換是否傳回摘要或詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="d9206-131">Switch for whether summary or detailed information is returned.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: $false
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d9206-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9206-132">CommonParameters</span></span>
<span data-ttu-id="d9206-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d9206-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9206-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d9206-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9206-135">輸入</span><span class="sxs-lookup"><span data-stu-id="d9206-135">INPUTS</span></span>

### <span data-ttu-id="d9206-136">IStorageAdminIdentity （StorageAdmin）的</span><span class="sxs-lookup"><span data-stu-id="d9206-136">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity</span></span>

## <span data-ttu-id="d9206-137">輸出</span><span class="sxs-lookup"><span data-stu-id="d9206-137">OUTPUTS</span></span>

### <span data-ttu-id="d9206-138">IStorageAccount （StorageAdmin）。 Api201908Preview。</span><span class="sxs-lookup"><span data-stu-id="d9206-138">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageAccount</span></span>



## <span data-ttu-id="d9206-139">筆記</span><span class="sxs-lookup"><span data-stu-id="d9206-139">NOTES</span></span>

<span data-ttu-id="d9206-140">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="d9206-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d9206-141">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="d9206-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="d9206-142">INPUTOBJECT <IStorageAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="d9206-142">INPUTOBJECT <IStorageAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d9206-143">`[AccountId <String>]`：租使用者看不到的內部儲存空間帳戶 ID。</span><span class="sxs-lookup"><span data-stu-id="d9206-143">`[AccountId <String>]`: Internal storage account ID, which is not visible to tenant.</span></span>
  - <span data-ttu-id="d9206-144">`[AsyncOperationId <String>]`：非同步作業 Id。</span><span class="sxs-lookup"><span data-stu-id="d9206-144">`[AsyncOperationId <String>]`: Async Operation Id.</span></span>
  - <span data-ttu-id="d9206-145">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="d9206-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d9206-146">`[Location <String>]`：資源位置。</span><span class="sxs-lookup"><span data-stu-id="d9206-146">`[Location <String>]`: Resource location.</span></span>
  - <span data-ttu-id="d9206-147">`[QuotaName <String>]`：儲存配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="d9206-147">`[QuotaName <String>]`: The name of the storage quota.</span></span>
  - <span data-ttu-id="d9206-148">`[ResourceGroup <String>]`：資源組名。</span><span class="sxs-lookup"><span data-stu-id="d9206-148">`[ResourceGroup <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="d9206-149">`[ServiceName <String>]`：儲存服務名稱。</span><span class="sxs-lookup"><span data-stu-id="d9206-149">`[ServiceName <String>]`: Storage service name.</span></span>
  - <span data-ttu-id="d9206-150">`[SubscriptionId <String>]`：訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="d9206-150">`[SubscriptionId <String>]`: Subscription Id.</span></span>

## <span data-ttu-id="d9206-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="d9206-151">RELATED LINKS</span></span>

