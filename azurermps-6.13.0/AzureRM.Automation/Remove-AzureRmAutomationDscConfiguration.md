---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6389EE2A-12B5-46A1-A2B9-4B3CF5A55A30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: e5d7f6c75624fcfb15fa08718acc24e02336cb5e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623771"
---
# <span data-ttu-id="9c83d-101">Remove-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="9c83d-101">Remove-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="9c83d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9c83d-102">SYNOPSIS</span></span>
<span data-ttu-id="9c83d-103">從自動化中移除 DSC 配置。</span><span class="sxs-lookup"><span data-stu-id="9c83d-103">Removes DSC configurations from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c83d-104">句法</span><span class="sxs-lookup"><span data-stu-id="9c83d-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationDscConfiguration [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9c83d-105">說明</span><span class="sxs-lookup"><span data-stu-id="9c83d-105">DESCRIPTION</span></span>
<span data-ttu-id="9c83d-106">**AzureRmAutomationDscConfiguration** Cmdlet 會從 Azure 自動化 (DSC) 配置中移除 Ap 所需的狀態設定。</span><span class="sxs-lookup"><span data-stu-id="9c83d-106">The **Remove-AzureRmAutomationDscConfiguration** cmdlet removes APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="9c83d-107">示例</span><span class="sxs-lookup"><span data-stu-id="9c83d-107">EXAMPLES</span></span>

## <span data-ttu-id="9c83d-108">參數</span><span class="sxs-lookup"><span data-stu-id="9c83d-108">PARAMETERS</span></span>

### <span data-ttu-id="9c83d-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9c83d-109">-AutomationAccountName</span></span>
<span data-ttu-id="9c83d-110">指定包含此 Cmdlet 移除之 DSC 設定的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="9c83d-110">Specifies the name of the Automation account that contains DSC configurations that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9c83d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c83d-111">-DefaultProfile</span></span>
<span data-ttu-id="9c83d-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="9c83d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9c83d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="9c83d-113">-Force</span></span>
<span data-ttu-id="9c83d-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="9c83d-114">ps_force</span></span>

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

### <span data-ttu-id="9c83d-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="9c83d-115">-Name</span></span>
<span data-ttu-id="9c83d-116">指定此 Cmdlet 移除的 DSC 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="9c83d-116">Specifies the name of the DSC configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9c83d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c83d-117">-ResourceGroupName</span></span>
<span data-ttu-id="9c83d-118">指定此 Cmdlet 取得 DSC 設定之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9c83d-118">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="9c83d-119">-確認</span><span class="sxs-lookup"><span data-stu-id="9c83d-119">-Confirm</span></span>
<span data-ttu-id="9c83d-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9c83d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c83d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c83d-121">-WhatIf</span></span>
<span data-ttu-id="9c83d-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9c83d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c83d-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9c83d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c83d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c83d-124">CommonParameters</span></span>
<span data-ttu-id="9c83d-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9c83d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c83d-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9c83d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c83d-127">輸入</span><span class="sxs-lookup"><span data-stu-id="9c83d-127">INPUTS</span></span>

### <span data-ttu-id="9c83d-128">System.object</span><span class="sxs-lookup"><span data-stu-id="9c83d-128">System.String</span></span>

## <span data-ttu-id="9c83d-129">輸出</span><span class="sxs-lookup"><span data-stu-id="9c83d-129">OUTPUTS</span></span>

### <span data-ttu-id="9c83d-130">System.void</span><span class="sxs-lookup"><span data-stu-id="9c83d-130">System.Void</span></span>

## <span data-ttu-id="9c83d-131">筆記</span><span class="sxs-lookup"><span data-stu-id="9c83d-131">NOTES</span></span>

## <span data-ttu-id="9c83d-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="9c83d-132">RELATED LINKS</span></span>

[<span data-ttu-id="9c83d-133">Export-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="9c83d-133">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="9c83d-134">AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="9c83d-134">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="9c83d-135">匯入-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="9c83d-135">Import-AzureRmAutomationDscConfiguration</span></span>](./Import-AzureRmAutomationDscConfiguration.md)


