---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 7AAF2ACC-84ED-449C-B1E8-F074463F44EB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountMap.md
ms.openlocfilehash: 769a92f9cd164ef2b3754a84d7a948f3bedd05da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447074"
---
# <span data-ttu-id="3954e-101">Remove-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="3954e-101">Remove-AzureRmIntegrationAccountMap</span></span>

## <span data-ttu-id="3954e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3954e-102">SYNOPSIS</span></span>
<span data-ttu-id="3954e-103">移除整合帳戶對應。</span><span class="sxs-lookup"><span data-stu-id="3954e-103">Removes an integration account map.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3954e-104">句法</span><span class="sxs-lookup"><span data-stu-id="3954e-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3954e-105">說明</span><span class="sxs-lookup"><span data-stu-id="3954e-105">DESCRIPTION</span></span>
<span data-ttu-id="3954e-106">**AzureRmIntegrationAccountMap** Cmdlet 會從資源群組中移除整合帳戶地圖。</span><span class="sxs-lookup"><span data-stu-id="3954e-106">The **Remove-AzureRmIntegrationAccountMap** cmdlet removes an integration account map from a resource group.</span></span>
<span data-ttu-id="3954e-107">指定整合帳戶名稱、資源群組名稱和地圖名稱。</span><span class="sxs-lookup"><span data-stu-id="3954e-107">Specify the integration account name, resource group name, and map name.</span></span>

<span data-ttu-id="3954e-108">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="3954e-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="3954e-109">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="3954e-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="3954e-110">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="3954e-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="3954e-111">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="3954e-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="3954e-112">示例</span><span class="sxs-lookup"><span data-stu-id="3954e-112">EXAMPLES</span></span>

### <span data-ttu-id="3954e-113">範例1：移除整合帳戶對應圖</span><span class="sxs-lookup"><span data-stu-id="3954e-113">Example 1: Remove an integration account map</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47"
```

<span data-ttu-id="3954e-114">這個命令會移除名為 IntegrationAccountMap47 的整合帳戶地圖。</span><span class="sxs-lookup"><span data-stu-id="3954e-114">This command removes the integration account map named IntegrationAccountMap47.</span></span>

## <span data-ttu-id="3954e-115">參數</span><span class="sxs-lookup"><span data-stu-id="3954e-115">PARAMETERS</span></span>

### <span data-ttu-id="3954e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3954e-116">-DefaultProfile</span></span>
<span data-ttu-id="3954e-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="3954e-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3954e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="3954e-118">-Force</span></span>
<span data-ttu-id="3954e-119">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="3954e-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3954e-120">-MapName</span><span class="sxs-lookup"><span data-stu-id="3954e-120">-MapName</span></span>
<span data-ttu-id="3954e-121">指定整合帳戶對應的名稱。</span><span class="sxs-lookup"><span data-stu-id="3954e-121">Specifies the name of the integration account map.</span></span>

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

### <span data-ttu-id="3954e-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="3954e-122">-Name</span></span>
<span data-ttu-id="3954e-123">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="3954e-123">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="3954e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3954e-124">-ResourceGroupName</span></span>
<span data-ttu-id="3954e-125">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3954e-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3954e-126">-確認</span><span class="sxs-lookup"><span data-stu-id="3954e-126">-Confirm</span></span>
<span data-ttu-id="3954e-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3954e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3954e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3954e-128">-WhatIf</span></span>
<span data-ttu-id="3954e-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3954e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3954e-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3954e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3954e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3954e-131">CommonParameters</span></span>
<span data-ttu-id="3954e-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3954e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3954e-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3954e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3954e-134">輸入</span><span class="sxs-lookup"><span data-stu-id="3954e-134">INPUTS</span></span>

### <span data-ttu-id="3954e-135">所有</span><span class="sxs-lookup"><span data-stu-id="3954e-135">None</span></span>
<span data-ttu-id="3954e-136">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="3954e-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3954e-137">輸出</span><span class="sxs-lookup"><span data-stu-id="3954e-137">OUTPUTS</span></span>

## <span data-ttu-id="3954e-138">筆記</span><span class="sxs-lookup"><span data-stu-id="3954e-138">NOTES</span></span>

## <span data-ttu-id="3954e-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="3954e-139">RELATED LINKS</span></span>

[<span data-ttu-id="3954e-140">AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="3954e-140">Get-AzureRmIntegrationAccountMap</span></span>](./Get-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="3954e-141">新-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="3954e-141">New-AzureRmIntegrationAccountMap</span></span>](./New-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="3954e-142">Set-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="3954e-142">Set-AzureRmIntegrationAccountMap</span></span>](./Set-AzureRmIntegrationAccountMap.md)


