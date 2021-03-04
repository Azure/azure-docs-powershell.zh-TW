---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/powershell/module/az.support/new-azsupportticketcommunication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicketCommunication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicketCommunication.md
ms.openlocfilehash: 0c8595605f5dc84c28e4e00ee66e72cdfc79256c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907205"
---
# <span data-ttu-id="209ba-101">New-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="209ba-101">New-AzSupportTicketCommunication</span></span>

## <span data-ttu-id="209ba-102">簡介</span><span class="sxs-lookup"><span data-stu-id="209ba-102">SYNOPSIS</span></span>
<span data-ttu-id="209ba-103">建立新的支援票證通訊。</span><span class="sxs-lookup"><span data-stu-id="209ba-103">Creates a new support ticket communication.</span></span>

## <span data-ttu-id="209ba-104">語法</span><span class="sxs-lookup"><span data-stu-id="209ba-104">SYNTAX</span></span>

### <span data-ttu-id="209ba-105">CreateByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="209ba-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSupportTicketCommunication -SupportTicketName <String> -Name <String> -Subject <String> -Body <String>
 [-Sender <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="209ba-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="209ba-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSupportTicketCommunication -SupportTicketObject <PSSupportTicket> -Name <String> -Subject <String>
 -Body <String> [-Sender <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="209ba-107">描述</span><span class="sxs-lookup"><span data-stu-id="209ba-107">DESCRIPTION</span></span>
<span data-ttu-id="209ba-108">新增客戶通訊至 Azure 支援票證。</span><span class="sxs-lookup"><span data-stu-id="209ba-108">Adds a new customer communication to an Azure support ticket.</span></span>

## <span data-ttu-id="209ba-109">例子</span><span class="sxs-lookup"><span data-stu-id="209ba-109">EXAMPLES</span></span>

### <span data-ttu-id="209ba-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="209ba-110">Example 1</span></span>
```powershell
PS C:\> New-AzSupportTicketCommunication -Name "testmessage" -SupportTicketName "testticket" -Subject "test subject" -Body "test body" -Sender "user@contoso.com"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage  user@contoso.com     test subject   2/4/2020 9:38:14 PM
```

## <span data-ttu-id="209ba-111">參數</span><span class="sxs-lookup"><span data-stu-id="209ba-111">PARAMETERS</span></span>

### <span data-ttu-id="209ba-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="209ba-112">-AsJob</span></span>
<span data-ttu-id="209ba-113">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="209ba-113">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="209ba-114">-Body</span><span class="sxs-lookup"><span data-stu-id="209ba-114">-Body</span></span>
<span data-ttu-id="209ba-115">通訊的內體。</span><span class="sxs-lookup"><span data-stu-id="209ba-115">Body of the communication.</span></span>

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

### <span data-ttu-id="209ba-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="209ba-116">-DefaultProfile</span></span>
<span data-ttu-id="209ba-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="209ba-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="209ba-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="209ba-118">-Name</span></span>
<span data-ttu-id="209ba-119">通訊資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="209ba-119">Name of the communication resource.</span></span>

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

### <span data-ttu-id="209ba-120">-寄件者</span><span class="sxs-lookup"><span data-stu-id="209ba-120">-Sender</span></span>
<span data-ttu-id="209ba-121">寄件者的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="209ba-121">Email address of the sender.</span></span>

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

### <span data-ttu-id="209ba-122">-Subject</span><span class="sxs-lookup"><span data-stu-id="209ba-122">-Subject</span></span>
<span data-ttu-id="209ba-123">通訊的主體。</span><span class="sxs-lookup"><span data-stu-id="209ba-123">Subject of the communication.</span></span>

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

### <span data-ttu-id="209ba-124">-SupportTicketName</span><span class="sxs-lookup"><span data-stu-id="209ba-124">-SupportTicketName</span></span>
<span data-ttu-id="209ba-125">支援票證名稱。</span><span class="sxs-lookup"><span data-stu-id="209ba-125">Support ticket name.</span></span>

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

### <span data-ttu-id="209ba-126">-SupportTicketObject</span><span class="sxs-lookup"><span data-stu-id="209ba-126">-SupportTicketObject</span></span>
<span data-ttu-id="209ba-127">支援票證物件。</span><span class="sxs-lookup"><span data-stu-id="209ba-127">Support ticket object.</span></span>

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

### <span data-ttu-id="209ba-128">-確認</span><span class="sxs-lookup"><span data-stu-id="209ba-128">-Confirm</span></span>
<span data-ttu-id="209ba-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="209ba-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="209ba-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="209ba-130">-WhatIf</span></span>
<span data-ttu-id="209ba-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="209ba-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="209ba-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="209ba-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="209ba-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="209ba-133">CommonParameters</span></span>
<span data-ttu-id="209ba-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="209ba-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="209ba-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="209ba-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="209ba-136">輸入</span><span class="sxs-lookup"><span data-stu-id="209ba-136">INPUTS</span></span>

### <span data-ttu-id="209ba-137">Microsoft.Azure.Commands.support.models.PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="209ba-137">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="209ba-138">輸出</span><span class="sxs-lookup"><span data-stu-id="209ba-138">OUTPUTS</span></span>

### <span data-ttu-id="209ba-139">Microsoft.Azure.Commands.support.models.PSSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="209ba-139">Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication</span></span>

## <span data-ttu-id="209ba-140">筆記</span><span class="sxs-lookup"><span data-stu-id="209ba-140">NOTES</span></span>

## <span data-ttu-id="209ba-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="209ba-141">RELATED LINKS</span></span>
