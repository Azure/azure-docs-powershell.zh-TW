---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
ms.openlocfilehash: 6496f2c65c5cfecb01ed68d0e47281fba72b7b63
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965905"
---
# <span data-ttu-id="79d4f-101">New-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="79d4f-101">New-AzADGroup</span></span>

## <span data-ttu-id="79d4f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="79d4f-102">SYNOPSIS</span></span>
<span data-ttu-id="79d4f-103">建立新的 active directory 群組。</span><span class="sxs-lookup"><span data-stu-id="79d4f-103">Creates a new active directory group.</span></span>

## <span data-ttu-id="79d4f-104">句法</span><span class="sxs-lookup"><span data-stu-id="79d4f-104">SYNTAX</span></span>

```
New-AzADGroup -DisplayName <String> -MailNickname <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79d4f-105">說明</span><span class="sxs-lookup"><span data-stu-id="79d4f-105">DESCRIPTION</span></span>
<span data-ttu-id="79d4f-106">建立新的 active directory 群組。</span><span class="sxs-lookup"><span data-stu-id="79d4f-106">Creates a new active directory group.</span></span>

## <span data-ttu-id="79d4f-107">示例</span><span class="sxs-lookup"><span data-stu-id="79d4f-107">EXAMPLES</span></span>

### <span data-ttu-id="79d4f-108">範例 1-建立新的廣告群組</span><span class="sxs-lookup"><span data-stu-id="79d4f-108">Example 1 - Create a new AD group</span></span>

```
PS C:\> New-AzADGroup -DisplayName "MyGroupDisplayName" -MailNickname "MyGroupNick"
```

<span data-ttu-id="79d4f-109">建立名為 "MyGroupDisplayName" 的新 AD 群組，以及 [郵件別名 "MyGroupNick]。</span><span class="sxs-lookup"><span data-stu-id="79d4f-109">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "MyGroupNick".</span></span>

## <span data-ttu-id="79d4f-110">參數</span><span class="sxs-lookup"><span data-stu-id="79d4f-110">PARAMETERS</span></span>

### <span data-ttu-id="79d4f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79d4f-111">-DefaultProfile</span></span>
<span data-ttu-id="79d4f-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="79d4f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79d4f-113">-描述</span><span class="sxs-lookup"><span data-stu-id="79d4f-113">-Description</span></span>
<span data-ttu-id="79d4f-114">群組的描述。</span><span class="sxs-lookup"><span data-stu-id="79d4f-114">The description for the group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79d4f-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="79d4f-115">-DisplayName</span></span>
<span data-ttu-id="79d4f-116">群組的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="79d4f-116">The display name for the group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79d4f-117">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="79d4f-117">-MailNickname</span></span>
<span data-ttu-id="79d4f-118">群組的 [郵件別名]。</span><span class="sxs-lookup"><span data-stu-id="79d4f-118">The mail nickname for the group.</span></span> <span data-ttu-id="79d4f-119">不能包含 @ 符號。</span><span class="sxs-lookup"><span data-stu-id="79d4f-119">Cannot contain the @ sign.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79d4f-120">-確認</span><span class="sxs-lookup"><span data-stu-id="79d4f-120">-Confirm</span></span>
<span data-ttu-id="79d4f-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="79d4f-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79d4f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79d4f-122">-WhatIf</span></span>
<span data-ttu-id="79d4f-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="79d4f-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79d4f-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="79d4f-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79d4f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79d4f-125">CommonParameters</span></span>
<span data-ttu-id="79d4f-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="79d4f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79d4f-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="79d4f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79d4f-128">輸入</span><span class="sxs-lookup"><span data-stu-id="79d4f-128">INPUTS</span></span>

### <span data-ttu-id="79d4f-129">System.object</span><span class="sxs-lookup"><span data-stu-id="79d4f-129">System.String</span></span>

## <span data-ttu-id="79d4f-130">輸出</span><span class="sxs-lookup"><span data-stu-id="79d4f-130">OUTPUTS</span></span>

### <span data-ttu-id="79d4f-131">PSADGroup （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="79d4f-131">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="79d4f-132">筆記</span><span class="sxs-lookup"><span data-stu-id="79d4f-132">NOTES</span></span>

## <span data-ttu-id="79d4f-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="79d4f-133">RELATED LINKS</span></span>
