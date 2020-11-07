---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 56550997-21D9-4F85-B23A-677625482547
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountSchema.md
ms.openlocfilehash: 50eab845d20d9bf95c20e94f6309be2a302f413c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965783"
---
# <span data-ttu-id="95e12-101">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="95e12-101">Remove-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="95e12-102">摘要</span><span class="sxs-lookup"><span data-stu-id="95e12-102">SYNOPSIS</span></span>
<span data-ttu-id="95e12-103">移除整合帳戶架構。</span><span class="sxs-lookup"><span data-stu-id="95e12-103">Removes an integration account schema.</span></span>

## <span data-ttu-id="95e12-104">句法</span><span class="sxs-lookup"><span data-stu-id="95e12-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95e12-105">說明</span><span class="sxs-lookup"><span data-stu-id="95e12-105">DESCRIPTION</span></span>
<span data-ttu-id="95e12-106">**AzIntegrationAccountSchema** Cmdlet 會從資源群組中移除整合帳戶架構。</span><span class="sxs-lookup"><span data-stu-id="95e12-106">The **Remove-AzIntegrationAccountSchema** cmdlet removes an integration account schema from a resource group.</span></span>
<span data-ttu-id="95e12-107">指定整合帳戶名稱、資源群組名稱和架構名稱。</span><span class="sxs-lookup"><span data-stu-id="95e12-107">Specifying the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="95e12-108">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="95e12-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="95e12-109">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="95e12-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="95e12-110">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="95e12-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="95e12-111">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="95e12-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="95e12-112">示例</span><span class="sxs-lookup"><span data-stu-id="95e12-112">EXAMPLES</span></span>

### <span data-ttu-id="95e12-113">範例1：移除整合帳戶架構</span><span class="sxs-lookup"><span data-stu-id="95e12-113">Example 1: Remove an integration account schema</span></span>
```
PS C:\>Remove-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
```

<span data-ttu-id="95e12-114">這個命令會移除名為 IntegrationAccountSchema43 的整合帳戶架構。</span><span class="sxs-lookup"><span data-stu-id="95e12-114">This command removes an integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="95e12-115">參數</span><span class="sxs-lookup"><span data-stu-id="95e12-115">PARAMETERS</span></span>

### <span data-ttu-id="95e12-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95e12-116">-DefaultProfile</span></span>
<span data-ttu-id="95e12-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="95e12-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="95e12-118">-Force</span><span class="sxs-lookup"><span data-stu-id="95e12-118">-Force</span></span>
<span data-ttu-id="95e12-119">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="95e12-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="95e12-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="95e12-120">-Name</span></span>
<span data-ttu-id="95e12-121">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="95e12-121">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95e12-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95e12-122">-ResourceGroupName</span></span>
<span data-ttu-id="95e12-123">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="95e12-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="95e12-124">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="95e12-124">-SchemaName</span></span>
<span data-ttu-id="95e12-125">指定整合帳戶架構的名稱。</span><span class="sxs-lookup"><span data-stu-id="95e12-125">Specifies the name of an integration account schema.</span></span>

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

### <span data-ttu-id="95e12-126">-確認</span><span class="sxs-lookup"><span data-stu-id="95e12-126">-Confirm</span></span>
<span data-ttu-id="95e12-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="95e12-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95e12-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95e12-128">-WhatIf</span></span>
<span data-ttu-id="95e12-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="95e12-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95e12-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="95e12-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95e12-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95e12-131">CommonParameters</span></span>
<span data-ttu-id="95e12-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="95e12-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95e12-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="95e12-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95e12-134">輸入</span><span class="sxs-lookup"><span data-stu-id="95e12-134">INPUTS</span></span>

### <span data-ttu-id="95e12-135">System.object</span><span class="sxs-lookup"><span data-stu-id="95e12-135">System.String</span></span>

## <span data-ttu-id="95e12-136">輸出</span><span class="sxs-lookup"><span data-stu-id="95e12-136">OUTPUTS</span></span>

### <span data-ttu-id="95e12-137">System.void</span><span class="sxs-lookup"><span data-stu-id="95e12-137">System.Void</span></span>

## <span data-ttu-id="95e12-138">筆記</span><span class="sxs-lookup"><span data-stu-id="95e12-138">NOTES</span></span>

## <span data-ttu-id="95e12-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="95e12-139">RELATED LINKS</span></span>

[<span data-ttu-id="95e12-140">AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="95e12-140">Get-AzIntegrationAccountSchema</span></span>](./Get-AzIntegrationAccountSchema.md)

[<span data-ttu-id="95e12-141">新-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="95e12-141">New-AzIntegrationAccountSchema</span></span>](./New-AzIntegrationAccountSchema.md)

[<span data-ttu-id="95e12-142">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="95e12-142">Set-AzIntegrationAccountSchema</span></span>](./Set-AzIntegrationAccountSchema.md)


