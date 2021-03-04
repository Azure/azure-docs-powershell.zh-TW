---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C1C0F69D-6A3F-4523-BB70-27676A3DDCBD
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnection.md
ms.openlocfilehash: 0534f05bcc59a109851188c8b585badfc90d61c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916672"
---
# <span data-ttu-id="57259-101">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="57259-101">Remove-AzAutomationConnection</span></span>

## <span data-ttu-id="57259-102">簡介</span><span class="sxs-lookup"><span data-stu-id="57259-102">SYNOPSIS</span></span>
<span data-ttu-id="57259-103">移除自動化連接。</span><span class="sxs-lookup"><span data-stu-id="57259-103">Removes an Automation connection.</span></span>

## <span data-ttu-id="57259-104">語法</span><span class="sxs-lookup"><span data-stu-id="57259-104">SYNTAX</span></span>

```
Remove-AzAutomationConnection [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="57259-105">描述</span><span class="sxs-lookup"><span data-stu-id="57259-105">DESCRIPTION</span></span>
<span data-ttu-id="57259-106">**Remove-AzAutomationConnection** Cmdlet 會從 Azure Automation 移除一個連接。</span><span class="sxs-lookup"><span data-stu-id="57259-106">The **Remove-AzAutomationConnection** cmdlet removes a connection from Azure Automation.</span></span>

## <span data-ttu-id="57259-107">例子</span><span class="sxs-lookup"><span data-stu-id="57259-107">EXAMPLES</span></span>

### <span data-ttu-id="57259-108">範例 1：移除連接</span><span class="sxs-lookup"><span data-stu-id="57259-108">Example 1: Remove a connection</span></span>
```
PS C:\>Remove-AzAutomationConnection -AutomationAccountName "Contoso17" -Name "ContosoConnection" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="57259-109">此命令會移除自動化帳戶中名為 Contoso17 的 ContosoConnection 憑證。</span><span class="sxs-lookup"><span data-stu-id="57259-109">This command removes a certificate named ContosoConnection in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="57259-110">參數</span><span class="sxs-lookup"><span data-stu-id="57259-110">PARAMETERS</span></span>

### <span data-ttu-id="57259-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="57259-111">-AutomationAccountName</span></span>
<span data-ttu-id="57259-112">指定此 Cmdlet 移除連接的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="57259-112">Specifies the name of the automation account for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="57259-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57259-113">-DefaultProfile</span></span>
<span data-ttu-id="57259-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="57259-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="57259-115">-強制</span><span class="sxs-lookup"><span data-stu-id="57259-115">-Force</span></span>
<span data-ttu-id="57259-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="57259-116">ps_force</span></span>

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

### <span data-ttu-id="57259-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="57259-117">-Name</span></span>
<span data-ttu-id="57259-118">指定此 Cmdlet 移除的連接名稱。</span><span class="sxs-lookup"><span data-stu-id="57259-118">Specifies the name of the connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="57259-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57259-119">-ResourceGroupName</span></span>
<span data-ttu-id="57259-120">指定此 Cmdlet 移除其連接的資源組名。</span><span class="sxs-lookup"><span data-stu-id="57259-120">Specifies the name of the resource group for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="57259-121">-確認</span><span class="sxs-lookup"><span data-stu-id="57259-121">-Confirm</span></span>
<span data-ttu-id="57259-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="57259-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57259-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57259-123">-WhatIf</span></span>
<span data-ttu-id="57259-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="57259-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57259-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="57259-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57259-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57259-126">CommonParameters</span></span>
<span data-ttu-id="57259-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="57259-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57259-128">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="57259-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57259-129">輸入</span><span class="sxs-lookup"><span data-stu-id="57259-129">INPUTS</span></span>

### <span data-ttu-id="57259-130">System.String</span><span class="sxs-lookup"><span data-stu-id="57259-130">System.String</span></span>

## <span data-ttu-id="57259-131">輸出</span><span class="sxs-lookup"><span data-stu-id="57259-131">OUTPUTS</span></span>

### <span data-ttu-id="57259-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="57259-132">System.Void</span></span>

## <span data-ttu-id="57259-133">筆記</span><span class="sxs-lookup"><span data-stu-id="57259-133">NOTES</span></span>

## <span data-ttu-id="57259-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="57259-134">RELATED LINKS</span></span>

[<span data-ttu-id="57259-135">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="57259-135">Get-AzAutomationConnection</span></span>](./Get-AzAutomationConnection.md)

[<span data-ttu-id="57259-136">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="57259-136">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)


