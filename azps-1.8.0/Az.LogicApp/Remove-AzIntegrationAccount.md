---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 607FBE75-727D-4388-9504-94AD31BCDBBF
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccount.md
ms.openlocfilehash: b1833f2a87f21df7f7826ad395564fd4fe4151be
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787081"
---
# <span data-ttu-id="fa9ec-101">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="fa9ec-101">Remove-AzIntegrationAccount</span></span>

## <span data-ttu-id="fa9ec-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fa9ec-102">SYNOPSIS</span></span>
<span data-ttu-id="fa9ec-103">移除整合帳戶。</span><span class="sxs-lookup"><span data-stu-id="fa9ec-103">Removes an integration account.</span></span>

## <span data-ttu-id="fa9ec-104">句法</span><span class="sxs-lookup"><span data-stu-id="fa9ec-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccount -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa9ec-105">說明</span><span class="sxs-lookup"><span data-stu-id="fa9ec-105">DESCRIPTION</span></span>
<span data-ttu-id="fa9ec-106">**AzIntegrationAccount** Cmdlet 會從資源群組中移除整合帳戶。</span><span class="sxs-lookup"><span data-stu-id="fa9ec-106">The **Remove-AzIntegrationAccount** cmdlet removes an integration account from a resource group.</span></span>
<span data-ttu-id="fa9ec-107">指定整合帳戶名稱和資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="fa9ec-107">Specify the integration account name and resource group name.</span></span>
<span data-ttu-id="fa9ec-108">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="fa9ec-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="fa9ec-109">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="fa9ec-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="fa9ec-110">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="fa9ec-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="fa9ec-111">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="fa9ec-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="fa9ec-112">示例</span><span class="sxs-lookup"><span data-stu-id="fa9ec-112">EXAMPLES</span></span>

### <span data-ttu-id="fa9ec-113">範例1：移除整合帳戶</span><span class="sxs-lookup"><span data-stu-id="fa9ec-113">Example 1: Remove an integration account</span></span>
```
PS C:\>Remove-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Force
```

<span data-ttu-id="fa9ec-114">這個命令會移除名為 IntegrationAccount31 的整合帳戶。</span><span class="sxs-lookup"><span data-stu-id="fa9ec-114">This command removes an integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="fa9ec-115">參數</span><span class="sxs-lookup"><span data-stu-id="fa9ec-115">PARAMETERS</span></span>

### <span data-ttu-id="fa9ec-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa9ec-116">-DefaultProfile</span></span>
<span data-ttu-id="fa9ec-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="fa9ec-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fa9ec-118">-Force</span><span class="sxs-lookup"><span data-stu-id="fa9ec-118">-Force</span></span>
<span data-ttu-id="fa9ec-119">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="fa9ec-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fa9ec-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="fa9ec-120">-Name</span></span>
<span data-ttu-id="fa9ec-121">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="fa9ec-121">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="fa9ec-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa9ec-122">-ResourceGroupName</span></span>
<span data-ttu-id="fa9ec-123">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fa9ec-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="fa9ec-124">-確認</span><span class="sxs-lookup"><span data-stu-id="fa9ec-124">-Confirm</span></span>
<span data-ttu-id="fa9ec-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fa9ec-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa9ec-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa9ec-126">-WhatIf</span></span>
<span data-ttu-id="fa9ec-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fa9ec-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa9ec-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fa9ec-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa9ec-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa9ec-129">CommonParameters</span></span>
<span data-ttu-id="fa9ec-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fa9ec-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa9ec-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fa9ec-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa9ec-132">輸入</span><span class="sxs-lookup"><span data-stu-id="fa9ec-132">INPUTS</span></span>

### <span data-ttu-id="fa9ec-133">System.object</span><span class="sxs-lookup"><span data-stu-id="fa9ec-133">System.String</span></span>

## <span data-ttu-id="fa9ec-134">輸出</span><span class="sxs-lookup"><span data-stu-id="fa9ec-134">OUTPUTS</span></span>

### <span data-ttu-id="fa9ec-135">System.void</span><span class="sxs-lookup"><span data-stu-id="fa9ec-135">System.Void</span></span>

## <span data-ttu-id="fa9ec-136">筆記</span><span class="sxs-lookup"><span data-stu-id="fa9ec-136">NOTES</span></span>

## <span data-ttu-id="fa9ec-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="fa9ec-137">RELATED LINKS</span></span>

[<span data-ttu-id="fa9ec-138">新-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="fa9ec-138">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="fa9ec-139">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="fa9ec-139">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)

[<span data-ttu-id="fa9ec-140">AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="fa9ec-140">Get-AzIntegrationAccount</span></span>](./Get-AzIntegrationAccount.md)


