---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 607FBE75-727D-4388-9504-94AD31BCDBBF
online version: https://docs.microsoft.com/powershell/module/az.logicapp/remove-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccount.md
ms.openlocfilehash: d1f15544223a20113a40975780aa8ca899205f7e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904422"
---
# <span data-ttu-id="0e646-101">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="0e646-101">Remove-AzIntegrationAccount</span></span>

## <span data-ttu-id="0e646-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0e646-102">SYNOPSIS</span></span>
<span data-ttu-id="0e646-103">移除整合帳戶。</span><span class="sxs-lookup"><span data-stu-id="0e646-103">Removes an integration account.</span></span>

## <span data-ttu-id="0e646-104">語法</span><span class="sxs-lookup"><span data-stu-id="0e646-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccount -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e646-105">描述</span><span class="sxs-lookup"><span data-stu-id="0e646-105">DESCRIPTION</span></span>
<span data-ttu-id="0e646-106">**Remove-Az一Account** Cmdlet 會從資源群組移除整合帳戶。</span><span class="sxs-lookup"><span data-stu-id="0e646-106">The **Remove-AzIntegrationAccount** cmdlet removes an integration account from a resource group.</span></span>
<span data-ttu-id="0e646-107">指定整合帳戶名稱和資源組名。</span><span class="sxs-lookup"><span data-stu-id="0e646-107">Specify the integration account name and resource group name.</span></span>
<span data-ttu-id="0e646-108">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="0e646-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="0e646-109">若要使用動態參數，請于命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="0e646-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="0e646-110">若要探索動態參數的名稱，在 Cmdlet 名稱之後輸入連字號 (-) ，然後重複按 Tab 鍵以迴圈流覽可用的參數。</span><span class="sxs-lookup"><span data-stu-id="0e646-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="0e646-111">如果您省略必要的範本參數，Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="0e646-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="0e646-112">例子</span><span class="sxs-lookup"><span data-stu-id="0e646-112">EXAMPLES</span></span>

### <span data-ttu-id="0e646-113">範例 1：移除整合帳戶</span><span class="sxs-lookup"><span data-stu-id="0e646-113">Example 1: Remove an integration account</span></span>
```
PS C:\>Remove-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Force
```

<span data-ttu-id="0e646-114">此命令會移除一個名為 IntegrationAccount31 的整合帳戶。</span><span class="sxs-lookup"><span data-stu-id="0e646-114">This command removes an integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="0e646-115">參數</span><span class="sxs-lookup"><span data-stu-id="0e646-115">PARAMETERS</span></span>

### <span data-ttu-id="0e646-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e646-116">-DefaultProfile</span></span>
<span data-ttu-id="0e646-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="0e646-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0e646-118">-強制</span><span class="sxs-lookup"><span data-stu-id="0e646-118">-Force</span></span>
<span data-ttu-id="0e646-119">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="0e646-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0e646-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="0e646-120">-Name</span></span>
<span data-ttu-id="0e646-121">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="0e646-121">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="0e646-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e646-122">-ResourceGroupName</span></span>
<span data-ttu-id="0e646-123">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0e646-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="0e646-124">-確認</span><span class="sxs-lookup"><span data-stu-id="0e646-124">-Confirm</span></span>
<span data-ttu-id="0e646-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0e646-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e646-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e646-126">-WhatIf</span></span>
<span data-ttu-id="0e646-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0e646-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e646-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0e646-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e646-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e646-129">CommonParameters</span></span>
<span data-ttu-id="0e646-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0e646-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e646-131">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="0e646-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e646-132">輸入</span><span class="sxs-lookup"><span data-stu-id="0e646-132">INPUTS</span></span>

### <span data-ttu-id="0e646-133">System.String</span><span class="sxs-lookup"><span data-stu-id="0e646-133">System.String</span></span>

## <span data-ttu-id="0e646-134">輸出</span><span class="sxs-lookup"><span data-stu-id="0e646-134">OUTPUTS</span></span>

### <span data-ttu-id="0e646-135">System.Void</span><span class="sxs-lookup"><span data-stu-id="0e646-135">System.Void</span></span>

## <span data-ttu-id="0e646-136">筆記</span><span class="sxs-lookup"><span data-stu-id="0e646-136">NOTES</span></span>

## <span data-ttu-id="0e646-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="0e646-137">RELATED LINKS</span></span>

[<span data-ttu-id="0e646-138">New-AzCountAccount</span><span class="sxs-lookup"><span data-stu-id="0e646-138">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="0e646-139">Set-AzCountAccount</span><span class="sxs-lookup"><span data-stu-id="0e646-139">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)

[<span data-ttu-id="0e646-140">Get-AzCountAccount</span><span class="sxs-lookup"><span data-stu-id="0e646-140">Get-AzIntegrationAccount</span></span>](./Get-AzIntegrationAccount.md)


