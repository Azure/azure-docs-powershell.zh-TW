---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 848ce0e0c5608271f1f8facb955aad2df95b6a0a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127760"
---
# <span data-ttu-id="1d639-101">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d639-101">Remove-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="1d639-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1d639-102">SYNOPSIS</span></span>
<span data-ttu-id="1d639-103">移除整合帳戶批次設定。</span><span class="sxs-lookup"><span data-stu-id="1d639-103">Removes an integration account batch configuration.</span></span>

## <span data-ttu-id="1d639-104">句法</span><span class="sxs-lookup"><span data-stu-id="1d639-104">SYNTAX</span></span>

### <span data-ttu-id="1d639-105">ByIntegrationAccount (預設) </span><span class="sxs-lookup"><span data-stu-id="1d639-105">ByIntegrationAccount (Default)</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d639-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1d639-106">ByInputObject</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d639-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1d639-107">ByResourceId</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d639-108">說明</span><span class="sxs-lookup"><span data-stu-id="1d639-108">DESCRIPTION</span></span>
<span data-ttu-id="1d639-109">**AzIntegrationAccountBatchConfiguration** Cmdlet 會從整合帳戶中移除批次配置。</span><span class="sxs-lookup"><span data-stu-id="1d639-109">The **Remove-AzIntegrationAccountBatchConfiguration** cmdlet removes a batch configuration from an integration account.</span></span>

## <span data-ttu-id="1d639-110">示例</span><span class="sxs-lookup"><span data-stu-id="1d639-110">EXAMPLES</span></span>

### <span data-ttu-id="1d639-111">範例1：移除參數的批次設定</span><span class="sxs-lookup"><span data-stu-id="1d639-111">Example 1: Remove a batch configuration by parameters</span></span>
```powershell
PS C:\> Remove-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig"
```

<span data-ttu-id="1d639-112">移除集成帳戶 "sampleIntegrationAccount" 中名為 "sampleBatchConfig" 的批次配置。</span><span class="sxs-lookup"><span data-stu-id="1d639-112">Removes the batch configuration named "sampleBatchConfig" located in the integration account "sampleIntegrationAccount".</span></span>

## <span data-ttu-id="1d639-113">參數</span><span class="sxs-lookup"><span data-stu-id="1d639-113">PARAMETERS</span></span>

### <span data-ttu-id="1d639-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d639-114">-DefaultProfile</span></span>
<span data-ttu-id="1d639-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1d639-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d639-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d639-116">-InputObject</span></span>
<span data-ttu-id="1d639-117">整合帳戶批次配置。</span><span class="sxs-lookup"><span data-stu-id="1d639-117">An integration account batch configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d639-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="1d639-118">-Name</span></span>
<span data-ttu-id="1d639-119">整合帳戶批次配置名稱。</span><span class="sxs-lookup"><span data-stu-id="1d639-119">The integration account batch configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: BatchConfigurationName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d639-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="1d639-120">-ParentName</span></span>
<span data-ttu-id="1d639-121">整合帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="1d639-121">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d639-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1d639-122">-PassThru</span></span>
<span data-ttu-id="1d639-123">傳回命令是否成功。</span><span class="sxs-lookup"><span data-stu-id="1d639-123">Return whether the command was successful or not.</span></span>

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

### <span data-ttu-id="1d639-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d639-124">-ResourceGroupName</span></span>
<span data-ttu-id="1d639-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1d639-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d639-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1d639-126">-ResourceId</span></span>
<span data-ttu-id="1d639-127">整合帳戶批次配置資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1d639-127">The integration account batch configuration resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d639-128">-確認</span><span class="sxs-lookup"><span data-stu-id="1d639-128">-Confirm</span></span>
<span data-ttu-id="1d639-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1d639-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d639-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d639-130">-WhatIf</span></span>
<span data-ttu-id="1d639-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1d639-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1d639-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1d639-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d639-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d639-133">CommonParameters</span></span>
<span data-ttu-id="1d639-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1d639-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d639-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1d639-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d639-136">輸入</span><span class="sxs-lookup"><span data-stu-id="1d639-136">INPUTS</span></span>

### <span data-ttu-id="1d639-137">PSIntegrationAccountBatchConfiguration 中的 LogicApp。</span><span class="sxs-lookup"><span data-stu-id="1d639-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

### <span data-ttu-id="1d639-138">System.object</span><span class="sxs-lookup"><span data-stu-id="1d639-138">System.String</span></span>

## <span data-ttu-id="1d639-139">輸出</span><span class="sxs-lookup"><span data-stu-id="1d639-139">OUTPUTS</span></span>

### <span data-ttu-id="1d639-140">System.object</span><span class="sxs-lookup"><span data-stu-id="1d639-140">System.Boolean</span></span>

## <span data-ttu-id="1d639-141">筆記</span><span class="sxs-lookup"><span data-stu-id="1d639-141">NOTES</span></span>

## <span data-ttu-id="1d639-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="1d639-142">RELATED LINKS</span></span>
