---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/uninstall-azurerm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
ms.openlocfilehash: ee581528810663d09fe724f370b681ff9e20072f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100138975"
---
# <span data-ttu-id="5dc59-101">Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="5dc59-101">Uninstall-AzureRm</span></span>

## <span data-ttu-id="5dc59-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5dc59-102">SYNOPSIS</span></span>
<span data-ttu-id="5dc59-103">從電腦中移除所有 AzureRm 模組。</span><span class="sxs-lookup"><span data-stu-id="5dc59-103">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="5dc59-104">句法</span><span class="sxs-lookup"><span data-stu-id="5dc59-104">SYNTAX</span></span>

```
Uninstall-AzureRm [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5dc59-105">說明</span><span class="sxs-lookup"><span data-stu-id="5dc59-105">DESCRIPTION</span></span>
<span data-ttu-id="5dc59-106">從電腦中移除所有 AzureRm 模組。</span><span class="sxs-lookup"><span data-stu-id="5dc59-106">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="5dc59-107">示例</span><span class="sxs-lookup"><span data-stu-id="5dc59-107">EXAMPLES</span></span>

### <span data-ttu-id="5dc59-108">範例1</span><span class="sxs-lookup"><span data-stu-id="5dc59-108">Example 1</span></span>
```
PS C:\> Uninstall-AzureRm
```

<span data-ttu-id="5dc59-109">執行此命令時，會從電腦的所有 AzureRm 模組中移除執行 Cmdlet 的 PowerShell 版本。</span><span class="sxs-lookup"><span data-stu-id="5dc59-109">Running this command will remove all AzureRm modules from the machine for the version of PowerShell in which the cmdlet is run.</span></span>

## <span data-ttu-id="5dc59-110">參數</span><span class="sxs-lookup"><span data-stu-id="5dc59-110">PARAMETERS</span></span>

### <span data-ttu-id="5dc59-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dc59-111">-DefaultProfile</span></span>
<span data-ttu-id="5dc59-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5dc59-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5dc59-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5dc59-113">-PassThru</span></span>
<span data-ttu-id="5dc59-114">如果指定，則傳回移除的模組清單。</span><span class="sxs-lookup"><span data-stu-id="5dc59-114">Return list of Modules removed if specified.</span></span>

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

### <span data-ttu-id="5dc59-115">-確認</span><span class="sxs-lookup"><span data-stu-id="5dc59-115">-Confirm</span></span>
<span data-ttu-id="5dc59-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5dc59-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5dc59-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5dc59-117">-WhatIf</span></span>
<span data-ttu-id="5dc59-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5dc59-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5dc59-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5dc59-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5dc59-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dc59-120">CommonParameters</span></span>
<span data-ttu-id="5dc59-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5dc59-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dc59-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5dc59-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dc59-123">輸入</span><span class="sxs-lookup"><span data-stu-id="5dc59-123">INPUTS</span></span>

### <span data-ttu-id="5dc59-124">所有</span><span class="sxs-lookup"><span data-stu-id="5dc59-124">None</span></span>

## <span data-ttu-id="5dc59-125">輸出</span><span class="sxs-lookup"><span data-stu-id="5dc59-125">OUTPUTS</span></span>

### <span data-ttu-id="5dc59-126">System.object</span><span class="sxs-lookup"><span data-stu-id="5dc59-126">System.String</span></span>

## <span data-ttu-id="5dc59-127">筆記</span><span class="sxs-lookup"><span data-stu-id="5dc59-127">NOTES</span></span>

## <span data-ttu-id="5dc59-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="5dc59-128">RELATED LINKS</span></span>
