---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/powershell/module/az.support/update-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Update-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Update-AzSupportTicket.md
ms.openlocfilehash: 5fac9eac7225364af7c884ab64a80d4299939ec0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915710"
---
# <span data-ttu-id="9dbe4-101">Update-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="9dbe4-101">Update-AzSupportTicket</span></span>

## <span data-ttu-id="9dbe4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9dbe4-102">SYNOPSIS</span></span>
<span data-ttu-id="9dbe4-103">更新支援票證。</span><span class="sxs-lookup"><span data-stu-id="9dbe4-103">Updates support ticket.</span></span>

## <span data-ttu-id="9dbe4-104">語法</span><span class="sxs-lookup"><span data-stu-id="9dbe4-104">SYNTAX</span></span>

### <span data-ttu-id="9dbe4-105">UpdateByNameWithContactDetailParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9dbe4-105">UpdateByNameWithContactDetailParameterSet (Default)</span></span>
```
Update-AzSupportTicket -Name <String> [-Severity <Severity>] [-Status <Status>] [-CustomerFirstName <String>]
 [-CustomerLastName <String>] [-PreferredContactMethod <ContactMethod>] [-CustomerPrimaryEmailAddress <String>]
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] [-CustomerPreferredTimeZone <String>]
 [-CustomerCountry <String>] [-CustomerPreferredSupportLanguage <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9dbe4-106">UpdateByNameWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9dbe4-106">UpdateByNameWithContactObjectParameterSet</span></span>
```
Update-AzSupportTicket -Name <String> [-Severity <Severity>] [-Status <Status>] -CustomerContactDetail <PSContactProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9dbe4-107">UpdateByInputObjectWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="9dbe4-107">UpdateByInputObjectWithContactDetailParameterSet</span></span>
```
Update-AzSupportTicket -InputObject <PSSupportTicket> [-Severity <Severity>] [-Status <Status>] [-CustomerFirstName <String>]
 [-CustomerLastName <String>] [-PreferredContactMethod <ContactMethod>] [-CustomerPrimaryEmailAddress <String>]
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] [-CustomerPreferredTimeZone <String>]
 [-CustomerCountry <String>] [-CustomerPreferredSupportLanguage <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9dbe4-108">UpdateByInputObjectWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9dbe4-108">UpdateByInputObjectWithContactObjectParameterSet</span></span>
```
Update-AzSupportTicket -InputObject <PSSupportTicket> [-Severity <Severity>] [-Status <Status>]
 -CustomerContactDetail <PSContactProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9dbe4-109">描述</span><span class="sxs-lookup"><span data-stu-id="9dbe4-109">DESCRIPTION</span></span>
<span data-ttu-id="9dbe4-110">使用此 Cmdlet 更新支援票證的嚴重性等級、狀態或客戶連絡人詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9dbe4-110">Use this cmdlet to update a support ticket's severity level, status or customer contact details.</span></span> <span data-ttu-id="9dbe4-111">請注意，將票證指派給支援工程師時，不允許更新支援票證的嚴重性等級或狀態。</span><span class="sxs-lookup"><span data-stu-id="9dbe4-111">Note that updating a support ticket's severity level or status is not allowed when the ticket is assigned to a support engineer.</span></span> <span data-ttu-id="9dbe4-112">如果您想要在票證指派後更新嚴重性等級或狀態，請傳送票證上的通訊給支援工程師。</span><span class="sxs-lookup"><span data-stu-id="9dbe4-112">If you wish to update the severity level or status after ticket assignment, contact the support engineer by sending a communication on the ticket.</span></span>

## <span data-ttu-id="9dbe4-113">例子</span><span class="sxs-lookup"><span data-stu-id="9dbe4-113">EXAMPLES</span></span>

