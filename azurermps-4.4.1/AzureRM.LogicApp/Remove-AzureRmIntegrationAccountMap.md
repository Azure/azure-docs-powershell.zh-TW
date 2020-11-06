---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 7AAF2ACC-84ED-449C-B1E8-F074463F44EB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountMap.md
ms.openlocfilehash: a7104f33fd2e5b9428b062bd8ac359ccabb25520
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453451"
---
# <span data-ttu-id="61f03-101">Remove-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="61f03-101">Remove-AzureRmIntegrationAccountMap</span></span>

## <span data-ttu-id="61f03-102">摘要</span><span class="sxs-lookup"><span data-stu-id="61f03-102">SYNOPSIS</span></span>
<span data-ttu-id="61f03-103">移除整合帳戶對應。</span><span class="sxs-lookup"><span data-stu-id="61f03-103">Removes an integration account map.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61f03-104">句法</span><span class="sxs-lookup"><span data-stu-id="61f03-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61f03-105">說明</span><span class="sxs-lookup"><span data-stu-id="61f03-105">DESCRIPTION</span></span>
<span data-ttu-id="61f03-106">**AzureRmIntegrationAccountMap** Cmdlet 會從資源群組中移除整合帳戶地圖。</span><span class="sxs-lookup"><span data-stu-id="61f03-106">The **Remove-AzureRmIntegrationAccountMap** cmdlet removes an integration account map from a resource group.</span></span>
<span data-ttu-id="61f03-107">指定整合帳戶名稱、資源群組名稱和地圖名稱。</span><span class="sxs-lookup"><span data-stu-id="61f03-107">Specify the integration account name, resource group name, and map name.</span></span>

<span data-ttu-id="61f03-108">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="61f03-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="61f03-109">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="61f03-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="61f03-110">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="61f03-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="61f03-111">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="61f03-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="61f03-112">示例</span><span class="sxs-lookup"><span data-stu-id="61f03-112">EXAMPLES</span></span>

### <span data-ttu-id="61f03-113">範例1：移除整合帳戶對應圖</span><span class="sxs-lookup"><span data-stu-id="61f03-113">Example 1: Remove an integration account map</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47"
```

<span data-ttu-id="61f03-114">這個命令會移除名為 IntegrationAccountMap47 的整合帳戶地圖。</span><span class="sxs-lookup"><span data-stu-id="61f03-114">This command removes the integration account map named IntegrationAccountMap47.</span></span>

## <span data-ttu-id="61f03-115">參數</span><span class="sxs-lookup"><span data-stu-id="61f03-115">PARAMETERS</span></span>

### <span data-ttu-id="61f03-116">-Force</span><span class="sxs-lookup"><span data-stu-id="61f03-116">-Force</span></span>
<span data-ttu-id="61f03-117">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="61f03-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="61f03-118">-MapName</span><span class="sxs-lookup"><span data-stu-id="61f03-118">-MapName</span></span>
<span data-ttu-id="61f03-119">指定整合帳戶對應的名稱。</span><span class="sxs-lookup"><span data-stu-id="61f03-119">Specifies the name of the integration account map.</span></span>

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

### <span data-ttu-id="61f03-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="61f03-120">-Name</span></span>
<span data-ttu-id="61f03-121">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="61f03-121">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="61f03-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61f03-122">-ResourceGroupName</span></span>
<span data-ttu-id="61f03-123">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="61f03-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="61f03-124">-確認</span><span class="sxs-lookup"><span data-stu-id="61f03-124">-Confirm</span></span>
<span data-ttu-id="61f03-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="61f03-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61f03-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61f03-126">-WhatIf</span></span>
<span data-ttu-id="61f03-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="61f03-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61f03-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="61f03-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61f03-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61f03-129">-DefaultProfile</span></span>
<span data-ttu-id="61f03-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="61f03-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61f03-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61f03-131">CommonParameters</span></span>
<span data-ttu-id="61f03-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="61f03-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61f03-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="61f03-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61f03-134">輸入</span><span class="sxs-lookup"><span data-stu-id="61f03-134">INPUTS</span></span>

## <span data-ttu-id="61f03-135">輸出</span><span class="sxs-lookup"><span data-stu-id="61f03-135">OUTPUTS</span></span>

## <span data-ttu-id="61f03-136">筆記</span><span class="sxs-lookup"><span data-stu-id="61f03-136">NOTES</span></span>

## <span data-ttu-id="61f03-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="61f03-137">RELATED LINKS</span></span>

[<span data-ttu-id="61f03-138">AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="61f03-138">Get-AzureRmIntegrationAccountMap</span></span>](./Get-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="61f03-139">新-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="61f03-139">New-AzureRmIntegrationAccountMap</span></span>](./New-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="61f03-140">Set-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="61f03-140">Set-AzureRmIntegrationAccountMap</span></span>](./Set-AzureRmIntegrationAccountMap.md)


