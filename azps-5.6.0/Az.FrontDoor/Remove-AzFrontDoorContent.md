---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/remove-azfrontdoorcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorContent.md
ms.openlocfilehash: 608c80322e46f3c6871bac0350fcc8ae5a5113bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917733"
---
# <span data-ttu-id="03b31-101">Remove-AzFrontDoorContent</span><span class="sxs-lookup"><span data-stu-id="03b31-101">Remove-AzFrontDoorContent</span></span>

## <span data-ttu-id="03b31-102">簡介</span><span class="sxs-lookup"><span data-stu-id="03b31-102">SYNOPSIS</span></span>
<span data-ttu-id="03b31-103">移除前方門中的內容</span><span class="sxs-lookup"><span data-stu-id="03b31-103">Remove contents in Front Door</span></span>

## <span data-ttu-id="03b31-104">語法</span><span class="sxs-lookup"><span data-stu-id="03b31-104">SYNTAX</span></span>

```
Remove-AzFrontDoorContent -ResourceGroupName <String> -Name <String> -ContentPath <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03b31-105">描述</span><span class="sxs-lookup"><span data-stu-id="03b31-105">DESCRIPTION</span></span>
<span data-ttu-id="03b31-106">Remove-AzFrontDoorContent清除前門中的緩存內容</span><span class="sxs-lookup"><span data-stu-id="03b31-106">Remove-AzFrontDoorContent purges cached contents in a Front Door</span></span>

## <span data-ttu-id="03b31-107">例子</span><span class="sxs-lookup"><span data-stu-id="03b31-107">EXAMPLES</span></span>

### <span data-ttu-id="03b31-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="03b31-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorContent -ResourceGroupName $ResourceGroupName -Name $FrontDoorName -ContentPath "/*"
```

## <span data-ttu-id="03b31-109">參數</span><span class="sxs-lookup"><span data-stu-id="03b31-109">PARAMETERS</span></span>

### <span data-ttu-id="03b31-110">-ContentPath</span><span class="sxs-lookup"><span data-stu-id="03b31-110">-ContentPath</span></span>
<span data-ttu-id="03b31-111">要清除之內容的路徑。</span><span class="sxs-lookup"><span data-stu-id="03b31-111">The paths to the content to be purged.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03b31-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03b31-112">-DefaultProfile</span></span>
<span data-ttu-id="03b31-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="03b31-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03b31-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="03b31-114">-Name</span></span>
<span data-ttu-id="03b31-115">前門名稱。</span><span class="sxs-lookup"><span data-stu-id="03b31-115">Front Door name.</span></span>

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

### <span data-ttu-id="03b31-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03b31-116">-PassThru</span></span>
<span data-ttu-id="03b31-117">如果指定 (，則) 。</span><span class="sxs-lookup"><span data-stu-id="03b31-117">Return object (if specified).</span></span>

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

### <span data-ttu-id="03b31-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03b31-118">-ResourceGroupName</span></span>
<span data-ttu-id="03b31-119">前門的資源組名</span><span class="sxs-lookup"><span data-stu-id="03b31-119">The resource group name of the Front Door</span></span>

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

### <span data-ttu-id="03b31-120">-確認</span><span class="sxs-lookup"><span data-stu-id="03b31-120">-Confirm</span></span>
<span data-ttu-id="03b31-121">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="03b31-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03b31-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03b31-122">-WhatIf</span></span>
<span data-ttu-id="03b31-123">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="03b31-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03b31-124">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="03b31-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03b31-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03b31-125">CommonParameters</span></span>
<span data-ttu-id="03b31-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="03b31-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03b31-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="03b31-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03b31-128">輸入</span><span class="sxs-lookup"><span data-stu-id="03b31-128">INPUTS</span></span>

### <span data-ttu-id="03b31-129">沒有</span><span class="sxs-lookup"><span data-stu-id="03b31-129">None</span></span>

## <span data-ttu-id="03b31-130">輸出</span><span class="sxs-lookup"><span data-stu-id="03b31-130">OUTPUTS</span></span>

### <span data-ttu-id="03b31-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="03b31-131">System.Boolean</span></span>

## <span data-ttu-id="03b31-132">筆記</span><span class="sxs-lookup"><span data-stu-id="03b31-132">NOTES</span></span>

## <span data-ttu-id="03b31-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="03b31-133">RELATED LINKS</span></span>
