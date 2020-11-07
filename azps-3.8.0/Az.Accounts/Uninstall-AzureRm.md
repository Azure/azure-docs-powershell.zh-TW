---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/uninstall-azurerm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
ms.openlocfilehash: ee581528810663d09fe724f370b681ff9e20072f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957929"
---
# <span data-ttu-id="81b3f-101">Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="81b3f-101">Uninstall-AzureRm</span></span>

## <span data-ttu-id="81b3f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="81b3f-102">SYNOPSIS</span></span>
<span data-ttu-id="81b3f-103">從電腦中移除所有 AzureRm 模組。</span><span class="sxs-lookup"><span data-stu-id="81b3f-103">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="81b3f-104">句法</span><span class="sxs-lookup"><span data-stu-id="81b3f-104">SYNTAX</span></span>

```
Uninstall-AzureRm [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="81b3f-105">說明</span><span class="sxs-lookup"><span data-stu-id="81b3f-105">DESCRIPTION</span></span>
<span data-ttu-id="81b3f-106">從電腦中移除所有 AzureRm 模組。</span><span class="sxs-lookup"><span data-stu-id="81b3f-106">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="81b3f-107">示例</span><span class="sxs-lookup"><span data-stu-id="81b3f-107">EXAMPLES</span></span>

### <span data-ttu-id="81b3f-108">範例1</span><span class="sxs-lookup"><span data-stu-id="81b3f-108">Example 1</span></span>
```
PS C:\> Uninstall-AzureRm
```

<span data-ttu-id="81b3f-109">執行此命令時，會從電腦的所有 AzureRm 模組中移除執行 Cmdlet 的 PowerShell 版本。</span><span class="sxs-lookup"><span data-stu-id="81b3f-109">Running this command will remove all AzureRm modules from the machine for the version of PowerShell in which the cmdlet is run.</span></span>

## <span data-ttu-id="81b3f-110">參數</span><span class="sxs-lookup"><span data-stu-id="81b3f-110">PARAMETERS</span></span>

### <span data-ttu-id="81b3f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81b3f-111">-DefaultProfile</span></span>
<span data-ttu-id="81b3f-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="81b3f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81b3f-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="81b3f-113">-PassThru</span></span>
<span data-ttu-id="81b3f-114">如果指定，則傳回移除的模組清單。</span><span class="sxs-lookup"><span data-stu-id="81b3f-114">Return list of Modules removed if specified.</span></span>

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

### <span data-ttu-id="81b3f-115">-確認</span><span class="sxs-lookup"><span data-stu-id="81b3f-115">-Confirm</span></span>
<span data-ttu-id="81b3f-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="81b3f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81b3f-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81b3f-117">-WhatIf</span></span>
<span data-ttu-id="81b3f-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="81b3f-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81b3f-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="81b3f-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81b3f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81b3f-120">CommonParameters</span></span>
<span data-ttu-id="81b3f-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="81b3f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81b3f-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="81b3f-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81b3f-123">輸入</span><span class="sxs-lookup"><span data-stu-id="81b3f-123">INPUTS</span></span>

### <span data-ttu-id="81b3f-124">所有</span><span class="sxs-lookup"><span data-stu-id="81b3f-124">None</span></span>

## <span data-ttu-id="81b3f-125">輸出</span><span class="sxs-lookup"><span data-stu-id="81b3f-125">OUTPUTS</span></span>

### <span data-ttu-id="81b3f-126">System.object</span><span class="sxs-lookup"><span data-stu-id="81b3f-126">System.String</span></span>

## <span data-ttu-id="81b3f-127">筆記</span><span class="sxs-lookup"><span data-stu-id="81b3f-127">NOTES</span></span>

## <span data-ttu-id="81b3f-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="81b3f-128">RELATED LINKS</span></span>
