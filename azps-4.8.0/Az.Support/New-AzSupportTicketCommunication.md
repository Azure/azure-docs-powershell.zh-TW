---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportticketcommunication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicketCommunication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicketCommunication.md
ms.openlocfilehash: 3a0191e1df223427ec7d60dfd92f7607e2c171b0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127977"
---
# <span data-ttu-id="e9dec-101">New-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="e9dec-101">New-AzSupportTicketCommunication</span></span>

## <span data-ttu-id="e9dec-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e9dec-102">SYNOPSIS</span></span>
<span data-ttu-id="e9dec-103">建立新的支援票證通訊。</span><span class="sxs-lookup"><span data-stu-id="e9dec-103">Creates a new support ticket communication.</span></span>

## <span data-ttu-id="e9dec-104">句法</span><span class="sxs-lookup"><span data-stu-id="e9dec-104">SYNTAX</span></span>

### <span data-ttu-id="e9dec-105">CreateByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e9dec-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSupportTicketCommunication -SupportTicketName <String> -Name <String> -Subject <String> -Body <String>
 [-Sender <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e9dec-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9dec-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSupportTicketCommunication -SupportTicketObject <PSSupportTicket> -Name <String> -Subject <String>
 -Body <String> [-Sender <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e9dec-107">說明</span><span class="sxs-lookup"><span data-stu-id="e9dec-107">DESCRIPTION</span></span>
<span data-ttu-id="e9dec-108">將新的客戶通訊新增至 Azure 支援票證。</span><span class="sxs-lookup"><span data-stu-id="e9dec-108">Adds a new customer communication to an Azure support ticket.</span></span>

## <span data-ttu-id="e9dec-109">示例</span><span class="sxs-lookup"><span data-stu-id="e9dec-109">EXAMPLES</span></span>

### <span data-ttu-id="e9dec-110">範例1</span><span class="sxs-lookup"><span data-stu-id="e9dec-110">Example 1</span></span>
```powershell
PS C:\> New-AzSupportTicketCommunication -Name "testmessage" -SupportTicketName "testticket" -Subject "test subject" -Body "test body" -Sender "user@contoso.com"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage  user@contoso.com     test subject   2/4/2020 9:38:14 PM
```

## <span data-ttu-id="e9dec-111">參數</span><span class="sxs-lookup"><span data-stu-id="e9dec-111">PARAMETERS</span></span>

### <span data-ttu-id="e9dec-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e9dec-112">-AsJob</span></span>
<span data-ttu-id="e9dec-113">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e9dec-113">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="e9dec-114">-Body</span><span class="sxs-lookup"><span data-stu-id="e9dec-114">-Body</span></span>
<span data-ttu-id="e9dec-115">通訊的主體。</span><span class="sxs-lookup"><span data-stu-id="e9dec-115">Body of the communication.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9dec-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9dec-116">-DefaultProfile</span></span>
<span data-ttu-id="e9dec-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e9dec-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9dec-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="e9dec-118">-Name</span></span>
<span data-ttu-id="e9dec-119">通訊資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="e9dec-119">Name of the communication resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9dec-120">-寄件者</span><span class="sxs-lookup"><span data-stu-id="e9dec-120">-Sender</span></span>
<span data-ttu-id="e9dec-121">寄件者的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="e9dec-121">Email address of the sender.</span></span>

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

### <span data-ttu-id="e9dec-122">-Subject</span><span class="sxs-lookup"><span data-stu-id="e9dec-122">-Subject</span></span>
<span data-ttu-id="e9dec-123">溝通的目標。</span><span class="sxs-lookup"><span data-stu-id="e9dec-123">Subject of the communication.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9dec-124">-SupportTicketName</span><span class="sxs-lookup"><span data-stu-id="e9dec-124">-SupportTicketName</span></span>
<span data-ttu-id="e9dec-125">支援票證名稱。</span><span class="sxs-lookup"><span data-stu-id="e9dec-125">Support ticket name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9dec-126">-SupportTicketObject</span><span class="sxs-lookup"><span data-stu-id="e9dec-126">-SupportTicketObject</span></span>
<span data-ttu-id="e9dec-127">支援票證物件。</span><span class="sxs-lookup"><span data-stu-id="e9dec-127">Support ticket object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSSupportTicket
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9dec-128">-確認</span><span class="sxs-lookup"><span data-stu-id="e9dec-128">-Confirm</span></span>
<span data-ttu-id="e9dec-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e9dec-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9dec-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9dec-130">-WhatIf</span></span>
<span data-ttu-id="e9dec-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e9dec-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9dec-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e9dec-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9dec-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9dec-133">CommonParameters</span></span>
<span data-ttu-id="e9dec-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e9dec-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9dec-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e9dec-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9dec-136">輸入</span><span class="sxs-lookup"><span data-stu-id="e9dec-136">INPUTS</span></span>

### <span data-ttu-id="e9dec-137">PSSupportTicket （支援）。</span><span class="sxs-lookup"><span data-stu-id="e9dec-137">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="e9dec-138">輸出</span><span class="sxs-lookup"><span data-stu-id="e9dec-138">OUTPUTS</span></span>

### <span data-ttu-id="e9dec-139">PSSupportTicketCommunication （支援）。</span><span class="sxs-lookup"><span data-stu-id="e9dec-139">Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication</span></span>

## <span data-ttu-id="e9dec-140">筆記</span><span class="sxs-lookup"><span data-stu-id="e9dec-140">NOTES</span></span>

## <span data-ttu-id="e9dec-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="e9dec-141">RELATED LINKS</span></span>