### <span data-ttu-id="9dbe4-114">範例 1：更新支援票證的嚴重性。</span><span class="sxs-lookup"><span data-stu-id="9dbe4-114">Example 1: Update severity of support ticket.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -Severity "moderate"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="9dbe4-115">範例 2：更新支援票證的狀態。</span><span class="sxs-lookup"><span data-stu-id="9dbe4-115">Example 2: Update status of support ticket.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -Status "Closed"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Closed   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="9dbe4-116">範例 3：指定連絡人物件以更新支援票證的連絡人詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9dbe4-116">Example 3: Update contact details of support ticket by specify contact object.</span></span>
```powershell
PS C:\> $contactDetail = new-object Microsoft.Azure.Commands.Support.Models.PSContactProfile
PS C:\> $contactDetail.FirstName = "first name updated"
PS C:\> $contactDetail.LastName = "last name updated"
PS C:\> Update-AzSupportTicket -Name "test1" -CustomerContactDetail $contactDetail 

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="9dbe4-117">範例 4：以管道支援票證物件更新支援票證的嚴重性。</span><span class="sxs-lookup"><span data-stu-id="9dbe4-117">Example 4: Update severity of support ticket by piping support ticket object.</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Update-AzSupportTicket -Severity "moderate"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="9dbe4-118">範例 5：指定個別的連絡人參數來更新支援票證的連絡人詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9dbe4-118">Example 5: Update contact details of support ticket by specifying individual contact parameters.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -CustomerFirstName "first name updated" -CustomerLastName "last name updated" -AdditionalEmailAddress @("user2@contoso.com") 

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="9dbe4-119">範例 6：以管道支援票證物件更新支援票證的狀態。</span><span class="sxs-lookup"><span data-stu-id="9dbe4-119">Example 6: Update status of support ticket by piping support ticket object.</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Update-AzSupportTicket -Status "Closed"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Closed   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="9dbe4-120">參數</span><span class="sxs-lookup"><span data-stu-id="9dbe4-120">PARAMETERS</span></span>

### <span data-ttu-id="9dbe4-121">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="9dbe4-121">-AdditionalEmailAddress</span></span>
<span data-ttu-id="9dbe4-122">其他電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="9dbe4-122">Additional email addresses.</span></span>
<span data-ttu-id="9dbe4-123">此處所列的電子郵件地址將會複製到支援票證的任何對應。</span><span class="sxs-lookup"><span data-stu-id="9dbe4-123">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

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

### <span data-ttu-id="9dbe4-124">-CustomerContactDetail</span><span class="sxs-lookup"><span data-stu-id="9dbe4-124">-CustomerContactDetail</span></span>
<span data-ttu-id="9dbe4-125">更新 SupportTicket 上的連絡人詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9dbe4-125">Update Contact details on SupportTicket.</span></span>

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

### <span data-ttu-id="9dbe4-126">-CustomerCountry</span><span class="sxs-lookup"><span data-stu-id="9dbe4-126">-CustomerCountry</span></span>
<span data-ttu-id="9dbe4-127">客戶國家/地區。</span><span class="sxs-lookup"><span data-stu-id="9dbe4-127">Customer country.</span></span>
<span data-ttu-id="9dbe4-128">這必須是 ISO 3166 (有效的 ISO Alpha-3) 。</span><span class="sxs-lookup"><span data-stu-id="9dbe4-128">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

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

### <span data-ttu-id="9dbe4-129">-CustomerFirstName</span><span class="sxs-lookup"><span data-stu-id="9dbe4-129">-CustomerFirstName</span></span>
<span data-ttu-id="9dbe4-130">客戶名字。</span><span class="sxs-lookup"><span data-stu-id="9dbe4-130">Customer first name.</span></span>

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

### <span data-ttu-id="9dbe4-131">-CustomerLastName</span><span class="sxs-lookup"><span data-stu-id="9dbe4-131">-CustomerLastName</span></span>
<span data-ttu-id="9dbe4-132">客戶姓氏。</span><span class="sxs-lookup"><span data-stu-id="9dbe4-132">Customer last name.</span></span>

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

### <span data-ttu-id="9dbe4-133">-CustomerPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="9dbe4-133">-CustomerPhoneNumber</span></span>
<span data-ttu-id="9dbe4-134">客戶電話號碼。</span><span class="sxs-lookup"><span data-stu-id="9dbe4-134">Customer phone number.</span></span>
<span data-ttu-id="9dbe4-135">如果偏好的連絡人方法是電話，則此為必填專案。</span><span class="sxs-lookup"><span data-stu-id="9dbe4-135">This is required if preferred contact method is phone.</span></span>

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

### <span data-ttu-id="9dbe4-136">-CustomerPreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="9dbe4-136">-CustomerPreferredSupportLanguage</span></span>
<span data-ttu-id="9dbe4-137">客戶偏好的支援語言。</span><span class="sxs-lookup"><span data-stu-id="9dbe4-137">Customer preferred support language.</span></span>
<span data-ttu-id="9dbe4-138">這必須是此處所列的其中一個支援語言的有效語言代碼 https://azure.microsoft.com/support/faq/ 。</span><span class="sxs-lookup"><span data-stu-id="9dbe4-138">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/support/faq/.</span></span>

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

### <span data-ttu-id="9dbe4-139">-CustomerPreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="9dbe4-139">-CustomerPreferredTimeZone</span></span>
<span data-ttu-id="9dbe4-140">客戶偏好的時區。</span><span class="sxs-lookup"><span data-stu-id="9dbe4-140">Customer preferred time zone.</span></span>
<span data-ttu-id="9dbe4-141">這必須是有效的System.TimeZoneInfo.Id值。</span><span class="sxs-lookup"><span data-stu-id="9dbe4-141">This must be a valid System.TimeZoneInfo.Id value.</span></span>

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

### <span data-ttu-id="9dbe4-142">-CustomerPrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="9dbe4-142">-CustomerPrimaryEmailAddress</span></span>
<span data-ttu-id="9dbe4-143">客戶主要電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="9dbe4-143">Customer primary email address.</span></span>

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

### <span data-ttu-id="9dbe4-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dbe4-144">-DefaultProfile</span></span>
<span data-ttu-id="9dbe4-145">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9dbe4-145">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9dbe4-146">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9dbe4-146">-InputObject</span></span>
<span data-ttu-id="9dbe4-147">此 Cmdlet 更新的 SupportTicket 資源物件。</span><span class="sxs-lookup"><span data-stu-id="9dbe4-147">SupportTicket resource object that this cmdlet updates.</span></span>

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

### <span data-ttu-id="9dbe4-148">-名稱</span><span class="sxs-lookup"><span data-stu-id="9dbe4-148">-Name</span></span>
<span data-ttu-id="9dbe4-149">此 Cmdlet 更新的 SupportTicket 資源名稱。</span><span class="sxs-lookup"><span data-stu-id="9dbe4-149">Name of SupportTicket resource that this cmdlet updates.</span></span>

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

### <span data-ttu-id="9dbe4-150">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="9dbe4-150">-PreferredContactMethod</span></span>
<span data-ttu-id="9dbe4-151">偏好的連絡人方法。</span><span class="sxs-lookup"><span data-stu-id="9dbe4-151">Preferred contact method.</span></span>

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

### <span data-ttu-id="9dbe4-152">-嚴重性</span><span class="sxs-lookup"><span data-stu-id="9dbe4-152">-Severity</span></span>
<span data-ttu-id="9dbe4-153">更新 SupportTicket 的嚴重性。</span><span class="sxs-lookup"><span data-stu-id="9dbe4-153">Update Severity of SupportTicket.</span></span>

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

### <span data-ttu-id="9dbe4-154">-狀態</span><span class="sxs-lookup"><span data-stu-id="9dbe4-154">-Status</span></span>
<span data-ttu-id="9dbe4-155">更新 SupportTicket 的狀態。</span><span class="sxs-lookup"><span data-stu-id="9dbe4-155">Update Status of SupportTicket.</span></span>

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

### <span data-ttu-id="9dbe4-156">-確認</span><span class="sxs-lookup"><span data-stu-id="9dbe4-156">-Confirm</span></span>
<span data-ttu-id="9dbe4-157">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9dbe4-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9dbe4-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dbe4-158">-WhatIf</span></span>
<span data-ttu-id="9dbe4-159">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9dbe4-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9dbe4-160">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9dbe4-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9dbe4-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dbe4-161">CommonParameters</span></span>
<span data-ttu-id="9dbe4-162">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9dbe4-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dbe4-163">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9dbe4-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dbe4-164">輸入</span><span class="sxs-lookup"><span data-stu-id="9dbe4-164">INPUTS</span></span>

### <span data-ttu-id="9dbe4-165">Microsoft.Azure.Commands.support.models.PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="9dbe4-165">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="9dbe4-166">輸出</span><span class="sxs-lookup"><span data-stu-id="9dbe4-166">OUTPUTS</span></span>

### <span data-ttu-id="9dbe4-167">Microsoft.Azure.Commands.support.models.PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="9dbe4-167">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="9dbe4-168">筆記</span><span class="sxs-lookup"><span data-stu-id="9dbe4-168">NOTES</span></span>

## <span data-ttu-id="9dbe4-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="9dbe4-169">RELATED LINKS</span></span>
