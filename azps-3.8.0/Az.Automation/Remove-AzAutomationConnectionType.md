---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 92B69069-0F98-428A-B05C-BBA09EBC0381
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationconnectiontype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnectionType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnectionType.md
ms.openlocfilehash: 5eb31abcc632f06402b4196be8be4c5e32cdacf0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93966383"
---
# <span data-ttu-id="f70bf-101">Remove-AzAutomationConnectionType</span><span class="sxs-lookup"><span data-stu-id="f70bf-101">Remove-AzAutomationConnectionType</span></span>

## <span data-ttu-id="f70bf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f70bf-102">SYNOPSIS</span></span>
<span data-ttu-id="f70bf-103">移除自動化連線類型。</span><span class="sxs-lookup"><span data-stu-id="f70bf-103">Removes an Automation connection type.</span></span>

## <span data-ttu-id="f70bf-104">句法</span><span class="sxs-lookup"><span data-stu-id="f70bf-104">SYNTAX</span></span>

```
Remove-AzAutomationConnectionType [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f70bf-105">說明</span><span class="sxs-lookup"><span data-stu-id="f70bf-105">DESCRIPTION</span></span>
<span data-ttu-id="f70bf-106">**AzAutomationConnectionType** Cmdlet 會從 Azure 自動化中移除連線類型。</span><span class="sxs-lookup"><span data-stu-id="f70bf-106">The **Remove-AzAutomationConnectionType** cmdlet removes a connection type from Azure Automation.</span></span>
<span data-ttu-id="f70bf-107">所有與您刪除之連線類型相關聯的連線都無法使用。</span><span class="sxs-lookup"><span data-stu-id="f70bf-107">All connections that are associated with the connection type that you delete become unusable.</span></span>
<span data-ttu-id="f70bf-108">除非您建立符合下列條件的新連線類型，否則請移除它們：</span><span class="sxs-lookup"><span data-stu-id="f70bf-108">Remove them, unless you create a new connection type that meets the following criteria:</span></span> 
- <span data-ttu-id="f70bf-109">類型與原始連線類型的名稱相同。</span><span class="sxs-lookup"><span data-stu-id="f70bf-109">The type has the same name as the original connection type.</span></span> 
- <span data-ttu-id="f70bf-110">該類型具有與原始連線類型相同的欄位定義。</span><span class="sxs-lookup"><span data-stu-id="f70bf-110">The type has the same field definitions as the original connection type.</span></span>
<span data-ttu-id="f70bf-111">它可以有其他欄位。</span><span class="sxs-lookup"><span data-stu-id="f70bf-111">It can have additional fields.</span></span>

## <span data-ttu-id="f70bf-112">示例</span><span class="sxs-lookup"><span data-stu-id="f70bf-112">EXAMPLES</span></span>

### <span data-ttu-id="f70bf-113">範例1：移除連線類型</span><span class="sxs-lookup"><span data-stu-id="f70bf-113">Example 1: Remove a connection type</span></span>
```
PS C:\>Remove-AzAutomationConnectionType -AutomationAccountName "Contoso17" -Name "ContosoConnectionType" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f70bf-114">這個命令會在名為 Contoso17 的自動化帳戶中，移除一個名為 ContosoConnectionType 的連線類型。</span><span class="sxs-lookup"><span data-stu-id="f70bf-114">This command removes a connection type named ContosoConnectionType in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="f70bf-115">參數</span><span class="sxs-lookup"><span data-stu-id="f70bf-115">PARAMETERS</span></span>

### <span data-ttu-id="f70bf-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f70bf-116">-AutomationAccountName</span></span>
<span data-ttu-id="f70bf-117">指定此 Cmdlet 移除連線類型之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="f70bf-117">Specifies the name of the Automation account for which this cmdlet removes a connection type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f70bf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f70bf-118">-DefaultProfile</span></span>
<span data-ttu-id="f70bf-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f70bf-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f70bf-120">-Force</span><span class="sxs-lookup"><span data-stu-id="f70bf-120">-Force</span></span>
<span data-ttu-id="f70bf-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="f70bf-121">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f70bf-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="f70bf-122">-Name</span></span>
<span data-ttu-id="f70bf-123">指定此 Cmdlet 移除之自動化連線類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="f70bf-123">Specifies the name of the Automation connection type that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f70bf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f70bf-124">-ResourceGroupName</span></span>
<span data-ttu-id="f70bf-125">指定此 Cmdlet 移除自動化連線類型之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f70bf-125">Specifies the name of the resource group from which this cmdlet removes an Automation connection type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f70bf-126">-確認</span><span class="sxs-lookup"><span data-stu-id="f70bf-126">-Confirm</span></span>
<span data-ttu-id="f70bf-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f70bf-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f70bf-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f70bf-128">-WhatIf</span></span>
<span data-ttu-id="f70bf-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f70bf-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f70bf-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f70bf-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f70bf-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f70bf-131">CommonParameters</span></span>
<span data-ttu-id="f70bf-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f70bf-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f70bf-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f70bf-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f70bf-134">輸入</span><span class="sxs-lookup"><span data-stu-id="f70bf-134">INPUTS</span></span>

### <span data-ttu-id="f70bf-135">System.object</span><span class="sxs-lookup"><span data-stu-id="f70bf-135">System.String</span></span>

## <span data-ttu-id="f70bf-136">輸出</span><span class="sxs-lookup"><span data-stu-id="f70bf-136">OUTPUTS</span></span>

### <span data-ttu-id="f70bf-137">System.void</span><span class="sxs-lookup"><span data-stu-id="f70bf-137">System.Void</span></span>

## <span data-ttu-id="f70bf-138">筆記</span><span class="sxs-lookup"><span data-stu-id="f70bf-138">NOTES</span></span>

## <span data-ttu-id="f70bf-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="f70bf-139">RELATED LINKS</span></span>

[<span data-ttu-id="f70bf-140">移除-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="f70bf-140">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)

