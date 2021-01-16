---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
ms.openlocfilehash: 98d87c060c51d19db45e907f88d39f27350248c9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435466"
---
# <span data-ttu-id="b3bdd-101">New-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="b3bdd-101">New-AzADGroup</span></span>

## <span data-ttu-id="b3bdd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b3bdd-102">SYNOPSIS</span></span>
<span data-ttu-id="b3bdd-103">建立新的 active directory 群組。</span><span class="sxs-lookup"><span data-stu-id="b3bdd-103">Creates a new active directory group.</span></span>

## <span data-ttu-id="b3bdd-104">句法</span><span class="sxs-lookup"><span data-stu-id="b3bdd-104">SYNTAX</span></span>

```
New-AzADGroup -DisplayName <String> -MailNickname <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3bdd-105">說明</span><span class="sxs-lookup"><span data-stu-id="b3bdd-105">DESCRIPTION</span></span>
<span data-ttu-id="b3bdd-106">建立新的 active directory 群組。下列是所需的許可權：</span><span class="sxs-lookup"><span data-stu-id="b3bdd-106">Creates a new active directory group.Below are the permissions needed:</span></span>

- <span data-ttu-id="b3bdd-107">Azure Active Directory 圖形</span><span class="sxs-lookup"><span data-stu-id="b3bdd-107">Azure Active Directory Graph</span></span>
  - <span data-ttu-id="b3bdd-108">ReadWrite. All</span><span class="sxs-lookup"><span data-stu-id="b3bdd-108">Directory.ReadWrite.All</span></span>
- <span data-ttu-id="b3bdd-109">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="b3bdd-109">Microsoft Graph</span></span>
  - <span data-ttu-id="b3bdd-110">ReadWrite. All</span><span class="sxs-lookup"><span data-stu-id="b3bdd-110">Directory.ReadWrite.All</span></span>
  - <span data-ttu-id="b3bdd-111">PrivilegedAccess ReadWrite. AzureADGroup</span><span class="sxs-lookup"><span data-stu-id="b3bdd-111">PrivilegedAccess.ReadWrite.AzureADGroup</span></span>

## <span data-ttu-id="b3bdd-112">示例</span><span class="sxs-lookup"><span data-stu-id="b3bdd-112">EXAMPLES</span></span>

### <span data-ttu-id="b3bdd-113">範例1：建立新的廣告群組</span><span class="sxs-lookup"><span data-stu-id="b3bdd-113">Example 1: Create a new AD group</span></span>

```powershell
PS C:\> New-AzADGroup -DisplayName "MyGroupDisplayName" -MailNickname "MyGroupNick"
```

<span data-ttu-id="b3bdd-114">建立名為 "MyGroupDisplayName" 的新 AD 群組，以及 [郵件別名 "MyGroupNick]。</span><span class="sxs-lookup"><span data-stu-id="b3bdd-114">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "MyGroupNick".</span></span>

## <span data-ttu-id="b3bdd-115">參數</span><span class="sxs-lookup"><span data-stu-id="b3bdd-115">PARAMETERS</span></span>

### <span data-ttu-id="b3bdd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3bdd-116">-DefaultProfile</span></span>
<span data-ttu-id="b3bdd-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b3bdd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3bdd-118">-描述</span><span class="sxs-lookup"><span data-stu-id="b3bdd-118">-Description</span></span>
<span data-ttu-id="b3bdd-119">群組的描述。</span><span class="sxs-lookup"><span data-stu-id="b3bdd-119">The description for the group.</span></span>

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

### <span data-ttu-id="b3bdd-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b3bdd-120">-DisplayName</span></span>
<span data-ttu-id="b3bdd-121">群組的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="b3bdd-121">The display name for the group.</span></span>

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

### <span data-ttu-id="b3bdd-122">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="b3bdd-122">-MailNickname</span></span>
<span data-ttu-id="b3bdd-123">群組的 [郵件別名]。</span><span class="sxs-lookup"><span data-stu-id="b3bdd-123">The mail nickname for the group.</span></span> <span data-ttu-id="b3bdd-124">不能包含 @ 符號。</span><span class="sxs-lookup"><span data-stu-id="b3bdd-124">Cannot contain the @ sign.</span></span>

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

### <span data-ttu-id="b3bdd-125">-確認</span><span class="sxs-lookup"><span data-stu-id="b3bdd-125">-Confirm</span></span>
<span data-ttu-id="b3bdd-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b3bdd-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3bdd-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3bdd-127">-WhatIf</span></span>
<span data-ttu-id="b3bdd-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b3bdd-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3bdd-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b3bdd-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3bdd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3bdd-130">CommonParameters</span></span>
<span data-ttu-id="b3bdd-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b3bdd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3bdd-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b3bdd-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3bdd-133">輸入</span><span class="sxs-lookup"><span data-stu-id="b3bdd-133">INPUTS</span></span>

### <span data-ttu-id="b3bdd-134">System.object</span><span class="sxs-lookup"><span data-stu-id="b3bdd-134">System.String</span></span>

## <span data-ttu-id="b3bdd-135">輸出</span><span class="sxs-lookup"><span data-stu-id="b3bdd-135">OUTPUTS</span></span>

### <span data-ttu-id="b3bdd-136">PSADGroup （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="b3bdd-136">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="b3bdd-137">筆記</span><span class="sxs-lookup"><span data-stu-id="b3bdd-137">NOTES</span></span>

## <span data-ttu-id="b3bdd-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="b3bdd-138">RELATED LINKS</span></span>
