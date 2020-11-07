---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADGroup.md
ms.openlocfilehash: b5bc2f2eb99a8256dcaa6bc4f026d922f0f563ea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795295"
---
# <span data-ttu-id="255a5-101">New-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="255a5-101">New-AzADGroup</span></span>

## <span data-ttu-id="255a5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="255a5-102">SYNOPSIS</span></span>
<span data-ttu-id="255a5-103">建立新的 active directory 群組。</span><span class="sxs-lookup"><span data-stu-id="255a5-103">Creates a new active directory group.</span></span>

## <span data-ttu-id="255a5-104">句法</span><span class="sxs-lookup"><span data-stu-id="255a5-104">SYNTAX</span></span>

```
New-AzADGroup -DisplayName <String> -MailNickname <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="255a5-105">說明</span><span class="sxs-lookup"><span data-stu-id="255a5-105">DESCRIPTION</span></span>
<span data-ttu-id="255a5-106">建立新的 active directory 群組。</span><span class="sxs-lookup"><span data-stu-id="255a5-106">Creates a new active directory group.</span></span>

## <span data-ttu-id="255a5-107">示例</span><span class="sxs-lookup"><span data-stu-id="255a5-107">EXAMPLES</span></span>

### <span data-ttu-id="255a5-108">範例 1-建立新的廣告群組</span><span class="sxs-lookup"><span data-stu-id="255a5-108">Example 1 - Create a new AD group</span></span>

```
PS C:\> New-AzADGroup -DisplayName "MyGroupDisplayName" -MailNickname "myemail@domain.com"
```

<span data-ttu-id="255a5-109">建立名為 "MyGroupDisplayName" 的新廣告群組，以及郵件別名 " myemail@domain.com "。</span><span class="sxs-lookup"><span data-stu-id="255a5-109">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "myemail@domain.com".</span></span>

## <span data-ttu-id="255a5-110">參數</span><span class="sxs-lookup"><span data-stu-id="255a5-110">PARAMETERS</span></span>

### <span data-ttu-id="255a5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="255a5-111">-DefaultProfile</span></span>
<span data-ttu-id="255a5-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="255a5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="255a5-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="255a5-113">-DisplayName</span></span>
<span data-ttu-id="255a5-114">群組的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="255a5-114">The display name for the group.</span></span>

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

### <span data-ttu-id="255a5-115">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="255a5-115">-MailNickname</span></span>
<span data-ttu-id="255a5-116">群組的 [郵件別名]。</span><span class="sxs-lookup"><span data-stu-id="255a5-116">The mail nickname for the group.</span></span>

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

### <span data-ttu-id="255a5-117">-確認</span><span class="sxs-lookup"><span data-stu-id="255a5-117">-Confirm</span></span>
<span data-ttu-id="255a5-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="255a5-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="255a5-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="255a5-119">-WhatIf</span></span>
<span data-ttu-id="255a5-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="255a5-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="255a5-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="255a5-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="255a5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="255a5-122">CommonParameters</span></span>
<span data-ttu-id="255a5-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="255a5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="255a5-124">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="255a5-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="255a5-125">輸入</span><span class="sxs-lookup"><span data-stu-id="255a5-125">INPUTS</span></span>

### <span data-ttu-id="255a5-126">System.object</span><span class="sxs-lookup"><span data-stu-id="255a5-126">System.String</span></span>

## <span data-ttu-id="255a5-127">輸出</span><span class="sxs-lookup"><span data-stu-id="255a5-127">OUTPUTS</span></span>

### <span data-ttu-id="255a5-128">Microsoft.Azure.Graph.RBAC.Version1_6 PSADGroup</span><span class="sxs-lookup"><span data-stu-id="255a5-128">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="255a5-129">筆記</span><span class="sxs-lookup"><span data-stu-id="255a5-129">NOTES</span></span>

## <span data-ttu-id="255a5-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="255a5-130">RELATED LINKS</span></span>
