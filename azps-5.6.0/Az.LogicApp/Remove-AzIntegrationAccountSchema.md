---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 56550997-21D9-4F85-B23A-677625482547
online version: https://docs.microsoft.com/powershell/module/az.logicapp/remove-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountSchema.md
ms.openlocfilehash: b66c14eced87cb56b5e8b57766b268a63dbdb088
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904401"
---
# <span data-ttu-id="70c59-101">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="70c59-101">Remove-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="70c59-102">簡介</span><span class="sxs-lookup"><span data-stu-id="70c59-102">SYNOPSIS</span></span>
<span data-ttu-id="70c59-103">移除整合帳戶架構。</span><span class="sxs-lookup"><span data-stu-id="70c59-103">Removes an integration account schema.</span></span>

## <span data-ttu-id="70c59-104">語法</span><span class="sxs-lookup"><span data-stu-id="70c59-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70c59-105">描述</span><span class="sxs-lookup"><span data-stu-id="70c59-105">DESCRIPTION</span></span>
<span data-ttu-id="70c59-106">**Remove-Az有AccountSchema Cmdlet** 會從資源群組移除整合帳戶架構。</span><span class="sxs-lookup"><span data-stu-id="70c59-106">The **Remove-AzIntegrationAccountSchema** cmdlet removes an integration account schema from a resource group.</span></span>
<span data-ttu-id="70c59-107">指定整合帳戶名稱、資源組名和架構名稱。</span><span class="sxs-lookup"><span data-stu-id="70c59-107">Specifying the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="70c59-108">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="70c59-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="70c59-109">若要使用動態參數，請于命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="70c59-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="70c59-110">若要探索動態參數的名稱，在 Cmdlet 名稱之後輸入連字號 (-) ，然後重複按 Tab 鍵以迴圈流覽可用的參數。</span><span class="sxs-lookup"><span data-stu-id="70c59-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="70c59-111">如果您省略必要的範本參數，Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="70c59-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="70c59-112">例子</span><span class="sxs-lookup"><span data-stu-id="70c59-112">EXAMPLES</span></span>

### <span data-ttu-id="70c59-113">範例 1：移除整合帳戶架構</span><span class="sxs-lookup"><span data-stu-id="70c59-113">Example 1: Remove an integration account schema</span></span>
```
PS C:\>Remove-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
```

<span data-ttu-id="70c59-114">此命令會移除名為 IntegrationAccountSchema43 的整合帳戶架構。</span><span class="sxs-lookup"><span data-stu-id="70c59-114">This command removes an integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="70c59-115">參數</span><span class="sxs-lookup"><span data-stu-id="70c59-115">PARAMETERS</span></span>

### <span data-ttu-id="70c59-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70c59-116">-DefaultProfile</span></span>
<span data-ttu-id="70c59-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="70c59-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="70c59-118">-強制</span><span class="sxs-lookup"><span data-stu-id="70c59-118">-Force</span></span>
<span data-ttu-id="70c59-119">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="70c59-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="70c59-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="70c59-120">-Name</span></span>
<span data-ttu-id="70c59-121">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="70c59-121">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="70c59-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70c59-122">-ResourceGroupName</span></span>
<span data-ttu-id="70c59-123">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="70c59-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="70c59-124">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="70c59-124">-SchemaName</span></span>
<span data-ttu-id="70c59-125">指定整合帳戶架構的名稱。</span><span class="sxs-lookup"><span data-stu-id="70c59-125">Specifies the name of an integration account schema.</span></span>

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

### <span data-ttu-id="70c59-126">-確認</span><span class="sxs-lookup"><span data-stu-id="70c59-126">-Confirm</span></span>
<span data-ttu-id="70c59-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="70c59-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70c59-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70c59-128">-WhatIf</span></span>
<span data-ttu-id="70c59-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="70c59-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70c59-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="70c59-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70c59-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70c59-131">CommonParameters</span></span>
<span data-ttu-id="70c59-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="70c59-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70c59-133">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="70c59-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70c59-134">輸入</span><span class="sxs-lookup"><span data-stu-id="70c59-134">INPUTS</span></span>

### <span data-ttu-id="70c59-135">System.String</span><span class="sxs-lookup"><span data-stu-id="70c59-135">System.String</span></span>

## <span data-ttu-id="70c59-136">輸出</span><span class="sxs-lookup"><span data-stu-id="70c59-136">OUTPUTS</span></span>

### <span data-ttu-id="70c59-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="70c59-137">System.Void</span></span>

## <span data-ttu-id="70c59-138">筆記</span><span class="sxs-lookup"><span data-stu-id="70c59-138">NOTES</span></span>

## <span data-ttu-id="70c59-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="70c59-139">RELATED LINKS</span></span>

[<span data-ttu-id="70c59-140">Get-AzCountSchema</span><span class="sxs-lookup"><span data-stu-id="70c59-140">Get-AzIntegrationAccountSchema</span></span>](./Get-AzIntegrationAccountSchema.md)

[<span data-ttu-id="70c59-141">New-AzCountSchema</span><span class="sxs-lookup"><span data-stu-id="70c59-141">New-AzIntegrationAccountSchema</span></span>](./New-AzIntegrationAccountSchema.md)

[<span data-ttu-id="70c59-142">Set-AzCountSchema</span><span class="sxs-lookup"><span data-stu-id="70c59-142">Set-AzIntegrationAccountSchema</span></span>](./Set-AzIntegrationAccountSchema.md)


