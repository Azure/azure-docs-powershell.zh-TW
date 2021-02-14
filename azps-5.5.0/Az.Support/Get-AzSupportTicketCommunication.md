---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportticketcommunication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
ms.openlocfilehash: 07a8747f94f9c1fb93bbff06ce855363088a67a0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100134343"
---
# <span data-ttu-id="028e9-101">Get-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="028e9-101">Get-AzSupportTicketCommunication</span></span>

## <span data-ttu-id="028e9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="028e9-102">SYNOPSIS</span></span>
<span data-ttu-id="028e9-103">取得支援票證通訊。</span><span class="sxs-lookup"><span data-stu-id="028e9-103">Get support ticket communications.</span></span>

## <span data-ttu-id="028e9-104">句法</span><span class="sxs-lookup"><span data-stu-id="028e9-104">SYNTAX</span></span>

### <span data-ttu-id="028e9-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="028e9-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSupportTicketCommunication -SupportTicketName <String> [-Name <String>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

### <span data-ttu-id="028e9-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="028e9-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSupportTicketCommunication [-Name <String>] -SupportTicketObject <PSSupportTicket> [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

## <span data-ttu-id="028e9-107">說明</span><span class="sxs-lookup"><span data-stu-id="028e9-107">DESCRIPTION</span></span>
<span data-ttu-id="028e9-108">取得支援票證的通訊。</span><span class="sxs-lookup"><span data-stu-id="028e9-108">Gets communications for a support ticket.</span></span> <span data-ttu-id="028e9-109">如果您沒有指定任何其他參數，就會取得票證的所有通訊。</span><span class="sxs-lookup"><span data-stu-id="028e9-109">It will retrieve all the communications for a ticket if you do not specify any other parameters.</span></span> <span data-ttu-id="028e9-110">您也可以使用 Filter 參數，以 CreatedDate 或 CommunicationType 篩選通訊。</span><span class="sxs-lookup"><span data-stu-id="028e9-110">You can also filter the communications by CreatedDate or CommunicationType using the Filter parameter.</span></span> <span data-ttu-id="028e9-111">以下是您可以指定之篩選值的一些範例。</span><span class="sxs-lookup"><span data-stu-id="028e9-111">Here are some examples of filter values that you can specify.</span></span>


| <span data-ttu-id="028e9-112">例子</span><span class="sxs-lookup"><span data-stu-id="028e9-112">Scenario</span></span>                                                        | <span data-ttu-id="028e9-113">條件</span><span class="sxs-lookup"><span data-stu-id="028e9-113">Filter</span></span>                                                     |
|-----------------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="028e9-114">取得 Web 通訊</span><span class="sxs-lookup"><span data-stu-id="028e9-114">Get Web communications</span></span>                                          | <span data-ttu-id="028e9-115">"CommunicationType eq" 網頁 ""</span><span class="sxs-lookup"><span data-stu-id="028e9-115">"CommunicationType eq 'Web'"</span></span>                               |
| <span data-ttu-id="028e9-116">取得電話通訊</span><span class="sxs-lookup"><span data-stu-id="028e9-116">Get Phone communications</span></span>                                        | <span data-ttu-id="028e9-117">"CommunicationType eq" Phone ""</span><span class="sxs-lookup"><span data-stu-id="028e9-117">"CommunicationType eq 'Phone'"</span></span>                             |
| <span data-ttu-id="028e9-118">取得2019年12月20日或之後所建立的通訊</span><span class="sxs-lookup"><span data-stu-id="028e9-118">Get communications that were created on or after 20th Dec, 2019</span></span> | <span data-ttu-id="028e9-119">"CreatedDate ge 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="028e9-119">"CreatedDate ge 2019-12-20"</span></span>                                |
| <span data-ttu-id="028e9-120">取得2019年12月20日之後所建立的通訊</span><span class="sxs-lookup"><span data-stu-id="028e9-120">Get communications that were created after 20th Dec, 2019</span></span>       | <span data-ttu-id="028e9-121">"CreatedDate gt 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="028e9-121">"CreatedDate gt 2019-12-20"</span></span>                                |
| <span data-ttu-id="028e9-122">取得2019年12月20日之後建立的 Web 通訊</span><span class="sxs-lookup"><span data-stu-id="028e9-122">Gets Web communications created after 20th Dec, 2019</span></span>            | <span data-ttu-id="028e9-123">"CreatedDate gt 2019-12-20 and CommunicationType eq" 網頁 "</span><span class="sxs-lookup"><span data-stu-id="028e9-123">"CreatedDate gt 2019-12-20 and CommunicationType eq 'Web'"</span></span> |


