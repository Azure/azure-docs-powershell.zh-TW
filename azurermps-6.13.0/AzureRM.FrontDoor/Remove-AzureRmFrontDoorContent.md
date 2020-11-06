---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/remove-azurermfrontdoorcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoorContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoorContent.md
ms.openlocfilehash: c75d8bca528c954cf0612af3392fc79f3cd3b4a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93443823"
---
# <span data-ttu-id="47499-101">Remove-AzureRmFrontDoorContent</span><span class="sxs-lookup"><span data-stu-id="47499-101">Remove-AzureRmFrontDoorContent</span></span>

## <span data-ttu-id="47499-102">摘要</span><span class="sxs-lookup"><span data-stu-id="47499-102">SYNOPSIS</span></span>
<span data-ttu-id="47499-103">移除前門中的內容</span><span class="sxs-lookup"><span data-stu-id="47499-103">Remove contents in Front Door</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47499-104">句法</span><span class="sxs-lookup"><span data-stu-id="47499-104">SYNTAX</span></span>

```
Remove-AzureRmFrontDoorContent -ResourceGroupName <String> -Name <String> -ContentPath <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47499-105">說明</span><span class="sxs-lookup"><span data-stu-id="47499-105">DESCRIPTION</span></span>
<span data-ttu-id="47499-106">Remove-AzureRmFrontDoorContent 在前門中清除快取的內容</span><span class="sxs-lookup"><span data-stu-id="47499-106">Remove-AzureRmFrontDoorContent purges cached contents in a Front Door</span></span>

## <span data-ttu-id="47499-107">示例</span><span class="sxs-lookup"><span data-stu-id="47499-107">EXAMPLES</span></span>

### <span data-ttu-id="47499-108">範例1</span><span class="sxs-lookup"><span data-stu-id="47499-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmFrontDoorContent -ResourceGroupName $ResourceGroupName -Name $FrontDoorName -ContentPath "/*"
```

## <span data-ttu-id="47499-109">參數</span><span class="sxs-lookup"><span data-stu-id="47499-109">PARAMETERS</span></span>

### <span data-ttu-id="47499-110">-ContentPath</span><span class="sxs-lookup"><span data-stu-id="47499-110">-ContentPath</span></span>
<span data-ttu-id="47499-111">要清除之內容的路徑。</span><span class="sxs-lookup"><span data-stu-id="47499-111">The paths to the content to be purged.</span></span>

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

### <span data-ttu-id="47499-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47499-112">-DefaultProfile</span></span>
<span data-ttu-id="47499-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="47499-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47499-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="47499-114">-Name</span></span>
<span data-ttu-id="47499-115">前門名稱。</span><span class="sxs-lookup"><span data-stu-id="47499-115">Front Door name.</span></span>

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

### <span data-ttu-id="47499-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="47499-116">-PassThru</span></span>
<span data-ttu-id="47499-117">如果指定) ，則傳回物件 (。</span><span class="sxs-lookup"><span data-stu-id="47499-117">Return object (if specified).</span></span>

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

### <span data-ttu-id="47499-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47499-118">-ResourceGroupName</span></span>
<span data-ttu-id="47499-119">前門的資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="47499-119">The resource group name of the Front Door</span></span>

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

### <span data-ttu-id="47499-120">-確認</span><span class="sxs-lookup"><span data-stu-id="47499-120">-Confirm</span></span>
<span data-ttu-id="47499-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="47499-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47499-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47499-122">-WhatIf</span></span>
<span data-ttu-id="47499-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="47499-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47499-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="47499-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47499-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47499-125">CommonParameters</span></span>
<span data-ttu-id="47499-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="47499-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47499-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="47499-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47499-128">輸入</span><span class="sxs-lookup"><span data-stu-id="47499-128">INPUTS</span></span>

### <span data-ttu-id="47499-129">所有</span><span class="sxs-lookup"><span data-stu-id="47499-129">None</span></span>

## <span data-ttu-id="47499-130">輸出</span><span class="sxs-lookup"><span data-stu-id="47499-130">OUTPUTS</span></span>

### <span data-ttu-id="47499-131">System.object</span><span class="sxs-lookup"><span data-stu-id="47499-131">System.Boolean</span></span>

## <span data-ttu-id="47499-132">筆記</span><span class="sxs-lookup"><span data-stu-id="47499-132">NOTES</span></span>

## <span data-ttu-id="47499-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="47499-133">RELATED LINKS</span></span>
