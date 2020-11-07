---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 56550997-21D9-4F85-B23A-677625482547
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountSchema.md
ms.openlocfilehash: fc7acc34a018361b3ebaff67e57221c250e19771
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625160"
---
# <span data-ttu-id="8f65f-101">Remove-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="8f65f-101">Remove-AzureRmIntegrationAccountSchema</span></span>

## <span data-ttu-id="8f65f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8f65f-102">SYNOPSIS</span></span>
<span data-ttu-id="8f65f-103">移除整合帳戶架構。</span><span class="sxs-lookup"><span data-stu-id="8f65f-103">Removes an integration account schema.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f65f-104">句法</span><span class="sxs-lookup"><span data-stu-id="8f65f-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f65f-105">說明</span><span class="sxs-lookup"><span data-stu-id="8f65f-105">DESCRIPTION</span></span>
<span data-ttu-id="8f65f-106">**AzureRmIntegrationAccountSchema** Cmdlet 會從資源群組中移除整合帳戶架構。</span><span class="sxs-lookup"><span data-stu-id="8f65f-106">The **Remove-AzureRmIntegrationAccountSchema** cmdlet removes an integration account schema from a resource group.</span></span>
<span data-ttu-id="8f65f-107">指定整合帳戶名稱、資源群組名稱和架構名稱。</span><span class="sxs-lookup"><span data-stu-id="8f65f-107">Specifying the integration account name, resource group name, and schema name.</span></span>

<span data-ttu-id="8f65f-108">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="8f65f-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="8f65f-109">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="8f65f-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="8f65f-110">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="8f65f-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="8f65f-111">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="8f65f-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="8f65f-112">示例</span><span class="sxs-lookup"><span data-stu-id="8f65f-112">EXAMPLES</span></span>

### <span data-ttu-id="8f65f-113">範例1：移除整合帳戶架構</span><span class="sxs-lookup"><span data-stu-id="8f65f-113">Example 1: Remove an integration account schema</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
```

<span data-ttu-id="8f65f-114">這個命令會移除名為 IntegrationAccountSchema43 的整合帳戶架構。</span><span class="sxs-lookup"><span data-stu-id="8f65f-114">This command removes an integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="8f65f-115">參數</span><span class="sxs-lookup"><span data-stu-id="8f65f-115">PARAMETERS</span></span>

### <span data-ttu-id="8f65f-116">-Force</span><span class="sxs-lookup"><span data-stu-id="8f65f-116">-Force</span></span>
<span data-ttu-id="8f65f-117">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="8f65f-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8f65f-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="8f65f-118">-Name</span></span>
<span data-ttu-id="8f65f-119">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="8f65f-119">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="8f65f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f65f-120">-ResourceGroupName</span></span>
<span data-ttu-id="8f65f-121">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8f65f-121">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8f65f-122">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="8f65f-122">-SchemaName</span></span>
<span data-ttu-id="8f65f-123">指定整合帳戶架構的名稱。</span><span class="sxs-lookup"><span data-stu-id="8f65f-123">Specifies the name of an integration account schema.</span></span>

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

### <span data-ttu-id="8f65f-124">-確認</span><span class="sxs-lookup"><span data-stu-id="8f65f-124">-Confirm</span></span>
<span data-ttu-id="8f65f-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8f65f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f65f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f65f-126">-WhatIf</span></span>
<span data-ttu-id="8f65f-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8f65f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f65f-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8f65f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f65f-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f65f-129">-DefaultProfile</span></span>
<span data-ttu-id="8f65f-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8f65f-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f65f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f65f-131">CommonParameters</span></span>
<span data-ttu-id="8f65f-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8f65f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f65f-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8f65f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f65f-134">輸入</span><span class="sxs-lookup"><span data-stu-id="8f65f-134">INPUTS</span></span>

## <span data-ttu-id="8f65f-135">輸出</span><span class="sxs-lookup"><span data-stu-id="8f65f-135">OUTPUTS</span></span>

## <span data-ttu-id="8f65f-136">筆記</span><span class="sxs-lookup"><span data-stu-id="8f65f-136">NOTES</span></span>

## <span data-ttu-id="8f65f-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="8f65f-137">RELATED LINKS</span></span>

[<span data-ttu-id="8f65f-138">AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="8f65f-138">Get-AzureRmIntegrationAccountSchema</span></span>](./Get-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="8f65f-139">新-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="8f65f-139">New-AzureRmIntegrationAccountSchema</span></span>](./New-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="8f65f-140">Set-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="8f65f-140">Set-AzureRmIntegrationAccountSchema</span></span>](./Set-AzureRmIntegrationAccountSchema.md)


