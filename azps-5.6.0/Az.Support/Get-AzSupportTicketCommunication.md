---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/powershell/module/az.support/get-azsupportticketcommunication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
ms.openlocfilehash: 106ee61629c1252300d63ca686848ba7cc926cea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909401"
---
# <span data-ttu-id="8624e-101">Get-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="8624e-101">Get-AzSupportTicketCommunication</span></span>

## <span data-ttu-id="8624e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8624e-102">SYNOPSIS</span></span>
<span data-ttu-id="8624e-103">取得支援票證通訊。</span><span class="sxs-lookup"><span data-stu-id="8624e-103">Get support ticket communications.</span></span>

## <span data-ttu-id="8624e-104">語法</span><span class="sxs-lookup"><span data-stu-id="8624e-104">SYNTAX</span></span>

### <span data-ttu-id="8624e-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8624e-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSupportTicketCommunication -SupportTicketName <String> [-Name <String>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

### <span data-ttu-id="8624e-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8624e-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSupportTicketCommunication [-Name <String>] -SupportTicketObject <PSSupportTicket> [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

## <span data-ttu-id="8624e-107">描述</span><span class="sxs-lookup"><span data-stu-id="8624e-107">DESCRIPTION</span></span>
<span data-ttu-id="8624e-108">獲得支援票證的通訊。</span><span class="sxs-lookup"><span data-stu-id="8624e-108">Gets communications for a support ticket.</span></span> <span data-ttu-id="8624e-109">如果您沒有指定任何其他參數，它會針對票證取回所有通訊。</span><span class="sxs-lookup"><span data-stu-id="8624e-109">It will retrieve all the communications for a ticket if you do not specify any other parameters.</span></span> <span data-ttu-id="8624e-110">您也可以使用 Filter 參數，根據 CreatedDate 或 CommunicationType 篩選通訊。</span><span class="sxs-lookup"><span data-stu-id="8624e-110">You can also filter the communications by CreatedDate or CommunicationType using the Filter parameter.</span></span> <span data-ttu-id="8624e-111">以下是您可以指定的篩選值範例。</span><span class="sxs-lookup"><span data-stu-id="8624e-111">Here are some examples of filter values that you can specify.</span></span>


| <span data-ttu-id="8624e-112">場景</span><span class="sxs-lookup"><span data-stu-id="8624e-112">Scenario</span></span>                                                        | <span data-ttu-id="8624e-113">濾波器</span><span class="sxs-lookup"><span data-stu-id="8624e-113">Filter</span></span>                                                     |
|-----------------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="8624e-114">取得 Web 通訊</span><span class="sxs-lookup"><span data-stu-id="8624e-114">Get Web communications</span></span>                                          | <span data-ttu-id="8624e-115">"CommunicationType eq 'Web'"</span><span class="sxs-lookup"><span data-stu-id="8624e-115">"CommunicationType eq 'Web'"</span></span>                               |
| <span data-ttu-id="8624e-116">取得電話通訊</span><span class="sxs-lookup"><span data-stu-id="8624e-116">Get Phone communications</span></span>                                        | <span data-ttu-id="8624e-117">"CommunicationType eq 'Phone'"</span><span class="sxs-lookup"><span data-stu-id="8624e-117">"CommunicationType eq 'Phone'"</span></span>                             |
| <span data-ttu-id="8624e-118">取得 2019 年 12 月 20 日當天或之後建立的溝通</span><span class="sxs-lookup"><span data-stu-id="8624e-118">Get communications that were created on or after 20th Dec, 2019</span></span> | <span data-ttu-id="8624e-119">"CreatedDate ge 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="8624e-119">"CreatedDate ge 2019-12-20"</span></span>                                |
| <span data-ttu-id="8624e-120">取得 2019 年 12 月 20 日之後建立的溝通</span><span class="sxs-lookup"><span data-stu-id="8624e-120">Get communications that were created after 20th Dec, 2019</span></span>       | <span data-ttu-id="8624e-121">"CreatedDate gt 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="8624e-121">"CreatedDate gt 2019-12-20"</span></span>                                |
| <span data-ttu-id="8624e-122">在 2019 年 12 月 20 日之後建立 Web 通訊</span><span class="sxs-lookup"><span data-stu-id="8624e-122">Gets Web communications created after 20th Dec, 2019</span></span>            | <span data-ttu-id="8624e-123">"CreatedDate gt 2019-12-20 and CommunicationType eq 'Web'"</span><span class="sxs-lookup"><span data-stu-id="8624e-123">"CreatedDate gt 2019-12-20 and CommunicationType eq 'Web'"</span></span> |


