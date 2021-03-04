---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/powershell/module/az.support/get-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
ms.openlocfilehash: c5f68e947af383787b3ed1e7d9c9c3983c45769b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916461"
---
# <span data-ttu-id="7f57c-101">Get-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="7f57c-101">Get-AzSupportTicket</span></span>

## <span data-ttu-id="7f57c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7f57c-102">SYNOPSIS</span></span>
<span data-ttu-id="7f57c-103">取得支援票證。</span><span class="sxs-lookup"><span data-stu-id="7f57c-103">Get support tickets.</span></span>

## <span data-ttu-id="7f57c-104">語法</span><span class="sxs-lookup"><span data-stu-id="7f57c-104">SYNTAX</span></span>

### <span data-ttu-id="7f57c-105">ListParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7f57c-105">ListParameterSet (Default)</span></span>
```
Get-AzSupportTicket [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="7f57c-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f57c-106">GetByNameParameterSet</span></span>
```
Get-AzSupportTicket -Name <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="7f57c-107">描述</span><span class="sxs-lookup"><span data-stu-id="7f57c-107">DESCRIPTION</span></span>
<span data-ttu-id="7f57c-108">獲得支援票證清單。</span><span class="sxs-lookup"><span data-stu-id="7f57c-108">Gets the list of support tickets.</span></span> <span data-ttu-id="7f57c-109">如果您沒有指定任何參數，它會取回所有支援票證。</span><span class="sxs-lookup"><span data-stu-id="7f57c-109">It will retrieve all the support tickets if you do not specify any parameters.</span></span> <span data-ttu-id="7f57c-110">您也可以使用 Filter 參數，根據狀態或 CreatedDate 篩選支援票證。</span><span class="sxs-lookup"><span data-stu-id="7f57c-110">You can also filter the support tickets by Status or CreatedDate using the Filter parameter.</span></span> <span data-ttu-id="7f57c-111">以下是您可以指定的篩選值範例。</span><span class="sxs-lookup"><span data-stu-id="7f57c-111">Here are some examples of filter values that you can specify.</span></span>

| <span data-ttu-id="7f57c-112">場景</span><span class="sxs-lookup"><span data-stu-id="7f57c-112">Scenario</span></span>                                                         | <span data-ttu-id="7f57c-113">濾波器</span><span class="sxs-lookup"><span data-stu-id="7f57c-113">Filter</span></span>                                           |
|------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="7f57c-114">取得開啟狀態中的票證</span><span class="sxs-lookup"><span data-stu-id="7f57c-114">Get tickets that are in open state</span></span>                               | <span data-ttu-id="7f57c-115">"Status eq 'Open'"</span><span class="sxs-lookup"><span data-stu-id="7f57c-115">"Status eq 'Open'"</span></span>                               |
| <span data-ttu-id="7f57c-116">取得關閉狀態中的票證</span><span class="sxs-lookup"><span data-stu-id="7f57c-116">Get tickets that are in closed state</span></span>                             | <span data-ttu-id="7f57c-117">"Status eq 'Closed'"</span><span class="sxs-lookup"><span data-stu-id="7f57c-117">"Status eq 'Closed'"</span></span>                             |
| <span data-ttu-id="7f57c-118">取得 2019 年 12 月 20 日當天或之後所建立的票證</span><span class="sxs-lookup"><span data-stu-id="7f57c-118">Get tickets that were created on or after 20th Dec, 2019</span></span>         | <span data-ttu-id="7f57c-119">"CreatedDate ge 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="7f57c-119">"CreatedDate ge 2019-12-20"</span></span>                      |
| <span data-ttu-id="7f57c-120">取得 2019 年 12 月 20 日之後所建立票證</span><span class="sxs-lookup"><span data-stu-id="7f57c-120">Get tickets that were created after 20th Dec, 2019</span></span>               | <span data-ttu-id="7f57c-121">"CreatedDate gt 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="7f57c-121">"CreatedDate gt 2019-12-20"</span></span>                      |
| <span data-ttu-id="7f57c-122">在 2019 年 12 月 20 日之後建立並開啟的票證</span><span class="sxs-lookup"><span data-stu-id="7f57c-122">Gets tickets created after 20th Dec, 2019 that are in open state</span></span> | <span data-ttu-id="7f57c-123">"CreatedDate gt 2019-12-20 and Status eq 'Open'"</span><span class="sxs-lookup"><span data-stu-id="7f57c-123">"CreatedDate gt 2019-12-20 and Status eq 'Open'"</span></span> |


<span data-ttu-id="7f57c-124">此 Cmdlet 支援透過 First 和 Skip 參數分頁。</span><span class="sxs-lookup"><span data-stu-id="7f57c-124">This cmdlet supports paging via First and Skip parameters.</span></span>

<span data-ttu-id="7f57c-125">您也可以指定票證名稱，以取回單一支援票證。</span><span class="sxs-lookup"><span data-stu-id="7f57c-125">You can also retrieve a single support ticket by specifying the ticket name.</span></span> 

## <span data-ttu-id="7f57c-126">例子</span><span class="sxs-lookup"><span data-stu-id="7f57c-126">EXAMPLES</span></span>

