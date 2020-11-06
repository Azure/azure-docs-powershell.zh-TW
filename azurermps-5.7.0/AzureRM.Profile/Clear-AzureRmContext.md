---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/clear-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmContext.md
ms.openlocfilehash: 960e1b35a90b0bc1c490cbf194c20ac7a051e4d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444460"
---
# <span data-ttu-id="23e92-101">Clear-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="23e92-101">Clear-AzureRmContext</span></span>

## <span data-ttu-id="23e92-102">摘要</span><span class="sxs-lookup"><span data-stu-id="23e92-102">SYNOPSIS</span></span>
<span data-ttu-id="23e92-103">移除所有 Azure 認證、帳戶及訂閱資訊。</span><span class="sxs-lookup"><span data-stu-id="23e92-103">Remove all Azure credentials, account, and subscription information.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23e92-104">句法</span><span class="sxs-lookup"><span data-stu-id="23e92-104">SYNTAX</span></span>

```
Clear-AzureRmContext -Scope <ContextModificationScope> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23e92-105">說明</span><span class="sxs-lookup"><span data-stu-id="23e92-105">DESCRIPTION</span></span>
<span data-ttu-id="23e92-106">移除所有 Azure 認證、帳戶及訂閱資訊。</span><span class="sxs-lookup"><span data-stu-id="23e92-106">Remove all Azure Credentials, account, and subscription information.</span></span>

## <span data-ttu-id="23e92-107">示例</span><span class="sxs-lookup"><span data-stu-id="23e92-107">EXAMPLES</span></span>

### <span data-ttu-id="23e92-108">清除全域內容</span><span class="sxs-lookup"><span data-stu-id="23e92-108">Clear global context</span></span>
```
PS C:\> Clear-AzureRmContext -Scope CurrentUser
```

<span data-ttu-id="23e92-109">移除任何 powershell 會話的所有帳戶、訂閱及認證資訊。</span><span class="sxs-lookup"><span data-stu-id="23e92-109">Remove all account, subscription, and credential information for any powershell session.</span></span>

## <span data-ttu-id="23e92-110">參數</span><span class="sxs-lookup"><span data-stu-id="23e92-110">PARAMETERS</span></span>

### <span data-ttu-id="23e92-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23e92-111">-DefaultProfile</span></span>
<span data-ttu-id="23e92-112">用於與 azure 進行通訊的認證、租使用者與訂閱</span><span class="sxs-lookup"><span data-stu-id="23e92-112">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23e92-113">-Force</span><span class="sxs-lookup"><span data-stu-id="23e92-113">-Force</span></span>
<span data-ttu-id="23e92-114">刪除全域範圍中的所有使用者和群組，但不提示</span><span class="sxs-lookup"><span data-stu-id="23e92-114">Delete all users and groups from the global scope without prompting</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23e92-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="23e92-115">-PassThru</span></span>
<span data-ttu-id="23e92-116">傳回表示成功或失敗的值</span><span class="sxs-lookup"><span data-stu-id="23e92-116">Return a value indicating success or failure</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23e92-117">-範圍</span><span class="sxs-lookup"><span data-stu-id="23e92-117">-Scope</span></span>
<span data-ttu-id="23e92-118">清除目前 PowerShell 會話或所有會話的內容。</span><span class="sxs-lookup"><span data-stu-id="23e92-118">Clear the context only for the current PowerShell session, or for all sessions.</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23e92-119">-確認</span><span class="sxs-lookup"><span data-stu-id="23e92-119">-Confirm</span></span>
<span data-ttu-id="23e92-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="23e92-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23e92-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23e92-121">-WhatIf</span></span>
<span data-ttu-id="23e92-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="23e92-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23e92-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="23e92-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23e92-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23e92-124">CommonParameters</span></span>
<span data-ttu-id="23e92-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="23e92-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23e92-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="23e92-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23e92-127">輸入</span><span class="sxs-lookup"><span data-stu-id="23e92-127">INPUTS</span></span>

### <span data-ttu-id="23e92-128">所有</span><span class="sxs-lookup"><span data-stu-id="23e92-128">None</span></span>

## <span data-ttu-id="23e92-129">輸出</span><span class="sxs-lookup"><span data-stu-id="23e92-129">OUTPUTS</span></span>

### <span data-ttu-id="23e92-130">System.object</span><span class="sxs-lookup"><span data-stu-id="23e92-130">System.Boolean</span></span>
<span data-ttu-id="23e92-131">如果成功清除內容，則為 True，否則則為 false。</span><span class="sxs-lookup"><span data-stu-id="23e92-131">True if the context was successfully cleared, false otherwise.</span></span>

## <span data-ttu-id="23e92-132">筆記</span><span class="sxs-lookup"><span data-stu-id="23e92-132">NOTES</span></span>

## <span data-ttu-id="23e92-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="23e92-133">RELATED LINKS</span></span>

