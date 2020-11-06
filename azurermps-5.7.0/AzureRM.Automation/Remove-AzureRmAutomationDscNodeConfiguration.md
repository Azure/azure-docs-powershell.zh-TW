---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6C6C7142-31CD-4245-BC55-CB7916EA12E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscNodeConfiguration.md
ms.openlocfilehash: 662ab70f3bda94e614742043521856d7a3fb99c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457475"
---
# <span data-ttu-id="1f978-101">Remove-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="1f978-101">Remove-AzureRmAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="1f978-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1f978-102">SYNOPSIS</span></span>
<span data-ttu-id="1f978-103">從自動化中的 DSC 節點設定中移除中繼資料。</span><span class="sxs-lookup"><span data-stu-id="1f978-103">Removes metadata from DSC node configurations in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f978-104">句法</span><span class="sxs-lookup"><span data-stu-id="1f978-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationDscNodeConfiguration [-Name] <String> [-Force] [-IgnoreNodeMappings]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f978-105">說明</span><span class="sxs-lookup"><span data-stu-id="1f978-105">DESCRIPTION</span></span>
<span data-ttu-id="1f978-106">**AzureRmAutomationDscNodeConfiguration** Cmdlet 會將中繼資料從 Ap 所需的 (狀態設定，從 Azure 自動化中的 DSC) 節點配置中移除。</span><span class="sxs-lookup"><span data-stu-id="1f978-106">The **Remove-AzureRmAutomationDscNodeConfiguration** cmdlet removes metadata from APS Desired State Configuration (DSC) node configurations in Azure Automation.</span></span>
<span data-ttu-id="1f978-107">自動化會將 DSC 節點設定儲存為受管理的物件格式， (MOF) 設定檔。</span><span class="sxs-lookup"><span data-stu-id="1f978-107">Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="1f978-108">示例</span><span class="sxs-lookup"><span data-stu-id="1f978-108">EXAMPLES</span></span>

## <span data-ttu-id="1f978-109">參數</span><span class="sxs-lookup"><span data-stu-id="1f978-109">PARAMETERS</span></span>

### <span data-ttu-id="1f978-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1f978-110">-AutomationAccountName</span></span>
<span data-ttu-id="1f978-111">指定包含此 Cmdlet 移除中繼資料之 DSC 節點配置之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="1f978-111">Specifies the name of an Automation account that contains the DSC node configurations for which this cmdlet removes metadata.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f978-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f978-112">-DefaultProfile</span></span>
<span data-ttu-id="1f978-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="1f978-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f978-114">-Force</span><span class="sxs-lookup"><span data-stu-id="1f978-114">-Force</span></span>
<span data-ttu-id="1f978-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="1f978-115">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f978-116">-IgnoreNodeMappings</span><span class="sxs-lookup"><span data-stu-id="1f978-116">-IgnoreNodeMappings</span></span>
<span data-ttu-id="1f978-117">表示此 Cmdlet 會忽略節點對應。</span><span class="sxs-lookup"><span data-stu-id="1f978-117">Indicates that this cmdlet ignores node mappings.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f978-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="1f978-118">-Name</span></span>
<span data-ttu-id="1f978-119">指定此 Cmdlet 移除中繼資料的 DSC 節點配置名稱。</span><span class="sxs-lookup"><span data-stu-id="1f978-119">Specifies the name of the DSC node configuration for which this cmdlet removes metadata.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NodeConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f978-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f978-120">-ResourceGroupName</span></span>
<span data-ttu-id="1f978-121">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1f978-121">Specifies the name of a resource group.</span></span>
<span data-ttu-id="1f978-122">這個 Cmdlet 會移除此參數指定之資源群組中的 DSC 節點配置中繼資料。</span><span class="sxs-lookup"><span data-stu-id="1f978-122">This cmdlet removes metadata for DSC node configurations in the resource group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f978-123">-確認</span><span class="sxs-lookup"><span data-stu-id="1f978-123">-Confirm</span></span>
<span data-ttu-id="1f978-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1f978-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f978-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f978-125">-WhatIf</span></span>
<span data-ttu-id="1f978-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1f978-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f978-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1f978-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f978-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f978-128">CommonParameters</span></span>
<span data-ttu-id="1f978-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1f978-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f978-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1f978-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f978-131">輸入</span><span class="sxs-lookup"><span data-stu-id="1f978-131">INPUTS</span></span>

### <span data-ttu-id="1f978-132">所有</span><span class="sxs-lookup"><span data-stu-id="1f978-132">None</span></span>
<span data-ttu-id="1f978-133">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="1f978-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1f978-134">輸出</span><span class="sxs-lookup"><span data-stu-id="1f978-134">OUTPUTS</span></span>

## <span data-ttu-id="1f978-135">筆記</span><span class="sxs-lookup"><span data-stu-id="1f978-135">NOTES</span></span>

## <span data-ttu-id="1f978-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="1f978-136">RELATED LINKS</span></span>

[<span data-ttu-id="1f978-137">AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="1f978-137">Get-AzureRmAutomationDscNodeConfiguration</span></span>](./Get-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="1f978-138">匯入-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="1f978-138">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="1f978-139">Azure 自動化 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1f978-139">Azure Automation Cmdlets</span></span>](./AzureRM.Automation.md)


