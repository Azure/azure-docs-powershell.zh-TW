---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 6140E973-D7AB-4A28-A4FA-818E08129372
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzAutoscaleSetting.md
ms.openlocfilehash: c5fcd5f4e331c55fb95a0d8657a59a944be585c5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622244"
---
# <span data-ttu-id="85a8c-101">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="85a8c-101">Remove-AzAutoscaleSetting</span></span>

## <span data-ttu-id="85a8c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="85a8c-102">SYNOPSIS</span></span>
<span data-ttu-id="85a8c-103">移除自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="85a8c-103">Removes an Autoscale setting.</span></span>

## <span data-ttu-id="85a8c-104">句法</span><span class="sxs-lookup"><span data-stu-id="85a8c-104">SYNTAX</span></span>

```
Remove-AzAutoscaleSetting -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85a8c-105">說明</span><span class="sxs-lookup"><span data-stu-id="85a8c-105">DESCRIPTION</span></span>
<span data-ttu-id="85a8c-106">**AzAutoscaleSetting** Cmdlet 會移除自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="85a8c-106">The **Remove-AzAutoscaleSetting** cmdlet removes an Autoscale setting.</span></span>
<span data-ttu-id="85a8c-107">您必須指定設定的名稱，以及其所指派之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="85a8c-107">You must specify the name of the setting and the name of the resource group to which it is assigned.</span></span>
<span data-ttu-id="85a8c-108">這個 Cmdlet 會實現 ShouldProcess 模式，亦即，在實際建立、修改或移除資源之前，它可能會要求使用者進行確認。</span><span class="sxs-lookup"><span data-stu-id="85a8c-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="85a8c-109">示例</span><span class="sxs-lookup"><span data-stu-id="85a8c-109">EXAMPLES</span></span>

## <span data-ttu-id="85a8c-110">參數</span><span class="sxs-lookup"><span data-stu-id="85a8c-110">PARAMETERS</span></span>

### <span data-ttu-id="85a8c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85a8c-111">-DefaultProfile</span></span>
<span data-ttu-id="85a8c-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="85a8c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="85a8c-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="85a8c-113">-Name</span></span>
<span data-ttu-id="85a8c-114">指定要移除的自動縮放設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="85a8c-114">Specifies the name of the Autoscale setting to remove.</span></span>

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

### <span data-ttu-id="85a8c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85a8c-115">-ResourceGroupName</span></span>
<span data-ttu-id="85a8c-116">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="85a8c-116">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85a8c-117">-確認</span><span class="sxs-lookup"><span data-stu-id="85a8c-117">-Confirm</span></span>
<span data-ttu-id="85a8c-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="85a8c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85a8c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85a8c-119">-WhatIf</span></span>
<span data-ttu-id="85a8c-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="85a8c-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="85a8c-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="85a8c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85a8c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85a8c-122">CommonParameters</span></span>
<span data-ttu-id="85a8c-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="85a8c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85a8c-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="85a8c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85a8c-125">輸入</span><span class="sxs-lookup"><span data-stu-id="85a8c-125">INPUTS</span></span>

### <span data-ttu-id="85a8c-126">System.object</span><span class="sxs-lookup"><span data-stu-id="85a8c-126">System.String</span></span>

## <span data-ttu-id="85a8c-127">輸出</span><span class="sxs-lookup"><span data-stu-id="85a8c-127">OUTPUTS</span></span>

### <span data-ttu-id="85a8c-128">AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="85a8c-128">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="85a8c-129">筆記</span><span class="sxs-lookup"><span data-stu-id="85a8c-129">NOTES</span></span>

## <span data-ttu-id="85a8c-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="85a8c-130">RELATED LINKS</span></span>

[<span data-ttu-id="85a8c-131">附加 AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="85a8c-131">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="85a8c-132">AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="85a8c-132">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)


