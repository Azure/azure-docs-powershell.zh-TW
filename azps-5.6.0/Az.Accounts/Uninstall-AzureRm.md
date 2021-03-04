---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/uninstall-azurerm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
ms.openlocfilehash: 796690bd0a5774e488b978003c48b02eedaac190
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905694"
---
# <span data-ttu-id="44898-101">Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="44898-101">Uninstall-AzureRm</span></span>

## <span data-ttu-id="44898-102">簡介</span><span class="sxs-lookup"><span data-stu-id="44898-102">SYNOPSIS</span></span>
<span data-ttu-id="44898-103">從電腦移除所有 AzureRm 模組。</span><span class="sxs-lookup"><span data-stu-id="44898-103">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="44898-104">語法</span><span class="sxs-lookup"><span data-stu-id="44898-104">SYNTAX</span></span>

```
Uninstall-AzureRm [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="44898-105">描述</span><span class="sxs-lookup"><span data-stu-id="44898-105">DESCRIPTION</span></span>
<span data-ttu-id="44898-106">從電腦移除所有 AzureRm 模組。</span><span class="sxs-lookup"><span data-stu-id="44898-106">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="44898-107">例子</span><span class="sxs-lookup"><span data-stu-id="44898-107">EXAMPLES</span></span>

### <span data-ttu-id="44898-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="44898-108">Example 1</span></span>
```
PS C:\> Uninstall-AzureRm
```

<span data-ttu-id="44898-109">執行此命令會針對執行 Cmdlet 的 PowerShell 版本，從電腦移除所有 AzureRm 模組。</span><span class="sxs-lookup"><span data-stu-id="44898-109">Running this command will remove all AzureRm modules from the machine for the version of PowerShell in which the cmdlet is run.</span></span>

## <span data-ttu-id="44898-110">參數</span><span class="sxs-lookup"><span data-stu-id="44898-110">PARAMETERS</span></span>

### <span data-ttu-id="44898-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44898-111">-DefaultProfile</span></span>
<span data-ttu-id="44898-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="44898-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44898-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="44898-113">-PassThru</span></span>
<span data-ttu-id="44898-114">已移除模組的退貨清單 ，如果已指定。</span><span class="sxs-lookup"><span data-stu-id="44898-114">Return list of Modules removed if specified.</span></span>

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

### <span data-ttu-id="44898-115">-確認</span><span class="sxs-lookup"><span data-stu-id="44898-115">-Confirm</span></span>
<span data-ttu-id="44898-116">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="44898-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44898-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44898-117">-WhatIf</span></span>
<span data-ttu-id="44898-118">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="44898-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44898-119">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="44898-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44898-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44898-120">CommonParameters</span></span>
<span data-ttu-id="44898-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="44898-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44898-122">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="44898-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44898-123">輸入</span><span class="sxs-lookup"><span data-stu-id="44898-123">INPUTS</span></span>

### <span data-ttu-id="44898-124">沒有</span><span class="sxs-lookup"><span data-stu-id="44898-124">None</span></span>

## <span data-ttu-id="44898-125">輸出</span><span class="sxs-lookup"><span data-stu-id="44898-125">OUTPUTS</span></span>

### <span data-ttu-id="44898-126">System.String</span><span class="sxs-lookup"><span data-stu-id="44898-126">System.String</span></span>

## <span data-ttu-id="44898-127">筆記</span><span class="sxs-lookup"><span data-stu-id="44898-127">NOTES</span></span>

## <span data-ttu-id="44898-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="44898-128">RELATED LINKS</span></span>
