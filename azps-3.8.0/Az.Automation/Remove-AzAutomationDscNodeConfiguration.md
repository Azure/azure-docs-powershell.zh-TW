---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6C6C7142-31CD-4245-BC55-CB7916EA12E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationDscNodeConfiguration.md
ms.openlocfilehash: 28add3b4bffe808be5391de3ddbac759c36f5820
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93966378"
---
# <span data-ttu-id="7aeba-101">Remove-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="7aeba-101">Remove-AzAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="7aeba-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7aeba-102">SYNOPSIS</span></span>
<span data-ttu-id="7aeba-103">從自動化中的 DSC 節點設定中移除中繼資料。</span><span class="sxs-lookup"><span data-stu-id="7aeba-103">Removes metadata from DSC node configurations in Automation.</span></span>

## <span data-ttu-id="7aeba-104">句法</span><span class="sxs-lookup"><span data-stu-id="7aeba-104">SYNTAX</span></span>

```
Remove-AzAutomationDscNodeConfiguration [-Name] <String> [-Force] [-IgnoreNodeMappings]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7aeba-105">說明</span><span class="sxs-lookup"><span data-stu-id="7aeba-105">DESCRIPTION</span></span>
<span data-ttu-id="7aeba-106">**AzAutomationDscNodeConfiguration** Cmdlet 會將中繼資料從 Ap 所需的 (狀態設定，從 Azure 自動化中的 DSC) 節點配置中移除。</span><span class="sxs-lookup"><span data-stu-id="7aeba-106">The **Remove-AzAutomationDscNodeConfiguration** cmdlet removes metadata from APS Desired State Configuration (DSC) node configurations in Azure Automation.</span></span>
<span data-ttu-id="7aeba-107">自動化會將 DSC 節點設定儲存為受管理的物件格式， (MOF) 設定檔。</span><span class="sxs-lookup"><span data-stu-id="7aeba-107">Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="7aeba-108">示例</span><span class="sxs-lookup"><span data-stu-id="7aeba-108">EXAMPLES</span></span>

## <span data-ttu-id="7aeba-109">參數</span><span class="sxs-lookup"><span data-stu-id="7aeba-109">PARAMETERS</span></span>

### <span data-ttu-id="7aeba-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7aeba-110">-AutomationAccountName</span></span>
<span data-ttu-id="7aeba-111">指定包含此 Cmdlet 移除中繼資料之 DSC 節點配置之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="7aeba-111">Specifies the name of an Automation account that contains the DSC node configurations for which this cmdlet removes metadata.</span></span>

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

### <span data-ttu-id="7aeba-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7aeba-112">-DefaultProfile</span></span>
<span data-ttu-id="7aeba-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="7aeba-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7aeba-114">-Force</span><span class="sxs-lookup"><span data-stu-id="7aeba-114">-Force</span></span>
<span data-ttu-id="7aeba-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="7aeba-115">ps_force</span></span>

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

### <span data-ttu-id="7aeba-116">-IgnoreNodeMappings</span><span class="sxs-lookup"><span data-stu-id="7aeba-116">-IgnoreNodeMappings</span></span>
<span data-ttu-id="7aeba-117">表示此 Cmdlet 會忽略節點對應。</span><span class="sxs-lookup"><span data-stu-id="7aeba-117">Indicates that this cmdlet ignores node mappings.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7aeba-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="7aeba-118">-Name</span></span>
<span data-ttu-id="7aeba-119">指定此 Cmdlet 移除中繼資料的 DSC 節點配置名稱。</span><span class="sxs-lookup"><span data-stu-id="7aeba-119">Specifies the name of the DSC node configuration for which this cmdlet removes metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NodeConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7aeba-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7aeba-120">-ResourceGroupName</span></span>
<span data-ttu-id="7aeba-121">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7aeba-121">Specifies the name of a resource group.</span></span>
<span data-ttu-id="7aeba-122">這個 Cmdlet 會移除此參數指定之資源群組中的 DSC 節點配置中繼資料。</span><span class="sxs-lookup"><span data-stu-id="7aeba-122">This cmdlet removes metadata for DSC node configurations in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="7aeba-123">-確認</span><span class="sxs-lookup"><span data-stu-id="7aeba-123">-Confirm</span></span>
<span data-ttu-id="7aeba-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7aeba-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7aeba-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7aeba-125">-WhatIf</span></span>
<span data-ttu-id="7aeba-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7aeba-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7aeba-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7aeba-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7aeba-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7aeba-128">CommonParameters</span></span>
<span data-ttu-id="7aeba-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7aeba-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7aeba-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7aeba-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7aeba-131">輸入</span><span class="sxs-lookup"><span data-stu-id="7aeba-131">INPUTS</span></span>

### <span data-ttu-id="7aeba-132">System.object</span><span class="sxs-lookup"><span data-stu-id="7aeba-132">System.String</span></span>

## <span data-ttu-id="7aeba-133">輸出</span><span class="sxs-lookup"><span data-stu-id="7aeba-133">OUTPUTS</span></span>

### <span data-ttu-id="7aeba-134">System.void</span><span class="sxs-lookup"><span data-stu-id="7aeba-134">System.Void</span></span>

## <span data-ttu-id="7aeba-135">筆記</span><span class="sxs-lookup"><span data-stu-id="7aeba-135">NOTES</span></span>

## <span data-ttu-id="7aeba-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="7aeba-136">RELATED LINKS</span></span>

[<span data-ttu-id="7aeba-137">AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="7aeba-137">Get-AzAutomationDscNodeConfiguration</span></span>](./Get-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="7aeba-138">匯入-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="7aeba-138">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="7aeba-139">Azure 自動化 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7aeba-139">Azure Automation Cmdlets</span></span>](./Az.Automation.md)


