---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorContent.md
ms.openlocfilehash: b7b01ec1b301741c07a0667931a63287cc503434
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100140875"
---
# <span data-ttu-id="afbc2-101">Remove-AzFrontDoorContent</span><span class="sxs-lookup"><span data-stu-id="afbc2-101">Remove-AzFrontDoorContent</span></span>

## <span data-ttu-id="afbc2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="afbc2-102">SYNOPSIS</span></span>
<span data-ttu-id="afbc2-103">移除前門中的內容</span><span class="sxs-lookup"><span data-stu-id="afbc2-103">Remove contents in Front Door</span></span>

## <span data-ttu-id="afbc2-104">句法</span><span class="sxs-lookup"><span data-stu-id="afbc2-104">SYNTAX</span></span>

```
Remove-AzFrontDoorContent -ResourceGroupName <String> -Name <String> -ContentPath <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afbc2-105">說明</span><span class="sxs-lookup"><span data-stu-id="afbc2-105">DESCRIPTION</span></span>
<span data-ttu-id="afbc2-106">Remove-AzFrontDoorContent 在前門中清除快取的內容</span><span class="sxs-lookup"><span data-stu-id="afbc2-106">Remove-AzFrontDoorContent purges cached contents in a Front Door</span></span>

## <span data-ttu-id="afbc2-107">示例</span><span class="sxs-lookup"><span data-stu-id="afbc2-107">EXAMPLES</span></span>

### <span data-ttu-id="afbc2-108">範例1</span><span class="sxs-lookup"><span data-stu-id="afbc2-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorContent -ResourceGroupName $ResourceGroupName -Name $FrontDoorName -ContentPath "/*"
```

## <span data-ttu-id="afbc2-109">參數</span><span class="sxs-lookup"><span data-stu-id="afbc2-109">PARAMETERS</span></span>

### <span data-ttu-id="afbc2-110">-ContentPath</span><span class="sxs-lookup"><span data-stu-id="afbc2-110">-ContentPath</span></span>
<span data-ttu-id="afbc2-111">要清除之內容的路徑。</span><span class="sxs-lookup"><span data-stu-id="afbc2-111">The paths to the content to be purged.</span></span>

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

### <span data-ttu-id="afbc2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afbc2-112">-DefaultProfile</span></span>
<span data-ttu-id="afbc2-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="afbc2-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afbc2-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="afbc2-114">-Name</span></span>
<span data-ttu-id="afbc2-115">前門名稱。</span><span class="sxs-lookup"><span data-stu-id="afbc2-115">Front Door name.</span></span>

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

### <span data-ttu-id="afbc2-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="afbc2-116">-PassThru</span></span>
<span data-ttu-id="afbc2-117">如果指定) ，則傳回物件 (。</span><span class="sxs-lookup"><span data-stu-id="afbc2-117">Return object (if specified).</span></span>

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

### <span data-ttu-id="afbc2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afbc2-118">-ResourceGroupName</span></span>
<span data-ttu-id="afbc2-119">前門的資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="afbc2-119">The resource group name of the Front Door</span></span>

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

### <span data-ttu-id="afbc2-120">-確認</span><span class="sxs-lookup"><span data-stu-id="afbc2-120">-Confirm</span></span>
<span data-ttu-id="afbc2-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="afbc2-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afbc2-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afbc2-122">-WhatIf</span></span>
<span data-ttu-id="afbc2-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="afbc2-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afbc2-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="afbc2-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afbc2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afbc2-125">CommonParameters</span></span>
<span data-ttu-id="afbc2-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="afbc2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afbc2-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="afbc2-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afbc2-128">輸入</span><span class="sxs-lookup"><span data-stu-id="afbc2-128">INPUTS</span></span>

### <span data-ttu-id="afbc2-129">所有</span><span class="sxs-lookup"><span data-stu-id="afbc2-129">None</span></span>

## <span data-ttu-id="afbc2-130">輸出</span><span class="sxs-lookup"><span data-stu-id="afbc2-130">OUTPUTS</span></span>

### <span data-ttu-id="afbc2-131">System.object</span><span class="sxs-lookup"><span data-stu-id="afbc2-131">System.Boolean</span></span>

## <span data-ttu-id="afbc2-132">筆記</span><span class="sxs-lookup"><span data-stu-id="afbc2-132">NOTES</span></span>

## <span data-ttu-id="afbc2-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="afbc2-133">RELATED LINKS</span></span>