<span data-ttu-id="028e9-124">這個 Cmdlet 支援透過第一個和略過參數進行分頁。</span><span class="sxs-lookup"><span data-stu-id="028e9-124">This cmdlet supports paging via First and Skip parameters.</span></span>

<span data-ttu-id="028e9-125">您也可以透過指定通訊名稱來取得單一支援票證通訊。</span><span class="sxs-lookup"><span data-stu-id="028e9-125">You can also retrieve a single support ticket communication by specifying the communication name.</span></span> 

## <span data-ttu-id="028e9-126">示例</span><span class="sxs-lookup"><span data-stu-id="028e9-126">EXAMPLES</span></span>

### <span data-ttu-id="028e9-127">範例1：檢索支援票證的所有通訊</span><span class="sxs-lookup"><span data-stu-id="028e9-127">Example 1: Retrieve all communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
```

### <span data-ttu-id="028e9-128">範例2：使用支援票證的名稱來取回單一通訊</span><span class="sxs-lookup"><span data-stu-id="028e9-128">Example 2: Retrieve a single communication by it's name for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Name "testmessage1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage1 user@contoso.com     test message   2/4/2020 9:38:14 PM
```

### <span data-ttu-id="028e9-129">範例3：檢索支援票證的前2筆通訊</span><span class="sxs-lookup"><span data-stu-id="028e9-129">Example 3: Retrieve first 2 communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="028e9-130">範例4：在跳過支援票證的前2筆通訊之後，再檢索後2筆通訊</span><span class="sxs-lookup"><span data-stu-id="028e9-130">Example 4: Retrieve next 2 communications after skipping first 2 communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Skip 2 -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage4 user@contoso.com     test message4  2/4/2020 9:38:14 PM
testmessage5 user@contoso.com     test message5  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="028e9-131">範例5：檢索支援票證的所有 Web 通訊</span><span class="sxs-lookup"><span data-stu-id="028e9-131">Example 5: Retrieve all Web communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web'"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="028e9-132">範例6：檢索支援票證2019年12月20日或之後所建立的所有通訊</span><span class="sxs-lookup"><span data-stu-id="028e9-132">Example 6: Retrieve all communications created on or after Dec 20th, 2019 for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="028e9-133">範例7：檢索支援票證2019年12月20日或之後所建立的所有 Web 通訊</span><span class="sxs-lookup"><span data-stu-id="028e9-133">Example 7: Retrieve all Web communications created on or after Dec 20th, 2019 for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web' and CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="028e9-134">範例8：透過管道支援票證物件來檢索支援票證的所有通訊</span><span class="sxs-lookup"><span data-stu-id="028e9-134">Example 8: Retrieve all communications for a support ticket by piping support ticket object</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Get-AzSupportTicketCommunication

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
```

## <span data-ttu-id="028e9-135">參數</span><span class="sxs-lookup"><span data-stu-id="028e9-135">PARAMETERS</span></span>

### <span data-ttu-id="028e9-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="028e9-136">-DefaultProfile</span></span>
<span data-ttu-id="028e9-137">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="028e9-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="028e9-138">-篩選</span><span class="sxs-lookup"><span data-stu-id="028e9-138">-Filter</span></span>
<span data-ttu-id="028e9-139">要套用至此 Cmdlet 結果的篩選。</span><span class="sxs-lookup"><span data-stu-id="028e9-139">Filter to be applied to the results of this cmdlet.</span></span>

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

### <span data-ttu-id="028e9-140">-名稱</span><span class="sxs-lookup"><span data-stu-id="028e9-140">-Name</span></span>
<span data-ttu-id="028e9-141">通訊名稱。</span><span class="sxs-lookup"><span data-stu-id="028e9-141">Communication name.</span></span>

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

### <span data-ttu-id="028e9-142">-SupportTicketName</span><span class="sxs-lookup"><span data-stu-id="028e9-142">-SupportTicketName</span></span>
<span data-ttu-id="028e9-143">支援票證名稱。</span><span class="sxs-lookup"><span data-stu-id="028e9-143">Support ticket name.</span></span>

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

### <span data-ttu-id="028e9-144">-SupportTicketObject</span><span class="sxs-lookup"><span data-stu-id="028e9-144">-SupportTicketObject</span></span>
<span data-ttu-id="028e9-145">支援票證物件。</span><span class="sxs-lookup"><span data-stu-id="028e9-145">Support ticket object.</span></span>

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

### <span data-ttu-id="028e9-146">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="028e9-146">-IncludeTotalCount</span></span>
<span data-ttu-id="028e9-147">報告資料集中的物件總數 (整數) 接著選取的物件。</span><span class="sxs-lookup"><span data-stu-id="028e9-147">Reports the total number of objects in the data set (an integer) followed by the selected objects.</span></span>
<span data-ttu-id="028e9-148">如果 Cmdlet 無法判斷總計數，則會顯示「未知總計數」。</span><span class="sxs-lookup"><span data-stu-id="028e9-148">If the cmdlet cannot determine the total count, it displays "Unknown total count."</span></span> <span data-ttu-id="028e9-149">這個整數有一個正確性屬性，指出總計數值的可靠性。</span><span class="sxs-lookup"><span data-stu-id="028e9-149">The integer has an Accuracy property that indicates the reliability of the total count value.</span></span>
<span data-ttu-id="028e9-150">精確度的值範圍從0.0 到1.0，其中0.0 表示 Cmdlet 無法計算物件，1.0 表示該計數完全正確，而在0.0 與1.0 之間的值則表示日益可靠的估計。</span><span class="sxs-lookup"><span data-stu-id="028e9-150">The value of Accuracy ranges from 0.0 to 1.0 where 0.0 means that the cmdlet could not count the objects, 1.0 means that the count is exact, and a value between 0.0 and 1.0 indicates an increasingly reliable estimate.</span></span>

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

### <span data-ttu-id="028e9-151">-略過</span><span class="sxs-lookup"><span data-stu-id="028e9-151">-Skip</span></span>
<span data-ttu-id="028e9-152">忽略指定的物件數目，然後取得剩餘的物件。</span><span class="sxs-lookup"><span data-stu-id="028e9-152">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="028e9-153">輸入要略過的物件數目。</span><span class="sxs-lookup"><span data-stu-id="028e9-153">Enter the number of objects to skip.</span></span>

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

### <span data-ttu-id="028e9-154">-優先</span><span class="sxs-lookup"><span data-stu-id="028e9-154">-First</span></span>
<span data-ttu-id="028e9-155">只取得指定數目的物件。</span><span class="sxs-lookup"><span data-stu-id="028e9-155">Gets only the specified number of objects.</span></span>
<span data-ttu-id="028e9-156">輸入要取得的物件數目。</span><span class="sxs-lookup"><span data-stu-id="028e9-156">Enter the number of objects to get.</span></span>

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

### <span data-ttu-id="028e9-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="028e9-157">CommonParameters</span></span>
<span data-ttu-id="028e9-158">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="028e9-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="028e9-159">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="028e9-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="028e9-160">輸入</span><span class="sxs-lookup"><span data-stu-id="028e9-160">INPUTS</span></span>

### <span data-ttu-id="028e9-161">PSSupportTicket （支援）。</span><span class="sxs-lookup"><span data-stu-id="028e9-161">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="028e9-162">輸出</span><span class="sxs-lookup"><span data-stu-id="028e9-162">OUTPUTS</span></span>

### <span data-ttu-id="028e9-163">PSSupportTicketCommunication （支援）。</span><span class="sxs-lookup"><span data-stu-id="028e9-163">Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication</span></span>

## <span data-ttu-id="028e9-164">筆記</span><span class="sxs-lookup"><span data-stu-id="028e9-164">NOTES</span></span>

## <span data-ttu-id="028e9-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="028e9-165">RELATED LINKS</span></span>
