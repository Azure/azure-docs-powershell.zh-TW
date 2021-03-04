---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 92B69069-0F98-428A-B05C-BBA09EBC0381
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationconnectiontype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnectionType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnectionType.md
ms.openlocfilehash: 4d153a05ad245eeece671adced6aa2f8029dc9a2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916671"
---
# <span data-ttu-id="ddde0-101">Remove-AzAutomationConnectionType</span><span class="sxs-lookup"><span data-stu-id="ddde0-101">Remove-AzAutomationConnectionType</span></span>

## <span data-ttu-id="ddde0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ddde0-102">SYNOPSIS</span></span>
<span data-ttu-id="ddde0-103">移除自動化連線類型。</span><span class="sxs-lookup"><span data-stu-id="ddde0-103">Removes an Automation connection type.</span></span>

## <span data-ttu-id="ddde0-104">語法</span><span class="sxs-lookup"><span data-stu-id="ddde0-104">SYNTAX</span></span>

```
Remove-AzAutomationConnectionType [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ddde0-105">描述</span><span class="sxs-lookup"><span data-stu-id="ddde0-105">DESCRIPTION</span></span>
<span data-ttu-id="ddde0-106">**Remove-AzAutomationConnectionType** Cmdlet 會從 Azure Automation 移除連線類型。</span><span class="sxs-lookup"><span data-stu-id="ddde0-106">The **Remove-AzAutomationConnectionType** cmdlet removes a connection type from Azure Automation.</span></span>
<span data-ttu-id="ddde0-107">所有與您刪除之連線類型相關聯的連結將無法使用。</span><span class="sxs-lookup"><span data-stu-id="ddde0-107">All connections that are associated with the connection type that you delete become unusable.</span></span>
<span data-ttu-id="ddde0-108">除非建立符合下列準則的新連線類型，否則將它們移除：</span><span class="sxs-lookup"><span data-stu-id="ddde0-108">Remove them, unless you create a new connection type that meets the following criteria:</span></span> 
- <span data-ttu-id="ddde0-109">該類型與原始連線類型的名稱相同。</span><span class="sxs-lookup"><span data-stu-id="ddde0-109">The type has the same name as the original connection type.</span></span> 
- <span data-ttu-id="ddde0-110">類型具有與原始連線類型相同的欄位定義。</span><span class="sxs-lookup"><span data-stu-id="ddde0-110">The type has the same field definitions as the original connection type.</span></span>
<span data-ttu-id="ddde0-111">它可以有其他欄位。</span><span class="sxs-lookup"><span data-stu-id="ddde0-111">It can have additional fields.</span></span>

## <span data-ttu-id="ddde0-112">例子</span><span class="sxs-lookup"><span data-stu-id="ddde0-112">EXAMPLES</span></span>

### <span data-ttu-id="ddde0-113">範例 1：移除連線類型</span><span class="sxs-lookup"><span data-stu-id="ddde0-113">Example 1: Remove a connection type</span></span>
```
PS C:\>Remove-AzAutomationConnectionType -AutomationAccountName "Contoso17" -Name "ContosoConnectionType" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ddde0-114">此命令會移除自動化帳戶中名為 Contoso17 的 ContosoConnectionType 連線類型。</span><span class="sxs-lookup"><span data-stu-id="ddde0-114">This command removes a connection type named ContosoConnectionType in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="ddde0-115">參數</span><span class="sxs-lookup"><span data-stu-id="ddde0-115">PARAMETERS</span></span>

### <span data-ttu-id="ddde0-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ddde0-116">-AutomationAccountName</span></span>
<span data-ttu-id="ddde0-117">指定此 Cmdlet 移除連線類型的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="ddde0-117">Specifies the name of the Automation account for which this cmdlet removes a connection type.</span></span>

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

### <span data-ttu-id="ddde0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddde0-118">-DefaultProfile</span></span>
<span data-ttu-id="ddde0-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="ddde0-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ddde0-120">-強制</span><span class="sxs-lookup"><span data-stu-id="ddde0-120">-Force</span></span>
<span data-ttu-id="ddde0-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="ddde0-121">ps_force</span></span>

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

### <span data-ttu-id="ddde0-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="ddde0-122">-Name</span></span>
<span data-ttu-id="ddde0-123">指定此 Cmdlet 移除的自動化連線類型名稱。</span><span class="sxs-lookup"><span data-stu-id="ddde0-123">Specifies the name of the Automation connection type that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ddde0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddde0-124">-ResourceGroupName</span></span>
<span data-ttu-id="ddde0-125">指定此 Cmdlet 移除自動化連線類型之資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ddde0-125">Specifies the name of the resource group from which this cmdlet removes an Automation connection type.</span></span>

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

### <span data-ttu-id="ddde0-126">-確認</span><span class="sxs-lookup"><span data-stu-id="ddde0-126">-Confirm</span></span>
<span data-ttu-id="ddde0-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ddde0-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddde0-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddde0-128">-WhatIf</span></span>
<span data-ttu-id="ddde0-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ddde0-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddde0-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ddde0-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddde0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddde0-131">CommonParameters</span></span>
<span data-ttu-id="ddde0-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ddde0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddde0-133">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="ddde0-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddde0-134">輸入</span><span class="sxs-lookup"><span data-stu-id="ddde0-134">INPUTS</span></span>

### <span data-ttu-id="ddde0-135">System.String</span><span class="sxs-lookup"><span data-stu-id="ddde0-135">System.String</span></span>

## <span data-ttu-id="ddde0-136">輸出</span><span class="sxs-lookup"><span data-stu-id="ddde0-136">OUTPUTS</span></span>

### <span data-ttu-id="ddde0-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="ddde0-137">System.Void</span></span>

## <span data-ttu-id="ddde0-138">筆記</span><span class="sxs-lookup"><span data-stu-id="ddde0-138">NOTES</span></span>

## <span data-ttu-id="ddde0-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="ddde0-139">RELATED LINKS</span></span>

[<span data-ttu-id="ddde0-140">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="ddde0-140">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