### <span data-ttu-id="7f57c-127">範例 1：取得前 2 張票證</span><span class="sxs-lookup"><span data-stu-id="7f57c-127">Example 1: Get first 2 tickets</span></span>
```powershell
PS C:\> Get-AzSupportTicket -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="7f57c-128">範例 2：在略過前 2 個之後取得前 2 張票證</span><span class="sxs-lookup"><span data-stu-id="7f57c-128">Example 2: Get first 2 tickets after skipping the first 2</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Skip 2 -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test3 test title3                  150010521000314 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test4 test title4                  150010521000315 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="7f57c-129">範例 3：按名稱取得支援票證</span><span class="sxs-lookup"><span data-stu-id="7f57c-129">Example 3: Get a support ticket by name</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="7f57c-130">範例 4：取得根據狀態篩選的前 2 個支援票證</span><span class="sxs-lookup"><span data-stu-id="7f57c-130">Example 4: Get first 2 support tickets filtered by status</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Closed'" -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="7f57c-131">範例 5：取得所有在 2019 年 12 月 20 日之後開啟狀態且已建立的支援票證</span><span class="sxs-lookup"><span data-stu-id="7f57c-131">Example 5: Get all support tickets that are in Open state and created after Dec 20th, 2019</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Open' and CreatedDate gt 2019-12-20"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test6 test title6                  150010521000311 Minimal  Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
test7 test title7                  150010521000312 Minimal  Billing                       Open   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="7f57c-132">參數</span><span class="sxs-lookup"><span data-stu-id="7f57c-132">PARAMETERS</span></span>

### <span data-ttu-id="7f57c-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f57c-133">-DefaultProfile</span></span>
<span data-ttu-id="7f57c-134">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7f57c-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f57c-135">-篩選</span><span class="sxs-lookup"><span data-stu-id="7f57c-135">-Filter</span></span>
<span data-ttu-id="7f57c-136">要用於此 Cmdlet 結果的篩選。</span><span class="sxs-lookup"><span data-stu-id="7f57c-136">Filter to be applied to the results of this cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f57c-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="7f57c-137">-Name</span></span>
<span data-ttu-id="7f57c-138">此 Cmdlet 獲得的支援票證名稱。</span><span class="sxs-lookup"><span data-stu-id="7f57c-138">Name of support ticket that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f57c-139">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="7f57c-139">-IncludeTotalCount</span></span>
<span data-ttu-id="7f57c-140">以整數來報告資料集中物件 (個整數) 選取的物件。</span><span class="sxs-lookup"><span data-stu-id="7f57c-140">Reports the total number of objects in the data set (an integer) followed by the selected objects.</span></span>
<span data-ttu-id="7f57c-141">如果 Cmdlet 無法判斷總計，則會顯示「未知總數」。</span><span class="sxs-lookup"><span data-stu-id="7f57c-141">If the cmdlet cannot determine the total count, it displays "Unknown total count."</span></span> <span data-ttu-id="7f57c-142">整數具有指出總計數值可靠性的 Accuracy 屬性。</span><span class="sxs-lookup"><span data-stu-id="7f57c-142">The integer has an Accuracy property that indicates the reliability of the total count value.</span></span>
<span data-ttu-id="7f57c-143">精確度值的範圍從 0.0 到 1.0，其中 0.0 表示 Cmdlet 無法計算物件，1.0 表示計數精確，而介於 0.0 到 1.0 之間的值表示估計值越可靠。</span><span class="sxs-lookup"><span data-stu-id="7f57c-143">The value of Accuracy ranges from 0.0 to 1.0 where 0.0 means that the cmdlet could not count the objects, 1.0 means that the count is exact, and a value between 0.0 and 1.0 indicates an increasingly reliable estimate.</span></span>

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

### <span data-ttu-id="7f57c-144">-略過</span><span class="sxs-lookup"><span data-stu-id="7f57c-144">-Skip</span></span>
<span data-ttu-id="7f57c-145">忽略指定的物件數目，然後獲得其餘的物件。</span><span class="sxs-lookup"><span data-stu-id="7f57c-145">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="7f57c-146">輸入要略過的物件數目。</span><span class="sxs-lookup"><span data-stu-id="7f57c-146">Enter the number of objects to skip.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f57c-147">-第一個</span><span class="sxs-lookup"><span data-stu-id="7f57c-147">-First</span></span>
<span data-ttu-id="7f57c-148">只獲得指定的物件數目。</span><span class="sxs-lookup"><span data-stu-id="7f57c-148">Gets only the specified number of objects.</span></span>
<span data-ttu-id="7f57c-149">輸入要取得的物件數目。</span><span class="sxs-lookup"><span data-stu-id="7f57c-149">Enter the number of objects to get.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f57c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f57c-150">CommonParameters</span></span>
<span data-ttu-id="7f57c-151">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7f57c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f57c-152">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f57c-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f57c-153">輸入</span><span class="sxs-lookup"><span data-stu-id="7f57c-153">INPUTS</span></span>

### <span data-ttu-id="7f57c-154">沒有</span><span class="sxs-lookup"><span data-stu-id="7f57c-154">None</span></span>

## <span data-ttu-id="7f57c-155">輸出</span><span class="sxs-lookup"><span data-stu-id="7f57c-155">OUTPUTS</span></span>

### <span data-ttu-id="7f57c-156">Microsoft.Azure.Commands.support.models.PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="7f57c-156">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="7f57c-157">筆記</span><span class="sxs-lookup"><span data-stu-id="7f57c-157">NOTES</span></span>

## <span data-ttu-id="7f57c-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="7f57c-158">RELATED LINKS</span></span>
