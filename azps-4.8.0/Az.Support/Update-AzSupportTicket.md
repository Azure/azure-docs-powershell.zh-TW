---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/update-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Update-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Update-AzSupportTicket.md
ms.openlocfilehash: 160d6b4d4a8505c99d5bfcb4c535ec7bbb3b6dd3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127972"
---
# <span data-ttu-id="c1ddf-101">Update-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="c1ddf-101">Update-AzSupportTicket</span></span>

## <span data-ttu-id="c1ddf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c1ddf-102">SYNOPSIS</span></span>
<span data-ttu-id="c1ddf-103">更新支援票證。</span><span class="sxs-lookup"><span data-stu-id="c1ddf-103">Updates support ticket.</span></span>

## <span data-ttu-id="c1ddf-104">句法</span><span class="sxs-lookup"><span data-stu-id="c1ddf-104">SYNTAX</span></span>

### <span data-ttu-id="c1ddf-105">UpdateByNameWithContactDetailParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c1ddf-105">UpdateByNameWithContactDetailParameterSet (Default)</span></span>
```
Update-AzSupportTicket -Name <String> [-Severity <Severity>] [-Status <Status>] [-CustomerFirstName <String>]
 [-CustomerLastName <String>] [-PreferredContactMethod <ContactMethod>] [-CustomerPrimaryEmailAddress <String>]
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] [-CustomerPreferredTimeZone <String>]
 [-CustomerCountry <String>] [-CustomerPreferredSupportLanguage <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1ddf-106">UpdateByNameWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1ddf-106">UpdateByNameWithContactObjectParameterSet</span></span>
```
Update-AzSupportTicket -Name <String> [-Severity <Severity>] [-Status <Status>] -CustomerContactDetail <PSContactProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1ddf-107">UpdateByInputObjectWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1ddf-107">UpdateByInputObjectWithContactDetailParameterSet</span></span>
```
Update-AzSupportTicket -InputObject <PSSupportTicket> [-Severity <Severity>] [-Status <Status>] [-CustomerFirstName <String>]
 [-CustomerLastName <String>] [-PreferredContactMethod <ContactMethod>] [-CustomerPrimaryEmailAddress <String>]
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] [-CustomerPreferredTimeZone <String>]
 [-CustomerCountry <String>] [-CustomerPreferredSupportLanguage <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1ddf-108">UpdateByInputObjectWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1ddf-108">UpdateByInputObjectWithContactObjectParameterSet</span></span>
```
Update-AzSupportTicket -InputObject <PSSupportTicket> [-Severity <Severity>] [-Status <Status>]
 -CustomerContactDetail <PSContactProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c1ddf-109">說明</span><span class="sxs-lookup"><span data-stu-id="c1ddf-109">DESCRIPTION</span></span>
<span data-ttu-id="c1ddf-110">使用此 Cmdlet 來更新支援票證的嚴重性等級、狀態或客戶連絡人詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c1ddf-110">Use this cmdlet to update a support ticket's severity level, status or customer contact details.</span></span> <span data-ttu-id="c1ddf-111">請注意，當票證指派給支援工程師時，不允許更新支援票證的嚴重性等級或狀態。</span><span class="sxs-lookup"><span data-stu-id="c1ddf-111">Note that updating a support ticket's severity level or status is not allowed when the ticket is assigned to a support engineer.</span></span> <span data-ttu-id="c1ddf-112">如果您想要在指派票證之後更新嚴重等級或狀態，請在票證上傳送通訊以與支援工程師聯繫。</span><span class="sxs-lookup"><span data-stu-id="c1ddf-112">If you wish to update the severity level or status after ticket assignment, contact the support engineer by sending a communication on the ticket.</span></span>

## <span data-ttu-id="c1ddf-113">示例</span><span class="sxs-lookup"><span data-stu-id="c1ddf-113">EXAMPLES</span></span>

