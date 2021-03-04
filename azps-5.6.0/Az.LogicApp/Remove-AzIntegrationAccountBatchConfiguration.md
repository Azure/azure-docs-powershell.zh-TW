---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/remove-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 24c5f3b93b2be446eed4e5b81e1e69bf2116aa8b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904414"
---
# <span data-ttu-id="7c0df-101">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7c0df-101">Remove-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="7c0df-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7c0df-102">SYNOPSIS</span></span>
<span data-ttu-id="7c0df-103">移除整合帳戶批次組組。</span><span class="sxs-lookup"><span data-stu-id="7c0df-103">Removes an integration account batch configuration.</span></span>

## <span data-ttu-id="7c0df-104">語法</span><span class="sxs-lookup"><span data-stu-id="7c0df-104">SYNTAX</span></span>

### <span data-ttu-id="7c0df-105">By方Account (預設) </span><span class="sxs-lookup"><span data-stu-id="7c0df-105">ByIntegrationAccount (Default)</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c0df-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7c0df-106">ByInputObject</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c0df-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7c0df-107">ByResourceId</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c0df-108">描述</span><span class="sxs-lookup"><span data-stu-id="7c0df-108">DESCRIPTION</span></span>
<span data-ttu-id="7c0df-109">**Remove-Az有AccountBatchConfiguration Cmdlet** 會從整合帳戶移除批次組配置。</span><span class="sxs-lookup"><span data-stu-id="7c0df-109">The **Remove-AzIntegrationAccountBatchConfiguration** cmdlet removes a batch configuration from an integration account.</span></span>

## <span data-ttu-id="7c0df-110">例子</span><span class="sxs-lookup"><span data-stu-id="7c0df-110">EXAMPLES</span></span>

### <span data-ttu-id="7c0df-111">範例 1：根據參數移除批次設定</span><span class="sxs-lookup"><span data-stu-id="7c0df-111">Example 1: Remove a batch configuration by parameters</span></span>
```powershell
PS C:\> Remove-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig"
```

<span data-ttu-id="7c0df-112">移除名為"sampleBatchConfig"的批次組組，該批次組組位於整合帳戶 "sample準備Account"。</span><span class="sxs-lookup"><span data-stu-id="7c0df-112">Removes the batch configuration named "sampleBatchConfig" located in the integration account "sampleIntegrationAccount".</span></span>

## <span data-ttu-id="7c0df-113">參數</span><span class="sxs-lookup"><span data-stu-id="7c0df-113">PARAMETERS</span></span>

### <span data-ttu-id="7c0df-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c0df-114">-DefaultProfile</span></span>
<span data-ttu-id="7c0df-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7c0df-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c0df-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c0df-116">-InputObject</span></span>
<span data-ttu-id="7c0df-117">整合帳戶批次組組。</span><span class="sxs-lookup"><span data-stu-id="7c0df-117">An integration account batch configuration.</span></span>

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

### <span data-ttu-id="7c0df-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="7c0df-118">-Name</span></span>
<span data-ttu-id="7c0df-119">整合帳戶批次組組名稱。</span><span class="sxs-lookup"><span data-stu-id="7c0df-119">The integration account batch configuration name.</span></span>

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

### <span data-ttu-id="7c0df-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="7c0df-120">-ParentName</span></span>
<span data-ttu-id="7c0df-121">整合帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="7c0df-121">The integration account name.</span></span>

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

### <span data-ttu-id="7c0df-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c0df-122">-PassThru</span></span>
<span data-ttu-id="7c0df-123">返回命令是否成功。</span><span class="sxs-lookup"><span data-stu-id="7c0df-123">Return whether the command was successful or not.</span></span>

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

### <span data-ttu-id="7c0df-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c0df-124">-ResourceGroupName</span></span>
<span data-ttu-id="7c0df-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="7c0df-125">The resource group name.</span></span>

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

### <span data-ttu-id="7c0df-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c0df-126">-ResourceId</span></span>
<span data-ttu-id="7c0df-127">整合帳戶批次組組資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="7c0df-127">The integration account batch configuration resource id.</span></span>

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

### <span data-ttu-id="7c0df-128">-確認</span><span class="sxs-lookup"><span data-stu-id="7c0df-128">-Confirm</span></span>
<span data-ttu-id="7c0df-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7c0df-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c0df-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c0df-130">-WhatIf</span></span>
<span data-ttu-id="7c0df-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7c0df-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7c0df-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7c0df-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c0df-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c0df-133">CommonParameters</span></span>
<span data-ttu-id="7c0df-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7c0df-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c0df-135">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="7c0df-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c0df-136">輸入</span><span class="sxs-lookup"><span data-stu-id="7c0df-136">INPUTS</span></span>

### <span data-ttu-id="7c0df-137">Microsoft.Azure.Commands.LogicApp.models.PS方AccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7c0df-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

### <span data-ttu-id="7c0df-138">System.String</span><span class="sxs-lookup"><span data-stu-id="7c0df-138">System.String</span></span>

## <span data-ttu-id="7c0df-139">輸出</span><span class="sxs-lookup"><span data-stu-id="7c0df-139">OUTPUTS</span></span>

### <span data-ttu-id="7c0df-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7c0df-140">System.Boolean</span></span>

## <span data-ttu-id="7c0df-141">筆記</span><span class="sxs-lookup"><span data-stu-id="7c0df-141">NOTES</span></span>

## <span data-ttu-id="7c0df-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="7c0df-142">RELATED LINKS</span></span>
