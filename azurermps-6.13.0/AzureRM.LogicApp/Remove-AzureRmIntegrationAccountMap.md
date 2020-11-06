---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 7AAF2ACC-84ED-449C-B1E8-F074463F44EB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountMap.md
ms.openlocfilehash: db3ff812c1c774feb07dd8ec688381cd29fa5cd2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449786"
---
# <span data-ttu-id="0dc18-101">Remove-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="0dc18-101">Remove-AzureRmIntegrationAccountMap</span></span>

## <span data-ttu-id="0dc18-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0dc18-102">SYNOPSIS</span></span>
<span data-ttu-id="0dc18-103">移除整合帳戶對應。</span><span class="sxs-lookup"><span data-stu-id="0dc18-103">Removes an integration account map.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0dc18-104">句法</span><span class="sxs-lookup"><span data-stu-id="0dc18-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0dc18-105">說明</span><span class="sxs-lookup"><span data-stu-id="0dc18-105">DESCRIPTION</span></span>
<span data-ttu-id="0dc18-106">**AzureRmIntegrationAccountMap** Cmdlet 會從資源群組中移除整合帳戶地圖。</span><span class="sxs-lookup"><span data-stu-id="0dc18-106">The **Remove-AzureRmIntegrationAccountMap** cmdlet removes an integration account map from a resource group.</span></span>
<span data-ttu-id="0dc18-107">指定整合帳戶名稱、資源群組名稱和地圖名稱。</span><span class="sxs-lookup"><span data-stu-id="0dc18-107">Specify the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="0dc18-108">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="0dc18-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="0dc18-109">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="0dc18-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="0dc18-110">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="0dc18-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="0dc18-111">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="0dc18-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="0dc18-112">示例</span><span class="sxs-lookup"><span data-stu-id="0dc18-112">EXAMPLES</span></span>

### <span data-ttu-id="0dc18-113">範例1：移除整合帳戶對應圖</span><span class="sxs-lookup"><span data-stu-id="0dc18-113">Example 1: Remove an integration account map</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47"
```

<span data-ttu-id="0dc18-114">這個命令會移除名為 IntegrationAccountMap47 的整合帳戶地圖。</span><span class="sxs-lookup"><span data-stu-id="0dc18-114">This command removes the integration account map named IntegrationAccountMap47.</span></span>

## <span data-ttu-id="0dc18-115">參數</span><span class="sxs-lookup"><span data-stu-id="0dc18-115">PARAMETERS</span></span>

### <span data-ttu-id="0dc18-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dc18-116">-DefaultProfile</span></span>
<span data-ttu-id="0dc18-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="0dc18-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0dc18-118">-Force</span><span class="sxs-lookup"><span data-stu-id="0dc18-118">-Force</span></span>
<span data-ttu-id="0dc18-119">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="0dc18-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0dc18-120">-MapName</span><span class="sxs-lookup"><span data-stu-id="0dc18-120">-MapName</span></span>
<span data-ttu-id="0dc18-121">指定整合帳戶對應的名稱。</span><span class="sxs-lookup"><span data-stu-id="0dc18-121">Specifies the name of the integration account map.</span></span>

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

### <span data-ttu-id="0dc18-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="0dc18-122">-Name</span></span>
<span data-ttu-id="0dc18-123">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="0dc18-123">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="0dc18-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0dc18-124">-ResourceGroupName</span></span>
<span data-ttu-id="0dc18-125">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0dc18-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="0dc18-126">-確認</span><span class="sxs-lookup"><span data-stu-id="0dc18-126">-Confirm</span></span>
<span data-ttu-id="0dc18-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0dc18-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0dc18-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0dc18-128">-WhatIf</span></span>
<span data-ttu-id="0dc18-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0dc18-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0dc18-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0dc18-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0dc18-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dc18-131">CommonParameters</span></span>
<span data-ttu-id="0dc18-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0dc18-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dc18-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0dc18-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dc18-134">輸入</span><span class="sxs-lookup"><span data-stu-id="0dc18-134">INPUTS</span></span>

### <span data-ttu-id="0dc18-135">System.object</span><span class="sxs-lookup"><span data-stu-id="0dc18-135">System.String</span></span>

## <span data-ttu-id="0dc18-136">輸出</span><span class="sxs-lookup"><span data-stu-id="0dc18-136">OUTPUTS</span></span>

### <span data-ttu-id="0dc18-137">System.void</span><span class="sxs-lookup"><span data-stu-id="0dc18-137">System.Void</span></span>

## <span data-ttu-id="0dc18-138">筆記</span><span class="sxs-lookup"><span data-stu-id="0dc18-138">NOTES</span></span>

## <span data-ttu-id="0dc18-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="0dc18-139">RELATED LINKS</span></span>

[<span data-ttu-id="0dc18-140">AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="0dc18-140">Get-AzureRmIntegrationAccountMap</span></span>](./Get-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="0dc18-141">新-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="0dc18-141">New-AzureRmIntegrationAccountMap</span></span>](./New-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="0dc18-142">Set-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="0dc18-142">Set-AzureRmIntegrationAccountMap</span></span>](./Set-AzureRmIntegrationAccountMap.md)


