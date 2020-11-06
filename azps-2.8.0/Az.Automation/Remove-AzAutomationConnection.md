---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C1C0F69D-6A3F-4523-BB70-27676A3DDCBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnection.md
ms.openlocfilehash: 76f82e81ca9593865fea642d44bf1bde58f60eb2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613717"
---
# <span data-ttu-id="f0e27-101">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="f0e27-101">Remove-AzAutomationConnection</span></span>

## <span data-ttu-id="f0e27-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f0e27-102">SYNOPSIS</span></span>
<span data-ttu-id="f0e27-103">移除 [自動化] 連線。</span><span class="sxs-lookup"><span data-stu-id="f0e27-103">Removes an Automation connection.</span></span>

## <span data-ttu-id="f0e27-104">句法</span><span class="sxs-lookup"><span data-stu-id="f0e27-104">SYNTAX</span></span>

```
Remove-AzAutomationConnection [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f0e27-105">說明</span><span class="sxs-lookup"><span data-stu-id="f0e27-105">DESCRIPTION</span></span>
<span data-ttu-id="f0e27-106">**AzAutomationConnection** Cmdlet 會從 Azure 自動化中移除連線。</span><span class="sxs-lookup"><span data-stu-id="f0e27-106">The **Remove-AzAutomationConnection** cmdlet removes a connection from Azure Automation.</span></span>

## <span data-ttu-id="f0e27-107">示例</span><span class="sxs-lookup"><span data-stu-id="f0e27-107">EXAMPLES</span></span>

### <span data-ttu-id="f0e27-108">範例1：移除連線</span><span class="sxs-lookup"><span data-stu-id="f0e27-108">Example 1: Remove a connection</span></span>
```
PS C:\>Remove-AzAutomationConnection -AutomationAccountName "Contoso17" -Name "ContosoConnection" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f0e27-109">這個命令會在名為 [Contoso17] 的自動化帳戶中移除名為 ContosoConnection 的憑證。</span><span class="sxs-lookup"><span data-stu-id="f0e27-109">This command removes a certificate named ContosoConnection in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="f0e27-110">參數</span><span class="sxs-lookup"><span data-stu-id="f0e27-110">PARAMETERS</span></span>

### <span data-ttu-id="f0e27-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f0e27-111">-AutomationAccountName</span></span>
<span data-ttu-id="f0e27-112">指定此 Cmdlet 移除連線之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="f0e27-112">Specifies the name of the automation account for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="f0e27-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0e27-113">-DefaultProfile</span></span>
<span data-ttu-id="f0e27-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f0e27-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f0e27-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f0e27-115">-Force</span></span>
<span data-ttu-id="f0e27-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="f0e27-116">ps_force</span></span>

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

### <span data-ttu-id="f0e27-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="f0e27-117">-Name</span></span>
<span data-ttu-id="f0e27-118">指定此 Cmdlet 移除的連線名稱。</span><span class="sxs-lookup"><span data-stu-id="f0e27-118">Specifies the name of the connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f0e27-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0e27-119">-ResourceGroupName</span></span>
<span data-ttu-id="f0e27-120">指定此 Cmdlet 移除連線之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f0e27-120">Specifies the name of the resource group for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="f0e27-121">-確認</span><span class="sxs-lookup"><span data-stu-id="f0e27-121">-Confirm</span></span>
<span data-ttu-id="f0e27-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f0e27-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0e27-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0e27-123">-WhatIf</span></span>
<span data-ttu-id="f0e27-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f0e27-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0e27-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f0e27-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0e27-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0e27-126">CommonParameters</span></span>
<span data-ttu-id="f0e27-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f0e27-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0e27-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f0e27-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0e27-129">輸入</span><span class="sxs-lookup"><span data-stu-id="f0e27-129">INPUTS</span></span>

### <span data-ttu-id="f0e27-130">System.object</span><span class="sxs-lookup"><span data-stu-id="f0e27-130">System.String</span></span>

## <span data-ttu-id="f0e27-131">輸出</span><span class="sxs-lookup"><span data-stu-id="f0e27-131">OUTPUTS</span></span>

### <span data-ttu-id="f0e27-132">System.void</span><span class="sxs-lookup"><span data-stu-id="f0e27-132">System.Void</span></span>

## <span data-ttu-id="f0e27-133">筆記</span><span class="sxs-lookup"><span data-stu-id="f0e27-133">NOTES</span></span>

## <span data-ttu-id="f0e27-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="f0e27-134">RELATED LINKS</span></span>

[<span data-ttu-id="f0e27-135">AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="f0e27-135">Get-AzAutomationConnection</span></span>](./Get-AzAutomationConnection.md)

[<span data-ttu-id="f0e27-136">新-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="f0e27-136">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)