### <span data-ttu-id="c1ddf-114">範例1：更新支援票證的嚴重度。</span><span class="sxs-lookup"><span data-stu-id="c1ddf-114">Example 1: Update severity of support ticket.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -Severity "moderate"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="c1ddf-115">範例2：更新支援票證的狀態。</span><span class="sxs-lookup"><span data-stu-id="c1ddf-115">Example 2: Update status of support ticket.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -Status "Closed"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Closed   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="c1ddf-116">範例3：透過指定連絡人物件來更新支援票證的連絡人詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c1ddf-116">Example 3: Update contact details of support ticket by specify contact object.</span></span>
```powershell
PS C:\> $contactDetail = new-object Microsoft.Azure.Commands.Support.Models.PSContactProfile
PS C:\> $contactDetail.FirstName = "first name updated"
PS C:\> $contactDetail.LastName = "last name updated"
PS C:\> Update-AzSupportTicket -Name "test1" -CustomerContactDetail $contactDetail 

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="c1ddf-117">範例4：依管道支援票證物件更新支援票證的嚴重度。</span><span class="sxs-lookup"><span data-stu-id="c1ddf-117">Example 4: Update severity of support ticket by piping support ticket object.</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Update-AzSupportTicket -Severity "moderate"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="c1ddf-118">範例5：透過指定個別的連絡人參數來更新支援票證的連絡人詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c1ddf-118">Example 5: Update contact details of support ticket by specifying individual contact parameters.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -CustomerFirstName "first name updated" -CustomerLastName "last name updated" -AdditionalEmailAddress @("user2@contoso.com") 

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="c1ddf-119">範例6：依管道支援票證物件更新支援票證的狀態。</span><span class="sxs-lookup"><span data-stu-id="c1ddf-119">Example 6: Update status of support ticket by piping support ticket object.</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Update-AzSupportTicket -Status "Closed"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Closed   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="c1ddf-120">參數</span><span class="sxs-lookup"><span data-stu-id="c1ddf-120">PARAMETERS</span></span>

### <span data-ttu-id="c1ddf-121">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="c1ddf-121">-AdditionalEmailAddress</span></span>
<span data-ttu-id="c1ddf-122">其他電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="c1ddf-122">Additional email addresses.</span></span>
<span data-ttu-id="c1ddf-123">此處列出的電子郵件地址將會在有關支援票證的任何函件上複製。</span><span class="sxs-lookup"><span data-stu-id="c1ddf-123">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1ddf-124">-CustomerContactDetail</span><span class="sxs-lookup"><span data-stu-id="c1ddf-124">-CustomerContactDetail</span></span>
<span data-ttu-id="c1ddf-125">更新 SupportTicket 上的連絡人詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c1ddf-125">Update Contact details on SupportTicket.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSContactProfile
Parameter Sets: UpdateByNameWithContactObjectParameterSet, UpdateByInputObjectWithContactObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1ddf-126">-CustomerCountry</span><span class="sxs-lookup"><span data-stu-id="c1ddf-126">-CustomerCountry</span></span>
<span data-ttu-id="c1ddf-127">客戶國家/地區。</span><span class="sxs-lookup"><span data-stu-id="c1ddf-127">Customer country.</span></span>
<span data-ttu-id="c1ddf-128">這必須是合法的 ISO Alpha-3 國家/地區代碼 (ISO 3166) 。</span><span class="sxs-lookup"><span data-stu-id="c1ddf-128">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1ddf-129">-CustomerFirstName</span><span class="sxs-lookup"><span data-stu-id="c1ddf-129">-CustomerFirstName</span></span>
<span data-ttu-id="c1ddf-130">客戶名字。</span><span class="sxs-lookup"><span data-stu-id="c1ddf-130">Customer first name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1ddf-131">-CustomerLastName</span><span class="sxs-lookup"><span data-stu-id="c1ddf-131">-CustomerLastName</span></span>
<span data-ttu-id="c1ddf-132">客戶姓氏。</span><span class="sxs-lookup"><span data-stu-id="c1ddf-132">Customer last name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1ddf-133">-CustomerPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="c1ddf-133">-CustomerPhoneNumber</span></span>
<span data-ttu-id="c1ddf-134">客戶電話號碼。</span><span class="sxs-lookup"><span data-stu-id="c1ddf-134">Customer phone number.</span></span>
<span data-ttu-id="c1ddf-135">如果您喜歡的連絡方式是手機，則需要這麼做。</span><span class="sxs-lookup"><span data-stu-id="c1ddf-135">This is required if preferred contact method is phone.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1ddf-136">-CustomerPreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="c1ddf-136">-CustomerPreferredSupportLanguage</span></span>
<span data-ttu-id="c1ddf-137">客戶慣用的支援語言。</span><span class="sxs-lookup"><span data-stu-id="c1ddf-137">Customer preferred support language.</span></span>
<span data-ttu-id="c1ddf-138">這必須是有效的語言 contry 程式碼，適用于此處所列的其中一個支援的語言 https://azure.microsoft.com/support/faq/ 。</span><span class="sxs-lookup"><span data-stu-id="c1ddf-138">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/support/faq/.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1ddf-139">-CustomerPreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="c1ddf-139">-CustomerPreferredTimeZone</span></span>
<span data-ttu-id="c1ddf-140">客戶慣用時區。</span><span class="sxs-lookup"><span data-stu-id="c1ddf-140">Customer preferred time zone.</span></span>
<span data-ttu-id="c1ddf-141">這必須是有效的 System.TimeZoneInfo.Id 值。</span><span class="sxs-lookup"><span data-stu-id="c1ddf-141">This must be a valid System.TimeZoneInfo.Id value.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1ddf-142">-CustomerPrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="c1ddf-142">-CustomerPrimaryEmailAddress</span></span>
<span data-ttu-id="c1ddf-143">客戶主要電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="c1ddf-143">Customer primary email address.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1ddf-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1ddf-144">-DefaultProfile</span></span>
<span data-ttu-id="c1ddf-145">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c1ddf-145">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1ddf-146">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c1ddf-146">-InputObject</span></span>
<span data-ttu-id="c1ddf-147">此 Cmdlet 更新的 SupportTicket 資源物件。</span><span class="sxs-lookup"><span data-stu-id="c1ddf-147">SupportTicket resource object that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSSupportTicket
Parameter Sets: UpdateByInputObjectWithContactDetailParameterSet, UpdateByInputObjectWithContactObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1ddf-148">-名稱</span><span class="sxs-lookup"><span data-stu-id="c1ddf-148">-Name</span></span>
<span data-ttu-id="c1ddf-149">此 Cmdlet 更新之 SupportTicket 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="c1ddf-149">Name of SupportTicket resource that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByNameWithContactObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1ddf-150">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="c1ddf-150">-PreferredContactMethod</span></span>
<span data-ttu-id="c1ddf-151">[首選連絡方式] 方法。</span><span class="sxs-lookup"><span data-stu-id="c1ddf-151">Preferred contact method.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.ContactMethod
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:
Accepted values: Email, Phone

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1ddf-152">-嚴重度</span><span class="sxs-lookup"><span data-stu-id="c1ddf-152">-Severity</span></span>
<span data-ttu-id="c1ddf-153">更新 SupportTicket 的嚴重度。</span><span class="sxs-lookup"><span data-stu-id="c1ddf-153">Update Severity of SupportTicket.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.Severity
Parameter Sets: (All)
Aliases:
Accepted values: Minimal, Moderate, Critical, HighestCriticalImpact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1ddf-154">-狀態</span><span class="sxs-lookup"><span data-stu-id="c1ddf-154">-Status</span></span>
<span data-ttu-id="c1ddf-155">更新 SupportTicket 的狀態。</span><span class="sxs-lookup"><span data-stu-id="c1ddf-155">Update Status of SupportTicket.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.Status
Parameter Sets: (All)
Aliases:
Accepted values: Open, Closed

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1ddf-156">-確認</span><span class="sxs-lookup"><span data-stu-id="c1ddf-156">-Confirm</span></span>
<span data-ttu-id="c1ddf-157">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c1ddf-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1ddf-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1ddf-158">-WhatIf</span></span>
<span data-ttu-id="c1ddf-159">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c1ddf-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1ddf-160">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c1ddf-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1ddf-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1ddf-161">CommonParameters</span></span>
<span data-ttu-id="c1ddf-162">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c1ddf-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1ddf-163">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c1ddf-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1ddf-164">輸入</span><span class="sxs-lookup"><span data-stu-id="c1ddf-164">INPUTS</span></span>

### <span data-ttu-id="c1ddf-165">PSSupportTicket （支援）。</span><span class="sxs-lookup"><span data-stu-id="c1ddf-165">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="c1ddf-166">輸出</span><span class="sxs-lookup"><span data-stu-id="c1ddf-166">OUTPUTS</span></span>

### <span data-ttu-id="c1ddf-167">PSSupportTicket （支援）。</span><span class="sxs-lookup"><span data-stu-id="c1ddf-167">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="c1ddf-168">筆記</span><span class="sxs-lookup"><span data-stu-id="c1ddf-168">NOTES</span></span>

## <span data-ttu-id="c1ddf-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="c1ddf-169">RELATED LINKS</span></span>
