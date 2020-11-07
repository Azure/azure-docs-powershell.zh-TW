---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 56550997-21D9-4F85-B23A-677625482547
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountSchema.md
ms.openlocfilehash: a1a34ca669b12ee815655531c33b6cdba519016c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626150"
---
# <span data-ttu-id="bd342-101">Remove-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="bd342-101">Remove-AzureRmIntegrationAccountSchema</span></span>

## <span data-ttu-id="bd342-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bd342-102">SYNOPSIS</span></span>
<span data-ttu-id="bd342-103">移除整合帳戶架構。</span><span class="sxs-lookup"><span data-stu-id="bd342-103">Removes an integration account schema.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd342-104">句法</span><span class="sxs-lookup"><span data-stu-id="bd342-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd342-105">說明</span><span class="sxs-lookup"><span data-stu-id="bd342-105">DESCRIPTION</span></span>
<span data-ttu-id="bd342-106">**AzureRmIntegrationAccountSchema** Cmdlet 會從資源群組中移除整合帳戶架構。</span><span class="sxs-lookup"><span data-stu-id="bd342-106">The **Remove-AzureRmIntegrationAccountSchema** cmdlet removes an integration account schema from a resource group.</span></span>
<span data-ttu-id="bd342-107">指定整合帳戶名稱、資源群組名稱和架構名稱。</span><span class="sxs-lookup"><span data-stu-id="bd342-107">Specifying the integration account name, resource group name, and schema name.</span></span>

<span data-ttu-id="bd342-108">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="bd342-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="bd342-109">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="bd342-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="bd342-110">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="bd342-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="bd342-111">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="bd342-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="bd342-112">示例</span><span class="sxs-lookup"><span data-stu-id="bd342-112">EXAMPLES</span></span>

### <span data-ttu-id="bd342-113">範例1：移除整合帳戶架構</span><span class="sxs-lookup"><span data-stu-id="bd342-113">Example 1: Remove an integration account schema</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
```

<span data-ttu-id="bd342-114">這個命令會移除名為 IntegrationAccountSchema43 的整合帳戶架構。</span><span class="sxs-lookup"><span data-stu-id="bd342-114">This command removes an integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="bd342-115">參數</span><span class="sxs-lookup"><span data-stu-id="bd342-115">PARAMETERS</span></span>

### <span data-ttu-id="bd342-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd342-116">-DefaultProfile</span></span>
<span data-ttu-id="bd342-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="bd342-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bd342-118">-Force</span><span class="sxs-lookup"><span data-stu-id="bd342-118">-Force</span></span>
<span data-ttu-id="bd342-119">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="bd342-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd342-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="bd342-120">-Name</span></span>
<span data-ttu-id="bd342-121">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="bd342-121">Specifies the name of the integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd342-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd342-122">-ResourceGroupName</span></span>
<span data-ttu-id="bd342-123">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bd342-123">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd342-124">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="bd342-124">-SchemaName</span></span>
<span data-ttu-id="bd342-125">指定整合帳戶架構的名稱。</span><span class="sxs-lookup"><span data-stu-id="bd342-125">Specifies the name of an integration account schema.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd342-126">-確認</span><span class="sxs-lookup"><span data-stu-id="bd342-126">-Confirm</span></span>
<span data-ttu-id="bd342-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bd342-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd342-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd342-128">-WhatIf</span></span>
<span data-ttu-id="bd342-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bd342-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd342-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bd342-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd342-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd342-131">CommonParameters</span></span>
<span data-ttu-id="bd342-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bd342-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd342-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bd342-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd342-134">輸入</span><span class="sxs-lookup"><span data-stu-id="bd342-134">INPUTS</span></span>

### <span data-ttu-id="bd342-135">所有</span><span class="sxs-lookup"><span data-stu-id="bd342-135">None</span></span>
<span data-ttu-id="bd342-136">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="bd342-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bd342-137">輸出</span><span class="sxs-lookup"><span data-stu-id="bd342-137">OUTPUTS</span></span>

## <span data-ttu-id="bd342-138">筆記</span><span class="sxs-lookup"><span data-stu-id="bd342-138">NOTES</span></span>

## <span data-ttu-id="bd342-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="bd342-139">RELATED LINKS</span></span>

[<span data-ttu-id="bd342-140">AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="bd342-140">Get-AzureRmIntegrationAccountSchema</span></span>](./Get-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="bd342-141">新-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="bd342-141">New-AzureRmIntegrationAccountSchema</span></span>](./New-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="bd342-142">Set-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="bd342-142">Set-AzureRmIntegrationAccountSchema</span></span>](./Set-AzureRmIntegrationAccountSchema.md)