<span data-ttu-id="8624e-124">此 Cmdlet 支援透過 First 和 Skip 參數分頁。</span><span class="sxs-lookup"><span data-stu-id="8624e-124">This cmdlet supports paging via First and Skip parameters.</span></span>

<span data-ttu-id="8624e-125">您也可以指定通訊名稱，以取回單一支援票證通訊。</span><span class="sxs-lookup"><span data-stu-id="8624e-125">You can also retrieve a single support ticket communication by specifying the communication name.</span></span> 

## <span data-ttu-id="8624e-126">例子</span><span class="sxs-lookup"><span data-stu-id="8624e-126">EXAMPLES</span></span>

### <span data-ttu-id="8624e-127">範例 1：取回支援票證的所有通訊</span><span class="sxs-lookup"><span data-stu-id="8624e-127">Example 1: Retrieve all communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
```

### <span data-ttu-id="8624e-128">範例 2：根據支援票證的名稱來取回單一通訊</span><span class="sxs-lookup"><span data-stu-id="8624e-128">Example 2: Retrieve a single communication by it's name for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Name "testmessage1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage1 user@contoso.com     test message   2/4/2020 9:38:14 PM
```

### <span data-ttu-id="8624e-129">範例 3：為支援票證取回前 2 個通訊</span><span class="sxs-lookup"><span data-stu-id="8624e-129">Example 3: Retrieve first 2 communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="8624e-130">範例 4：在跳過支援票證的前 2 個通訊之後，再取回下 2 個通訊</span><span class="sxs-lookup"><span data-stu-id="8624e-130">Example 4: Retrieve next 2 communications after skipping first 2 communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Skip 2 -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage4 user@contoso.com     test message4  2/4/2020 9:38:14 PM
testmessage5 user@contoso.com     test message5  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="8624e-131">範例 5：取回支援票證的所有 Web 通訊</span><span class="sxs-lookup"><span data-stu-id="8624e-131">Example 5: Retrieve all Web communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web'"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="8624e-132">範例 6：針對支援票證，在 2019 年 12 月 20 日當天或之後建立的所有通訊</span><span class="sxs-lookup"><span data-stu-id="8624e-132">Example 6: Retrieve all communications created on or after Dec 20th, 2019 for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="8624e-133">範例 7：針對支援票證，在 2019 年 12 月 20 日當天或之後建立的所有 Web 通訊</span><span class="sxs-lookup"><span data-stu-id="8624e-133">Example 7: Retrieve all Web communications created on or after Dec 20th, 2019 for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web' and CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="8624e-134">範例 8：使用管道支援票證物件來取回支援票證的所有通訊</span><span class="sxs-lookup"><span data-stu-id="8624e-134">Example 8: Retrieve all communications for a support ticket by piping support ticket object</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Get-AzSupportTicketCommunication

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
```

## <span data-ttu-id="8624e-135">參數</span><span class="sxs-lookup"><span data-stu-id="8624e-135">PARAMETERS</span></span>

### <span data-ttu-id="8624e-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8624e-136">-DefaultProfile</span></span>
<span data-ttu-id="8624e-137">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8624e-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8624e-138">-篩選</span><span class="sxs-lookup"><span data-stu-id="8624e-138">-Filter</span></span>
<span data-ttu-id="8624e-139">要用於此 Cmdlet 結果的篩選。</span><span class="sxs-lookup"><span data-stu-id="8624e-139">Filter to be applied to the results of this cmdlet.</span></span>

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

### <span data-ttu-id="8624e-140">-名稱</span><span class="sxs-lookup"><span data-stu-id="8624e-140">-Name</span></span>
<span data-ttu-id="8624e-141">通訊名稱。</span><span class="sxs-lookup"><span data-stu-id="8624e-141">Communication name.</span></span>

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

### <span data-ttu-id="8624e-142">-SupportTicketName</span><span class="sxs-lookup"><span data-stu-id="8624e-142">-SupportTicketName</span></span>
<span data-ttu-id="8624e-143">支援票證名稱。</span><span class="sxs-lookup"><span data-stu-id="8624e-143">Support ticket name.</span></span>

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

### <span data-ttu-id="8624e-144">-SupportTicketObject</span><span class="sxs-lookup"><span data-stu-id="8624e-144">-SupportTicketObject</span></span>
<span data-ttu-id="8624e-145">支援票證物件。</span><span class="sxs-lookup"><span data-stu-id="8624e-145">Support ticket object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSSupportTicket
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8624e-146">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="8624e-146">-IncludeTotalCount</span></span>
<span data-ttu-id="8624e-147">以整數來報告資料集中物件 (個整數) 選取的物件。</span><span class="sxs-lookup"><span data-stu-id="8624e-147">Reports the total number of objects in the data set (an integer) followed by the selected objects.</span></span>
<span data-ttu-id="8624e-148">如果 Cmdlet 無法判斷總計，則會顯示「未知總數」。</span><span class="sxs-lookup"><span data-stu-id="8624e-148">If the cmdlet cannot determine the total count, it displays "Unknown total count."</span></span> <span data-ttu-id="8624e-149">整數具有指出總計數值可靠性的 Accuracy 屬性。</span><span class="sxs-lookup"><span data-stu-id="8624e-149">The integer has an Accuracy property that indicates the reliability of the total count value.</span></span>
<span data-ttu-id="8624e-150">精確度值的範圍從 0.0 到 1.0，其中 0.0 表示 Cmdlet 無法計算物件，1.0 表示計數精確，而介於 0.0 到 1.0 之間的值表示估計值越可靠。</span><span class="sxs-lookup"><span data-stu-id="8624e-150">The value of Accuracy ranges from 0.0 to 1.0 where 0.0 means that the cmdlet could not count the objects, 1.0 means that the count is exact, and a value between 0.0 and 1.0 indicates an increasingly reliable estimate.</span></span>

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

### <span data-ttu-id="8624e-151">-略過</span><span class="sxs-lookup"><span data-stu-id="8624e-151">-Skip</span></span>
<span data-ttu-id="8624e-152">忽略指定的物件數目，然後獲得其餘的物件。</span><span class="sxs-lookup"><span data-stu-id="8624e-152">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="8624e-153">輸入要略過的物件數目。</span><span class="sxs-lookup"><span data-stu-id="8624e-153">Enter the number of objects to skip.</span></span>

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

### <span data-ttu-id="8624e-154">-第一個</span><span class="sxs-lookup"><span data-stu-id="8624e-154">-First</span></span>
<span data-ttu-id="8624e-155">只獲得指定的物件數目。</span><span class="sxs-lookup"><span data-stu-id="8624e-155">Gets only the specified number of objects.</span></span>
<span data-ttu-id="8624e-156">輸入要取得的物件數目。</span><span class="sxs-lookup"><span data-stu-id="8624e-156">Enter the number of objects to get.</span></span>

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

### <span data-ttu-id="8624e-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8624e-157">CommonParameters</span></span>
<span data-ttu-id="8624e-158">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8624e-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8624e-159">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8624e-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8624e-160">輸入</span><span class="sxs-lookup"><span data-stu-id="8624e-160">INPUTS</span></span>

### <span data-ttu-id="8624e-161">Microsoft.Azure.Commands.support.models.PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="8624e-161">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="8624e-162">輸出</span><span class="sxs-lookup"><span data-stu-id="8624e-162">OUTPUTS</span></span>

### <span data-ttu-id="8624e-163">Microsoft.Azure.Commands.support.models.PSSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="8624e-163">Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication</span></span>

## <span data-ttu-id="8624e-164">筆記</span><span class="sxs-lookup"><span data-stu-id="8624e-164">NOTES</span></span>

## <span data-ttu-id="8624e-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="8624e-165">RELATED LINKS</span></span>
