---
external help file: ''
Module Name: Azs.Gallery.Admin
online version: https://docs.microsoft.com/powershell/module/azs.gallery.admin/remove-azsgalleryitem
schema: 2.0.0
ms.openlocfilehash: c39a6cd64f48a7d8d6657499357daa1dd70fc091
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794888"
---
# <span data-ttu-id="b0503-101">Remove-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="b0503-101">Remove-AzsGalleryItem</span></span>

## <span data-ttu-id="b0503-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b0503-102">SYNOPSIS</span></span>
<span data-ttu-id="b0503-103">刪除特定的圖庫專案。</span><span class="sxs-lookup"><span data-stu-id="b0503-103">Delete a specific gallery item.</span></span>

## <span data-ttu-id="b0503-104">句法</span><span class="sxs-lookup"><span data-stu-id="b0503-104">SYNTAX</span></span>

### <span data-ttu-id="b0503-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="b0503-105">Delete (Default)</span></span>
```
Remove-AzsGalleryItem -Name <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b0503-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b0503-106">DeleteViaIdentity</span></span>
```
Remove-AzsGalleryItem -InputObject <IGalleryIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b0503-107">說明</span><span class="sxs-lookup"><span data-stu-id="b0503-107">DESCRIPTION</span></span>
<span data-ttu-id="b0503-108">刪除特定的圖庫專案。</span><span class="sxs-lookup"><span data-stu-id="b0503-108">Delete a specific gallery item.</span></span>

## <span data-ttu-id="b0503-109">示例</span><span class="sxs-lookup"><span data-stu-id="b0503-109">EXAMPLES</span></span>

### <span data-ttu-id="b0503-110">範例1： Remove-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="b0503-110">Example 1: Remove-AzsGalleryItem</span></span>
```powershell
PS C:\> Remove-AzsGalleryItem -Name TestUbuntu.Test.1.0.0

```

<span data-ttu-id="b0503-111">從 Azure 堆疊圖庫刪除 TestUbuntu. 1.0.0。</span><span class="sxs-lookup"><span data-stu-id="b0503-111">Deletes TestUbuntu.Test.1.0.0 from Azure Stack gallery.</span></span>

### <span data-ttu-id="b0503-112">範例2：透過管線 Remove-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="b0503-112">Example 2: Remove-AzsGalleryItem through pipeline</span></span>
```powershell
PS C:\> Get-AzsGalleryItem -Name TestUbuntu.Test.1.0.0 | Remove-AzsGalleryItem

```

<span data-ttu-id="b0503-113">刪除 TestUbuntu. 1.0.0 到管線。</span><span class="sxs-lookup"><span data-stu-id="b0503-113">Deletes TestUbuntu.Test.1.0.0 through pipeline.</span></span>

## <span data-ttu-id="b0503-114">參數</span><span class="sxs-lookup"><span data-stu-id="b0503-114">PARAMETERS</span></span>

### <span data-ttu-id="b0503-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0503-115">-DefaultProfile</span></span>
<span data-ttu-id="b0503-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b0503-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0503-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0503-117">-InputObject</span></span>
<span data-ttu-id="b0503-118">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b0503-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.IGalleryIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="b0503-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="b0503-119">-Name</span></span>
<span data-ttu-id="b0503-120">圖庫專案的身分識別。</span><span class="sxs-lookup"><span data-stu-id="b0503-120">Identity of the gallery item.</span></span>
<span data-ttu-id="b0503-121">包括發行者名稱、專案名稱，並且可能包含以句點字元分隔的版本。</span><span class="sxs-lookup"><span data-stu-id="b0503-121">Includes publisher name, item name, and may include version separated by period character.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: GalleryItemName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b0503-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b0503-122">-PassThru</span></span>
<span data-ttu-id="b0503-123">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="b0503-123">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b0503-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b0503-124">-SubscriptionId</span></span>
<span data-ttu-id="b0503-125">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="b0503-125">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b0503-126">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="b0503-126">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b0503-127">-確認</span><span class="sxs-lookup"><span data-stu-id="b0503-127">-Confirm</span></span>
<span data-ttu-id="b0503-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b0503-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0503-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0503-129">-WhatIf</span></span>
<span data-ttu-id="b0503-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b0503-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0503-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b0503-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0503-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0503-132">CommonParameters</span></span>
<span data-ttu-id="b0503-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b0503-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0503-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b0503-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0503-135">輸入</span><span class="sxs-lookup"><span data-stu-id="b0503-135">INPUTS</span></span>

### <span data-ttu-id="b0503-136">[IGalleryIdentity] 的圖庫。</span><span class="sxs-lookup"><span data-stu-id="b0503-136">Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.IGalleryIdentity</span></span>

## <span data-ttu-id="b0503-137">輸出</span><span class="sxs-lookup"><span data-stu-id="b0503-137">OUTPUTS</span></span>

### <span data-ttu-id="b0503-138">System.object</span><span class="sxs-lookup"><span data-stu-id="b0503-138">System.Boolean</span></span>



## <span data-ttu-id="b0503-139">筆記</span><span class="sxs-lookup"><span data-stu-id="b0503-139">NOTES</span></span>

<span data-ttu-id="b0503-140">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="b0503-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b0503-141">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="b0503-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="b0503-142">INPUTOBJECT <IGalleryIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="b0503-142">INPUTOBJECT <IGalleryIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b0503-143">`[GalleryItemName <String>]`：圖庫專案的身分識別。</span><span class="sxs-lookup"><span data-stu-id="b0503-143">`[GalleryItemName <String>]`: Identity of the gallery item.</span></span> <span data-ttu-id="b0503-144">包括發行者名稱、專案名稱，並且可能包含以句點字元分隔的版本。</span><span class="sxs-lookup"><span data-stu-id="b0503-144">Includes publisher name, item name, and may include version separated by period character.</span></span>
  - <span data-ttu-id="b0503-145">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="b0503-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b0503-146">`[SubscriptionId <String>]`：唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="b0503-146">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b0503-147">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="b0503-147">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="b0503-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="b0503-148">RELATED LINKS</span></span>

