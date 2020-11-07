---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6389EE2A-12B5-46A1-A2B9-4B3CF5A55A30
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationDscConfiguration.md
ms.openlocfilehash: bd418037f29aefc27d92ccebe1f34024728c77c9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93966380"
---
# <span data-ttu-id="fc144-101">Remove-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="fc144-101">Remove-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="fc144-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fc144-102">SYNOPSIS</span></span>
<span data-ttu-id="fc144-103">從自動化中移除 DSC 配置。</span><span class="sxs-lookup"><span data-stu-id="fc144-103">Removes DSC configurations from Automation.</span></span>

## <span data-ttu-id="fc144-104">句法</span><span class="sxs-lookup"><span data-stu-id="fc144-104">SYNTAX</span></span>

```
Remove-AzAutomationDscConfiguration [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fc144-105">說明</span><span class="sxs-lookup"><span data-stu-id="fc144-105">DESCRIPTION</span></span>
<span data-ttu-id="fc144-106">**AzAutomationDscConfiguration** Cmdlet 會從 Azure 自動化 (DSC) 配置中移除 Ap 所需的狀態設定。</span><span class="sxs-lookup"><span data-stu-id="fc144-106">The **Remove-AzAutomationDscConfiguration** cmdlet removes APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="fc144-107">示例</span><span class="sxs-lookup"><span data-stu-id="fc144-107">EXAMPLES</span></span>

## <span data-ttu-id="fc144-108">參數</span><span class="sxs-lookup"><span data-stu-id="fc144-108">PARAMETERS</span></span>

### <span data-ttu-id="fc144-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fc144-109">-AutomationAccountName</span></span>
<span data-ttu-id="fc144-110">指定包含此 Cmdlet 移除之 DSC 設定的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="fc144-110">Specifies the name of the Automation account that contains DSC configurations that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc144-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc144-111">-DefaultProfile</span></span>
<span data-ttu-id="fc144-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="fc144-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc144-113">-Force</span><span class="sxs-lookup"><span data-stu-id="fc144-113">-Force</span></span>
<span data-ttu-id="fc144-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="fc144-114">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc144-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="fc144-115">-Name</span></span>
<span data-ttu-id="fc144-116">指定此 Cmdlet 移除的 DSC 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="fc144-116">Specifies the name of the DSC configuration that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc144-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc144-117">-ResourceGroupName</span></span>
<span data-ttu-id="fc144-118">指定此 Cmdlet 取得 DSC 設定之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fc144-118">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc144-119">-確認</span><span class="sxs-lookup"><span data-stu-id="fc144-119">-Confirm</span></span>
<span data-ttu-id="fc144-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fc144-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc144-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc144-121">-WhatIf</span></span>
<span data-ttu-id="fc144-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fc144-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc144-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fc144-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc144-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc144-124">CommonParameters</span></span>
<span data-ttu-id="fc144-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fc144-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc144-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fc144-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc144-127">輸入</span><span class="sxs-lookup"><span data-stu-id="fc144-127">INPUTS</span></span>

### <span data-ttu-id="fc144-128">System.object</span><span class="sxs-lookup"><span data-stu-id="fc144-128">System.String</span></span>

## <span data-ttu-id="fc144-129">輸出</span><span class="sxs-lookup"><span data-stu-id="fc144-129">OUTPUTS</span></span>

### <span data-ttu-id="fc144-130">System.void</span><span class="sxs-lookup"><span data-stu-id="fc144-130">System.Void</span></span>

## <span data-ttu-id="fc144-131">筆記</span><span class="sxs-lookup"><span data-stu-id="fc144-131">NOTES</span></span>

## <span data-ttu-id="fc144-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="fc144-132">RELATED LINKS</span></span>

[<span data-ttu-id="fc144-133">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="fc144-133">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="fc144-134">AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="fc144-134">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)

[<span data-ttu-id="fc144-135">匯入-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="fc144-135">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)


