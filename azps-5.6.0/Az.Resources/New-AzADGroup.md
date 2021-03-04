---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
ms.openlocfilehash: 910453711e047f9be1694bed0c92c502694d8a6e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908041"
---
# <span data-ttu-id="2111d-101">New-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="2111d-101">New-AzADGroup</span></span>

## <span data-ttu-id="2111d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2111d-102">SYNOPSIS</span></span>
<span data-ttu-id="2111d-103">建立新 Active Directory 群組。</span><span class="sxs-lookup"><span data-stu-id="2111d-103">Creates a new active directory group.</span></span>

## <span data-ttu-id="2111d-104">語法</span><span class="sxs-lookup"><span data-stu-id="2111d-104">SYNTAX</span></span>

```
New-AzADGroup -DisplayName <String> -MailNickname <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2111d-105">描述</span><span class="sxs-lookup"><span data-stu-id="2111d-105">DESCRIPTION</span></span>
<span data-ttu-id="2111d-106">建立新 Active Directory 群組。以下是所需的許可權：</span><span class="sxs-lookup"><span data-stu-id="2111d-106">Creates a new active directory group.Below are the permissions needed:</span></span>

- <span data-ttu-id="2111d-107">Azure Active Directory Graph</span><span class="sxs-lookup"><span data-stu-id="2111d-107">Azure Active Directory Graph</span></span>
  - <span data-ttu-id="2111d-108">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2111d-108">Directory.ReadWrite.All</span></span>
- <span data-ttu-id="2111d-109">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="2111d-109">Microsoft Graph</span></span>
  - <span data-ttu-id="2111d-110">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2111d-110">Directory.ReadWrite.All</span></span>
  - <span data-ttu-id="2111d-111">PrivilegedAccess.ReadWrite.AzureADGroup</span><span class="sxs-lookup"><span data-stu-id="2111d-111">PrivilegedAccess.ReadWrite.AzureADGroup</span></span>

## <span data-ttu-id="2111d-112">例子</span><span class="sxs-lookup"><span data-stu-id="2111d-112">EXAMPLES</span></span>

### <span data-ttu-id="2111d-113">範例 1：建立新 AD 群組</span><span class="sxs-lookup"><span data-stu-id="2111d-113">Example 1: Create a new AD group</span></span>

```powershell
PS C:\> New-AzADGroup -DisplayName "MyGroupDisplayName" -MailNickname "MyGroupNick"
```

<span data-ttu-id="2111d-114">建立名稱為 「MyGroupDisplayName」和郵件昵稱「MyGroupNick」的新 AD 群組。</span><span class="sxs-lookup"><span data-stu-id="2111d-114">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "MyGroupNick".</span></span>

## <span data-ttu-id="2111d-115">參數</span><span class="sxs-lookup"><span data-stu-id="2111d-115">PARAMETERS</span></span>

### <span data-ttu-id="2111d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2111d-116">-DefaultProfile</span></span>
<span data-ttu-id="2111d-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2111d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2111d-118">-描述</span><span class="sxs-lookup"><span data-stu-id="2111d-118">-Description</span></span>
<span data-ttu-id="2111d-119">群組的描述。</span><span class="sxs-lookup"><span data-stu-id="2111d-119">The description for the group.</span></span>

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

### <span data-ttu-id="2111d-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2111d-120">-DisplayName</span></span>
<span data-ttu-id="2111d-121">群組的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="2111d-121">The display name for the group.</span></span>

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

### <span data-ttu-id="2111d-122">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="2111d-122">-MailNickname</span></span>
<span data-ttu-id="2111d-123">群組的郵件昵稱。</span><span class="sxs-lookup"><span data-stu-id="2111d-123">The mail nickname for the group.</span></span> <span data-ttu-id="2111d-124">不能包含 @ 符號。</span><span class="sxs-lookup"><span data-stu-id="2111d-124">Cannot contain the @ sign.</span></span>

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

### <span data-ttu-id="2111d-125">-確認</span><span class="sxs-lookup"><span data-stu-id="2111d-125">-Confirm</span></span>
<span data-ttu-id="2111d-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2111d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2111d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2111d-127">-WhatIf</span></span>
<span data-ttu-id="2111d-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2111d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2111d-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2111d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2111d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2111d-130">CommonParameters</span></span>
<span data-ttu-id="2111d-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2111d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2111d-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2111d-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2111d-133">輸入</span><span class="sxs-lookup"><span data-stu-id="2111d-133">INPUTS</span></span>

### <span data-ttu-id="2111d-134">System.String</span><span class="sxs-lookup"><span data-stu-id="2111d-134">System.String</span></span>

## <span data-ttu-id="2111d-135">輸出</span><span class="sxs-lookup"><span data-stu-id="2111d-135">OUTPUTS</span></span>

### <span data-ttu-id="2111d-136">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span><span class="sxs-lookup"><span data-stu-id="2111d-136">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="2111d-137">筆記</span><span class="sxs-lookup"><span data-stu-id="2111d-137">NOTES</span></span>

## <span data-ttu-id="2111d-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="2111d-138">RELATED LINKS</span></span>
